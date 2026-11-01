---
document_id: TECH-LEAD-VISION
title: Escolhas de tecnologias — plataforma de cursos
status: fictional-example
version: 2.0.0
depends_on:
  - DOC-06
  - DOC-07
reconciled_with:
  - Infraestrutura_e_Plano_de_Fundacao
governs:
  - languages
  - runtimes
  - frameworks
  - libraries
  - toolchain
  - technology-standards
---

# Escolhas de tecnologias — plataforma de cursos

> **Estudo fictício, versão 2.0.** Requisitos, decisões, aprovações e cenários abaixo são ilustrativos. Nenhuma aplicação, pesquisa com usuários, contratação, implantação ou teste deste produto foi executado. Consulte o [índice e a autoridade de cada assunto](README.md).

## 1. Objetivo

Materializar o Documento 06 e o Documento 07 em um conjunto de tecnologias explícito, pequeno, coerente e adequado a uma equipe reduzida.

A sequência deste exemplo é:

**Passos ilustrativos:**

1. DOC-06.
2. qualidade e disciplina de código.
3. DOC-07.
4. forças + arquitetura + limites entre componentes.
5. VISÃO DO TECH LEAD.
6. linguagem + runtime + frameworks + libraries + tooling.
7. INFRAESTRUTURA.
8. fornecedores e ambientes compatíveis.

Este documento não altera a arquitetura para acomodar uma tecnologia preferida.

## 2. Necessidades recebidas da arquitetura

```text
TL-NEED-001 — Web e API compartilham contratos tipados sem acoplar domínio a framework.
TL-NEED-002 — packages/domain permanece independente de UI, HTTP, banco e fornecedores.
TL-NEED-003 — web e API possuem build/deploy independentes no mesmo monorepo.
TL-NEED-004 — entradas externas possuem validação durante a execução.
TL-NEED-005 — persistência principal é relacional, transacional e indexável.
TL-NEED-006 — unit, integration, E2E e verificações de dependências são automatizáveis.
TL-NEED-007 — equipe pequena exige baixa quantidade de modelos mentais/tooling sobreposto.
TL-NEED-008 — não existe requisito de SSR no Beta.
TL-NEED-009 — API HTTP deve ser stateless.
TL-NEED-010 — integrações com software corporativo entram por adapters/ports.
```

## 3. Verificações antes de adotar

A tabela seguinte ilustra responsabilidades e restrições de uso. Não é uma pesquisa atual de versões ou uma recomendação universal. Antes de adotar, registrar versão exata, suporte, licença, manutenção, segurança, requisitos de runtime e compatibilidade na [Issue de pesquisa](issues-e-criterios.md). Conferir documentação oficial e executar uma prova pequena para os contratos críticos.

Não há lockfile, instalação ou execução neste exemplo. Nenhuma versão está homologada. Não copiar a seleção para um produto sem comparação contextual. Usar o [registro de comparação](comparacao-e-decisao.md) e o [catálogo de fontes do método](../../docs/fontes-de-referencia.md) como orientação de pesquisa, sem tratá-lo como validação desta combinação.

## 4. Seleção ilustrativa, pendente de verificação

| Responsabilidade | Decisão | Política |
| --- | --- | --- |
| Linguagem principal | TypeScript (versão a validar) | strict |
| Runtime API/tooling | Node.js (versão a validar) | patch travado no FND |
| Web UI | React (versão a validar) | sem RSC/SSR no Beta |
| Build web | Vite (versão a validar) | configuração mínima |
| Routing web | React Router (versão a validar) | SPA/Data/Declarative conforme necessidade; sem server framework por hábito |
| API HTTP | Fastify (versão a validar) | controladores enxutos + application/domain abaixo |
| Runtime validation | Zod (versão a validar) | limites entre componentes e contratos |
| Banco lógico | PostgreSQL | fornecedor decidido em Infraestrutura |
| Driver SQL da API | `pg` | apenas adapters de infraestrutura |
| Server-state web | `@tanstack/react-query` | cache de dados remotos; não usar como state store genérico |
| Forms | `react-hook-form` quando formulários justificarem | estado simples continua local |
| Unit/integration runner | Vitest (versão a validar) | testes próximos do comportamento |
| UI/component tests | Testing Library | testar comportamento acessível |
| E2E | Playwright | jornadas críticas e smoke |
| Package manager | pnpm | workspace nativo; versão fixada no FND |
| Workspace | pnpm workspaces | sem Turborepo/Nx inicialmente |
| Lint | ESLint + TypeScript ESLint | config compartilhada |
| Formatting | Prettier | sem regras concorrentes de estilo |
| Logging API | logger estruturado do Fastify/Pino | nunca logar secrets |

Na adoção real, versões exatas e versões de ferramentas pertencem ao registro de decisão e ao lockfile. Versão não verificada impede declarar compatibilidade confirmada.

## 5. Organização tecnológica do monorepo

```text
/apps
  /web          React + Vite
  /api          Fastify
/packages
  /domain       TypeScript puro, sem framework/fornecedor
  /contracts    Zod + tipos públicos compartilháveis
  /design-tokens
  /config       configs compartilhadas de tooling
/infra          manifests/scripts operacionais aprovados
/tooling        checks de limites entre componentes e automações locais
/docs
```

Regras:

- `packages/domain` não importa React, Fastify, `pg` ou SDK de fornecedor;
- `packages/contracts` pode expor schemas Zod e tipos inferidos destinados aos limites entre componentes;
- `apps/api` adapta HTTP para application/domain;
- acesso SQL fica atrás de repositories/adapters;
- `apps/web` consome API pública e nunca usa credencial administrativa;
- fornecedor SDK entra somente na camada autorizada por este documento.

## 6. Dados e migrations

### Banco

**PostgreSQL** é escolhido como sistema relacional porque satisfaz `TL-NEED-005` e é a alternativa relacional ilustrativa; conferir os requisitos do fornecedor selecionado.

### Acesso a dados

**Decisão inicial:** não adicionar ORM completo no Beta.

A API utiliza `pg` em adapters/repositories explícitos.

Motivos:

- mantém queries e transações visíveis;
- evita criar segundo modelo de domínio;
- reduz dependências e geração de código;
- permite substituir fornecedor sem alterar regras de negócio.

Os resultados de queries relevantes devem ser mapeados/validados nos limites adequados entre componentes; tipos estáticos não substituem validação de dados externos.

### Migrations

O formato oficial é **SQL versionado no repositório**.

O executor concreto pode ser reconciliado após a escolha do fornecedor, desde que:

- não altere o formato histórico silenciosamente;
- seja reproduzível em CI/staging;
- não faça drift fora do Git.

## 7. Estado e dados no frontend

### Server state

`@tanstack/react-query` é a proposta para cache, sincronização e invalidação de dados vindos da API.

### Estado local

Estado que pertence a uma tela/componente permanece em React local state ou primitives equivalentes.

### State manager global

**Não adicionar Redux, Zustand ou outro state manager global no Beta sem requisito comprovado.**

A proposta é avaliar primeiro estado local, roteamento e cache de consultas. Só uma implementação e suas verificações podem demonstrar suficiência.

### Formulários

`react-hook-form` pode ser usado em formulários administrativos com validação/estado suficiente para justificar a biblioteca. Formulários triviais não precisam de abstração adicional.

## 8. Contratos e validação

Zod é oficial para payloads externos relevantes.

**Passos ilustrativos:**

1. request externa.
2. Zod parse/validation.
3. application input tipado.
4. domain.

Não duplicar schemas equivalentes em web e API quando o contrato puder ser compartilhado com segurança em `packages/contracts`.

Schemas de contrato não devem importar infraestrutura nem regras de UI.

## 9. Testes

### Vitest

Usar para:

- domínio;
- application services;
- utilities especializadas;
- contratos;
- componentes quando o teste em ambiente apropriado produzir valor.

### Testing Library

Usar para comportamento de componentes e superfícies, priorizando semântica/acessibilidade em vez de detalhes internos.

### Playwright

Usar para:

- convite/primeiro acesso;
- contexto de tenant;
- criação de empresa/turma;
- matrícula/trilha;
- conclusão/quiz;
- restrição do gestor;
- certificado;
- smoke de staging.

Teste E2E não substitui testes rápidos de domínio e integração.

## 10. Toolchain e qualidade

### pnpm

Escolhido pela capacidade nativa de workspaces e por reduzir a necessidade de tooling adicional para o monorepo pequeno.

### Sem orquestrador de monorepo inicialmente

**Turborepo/Nx não são adicionados no FND inicial.**

O projeto começa com scripts de workspace e CI simples. Reavaliar somente se tempos de build, cache ou grafo de tarefas criarem necessidade observável.

### Verificações

O conjunto de tecnologias deve materializar comandos equivalentes a:

```text
format:check
lint
typecheck
test
build
check:boundaries
E2E/smoke quando aplicável
```

## 11. Bibliotecas que não são pré-aprovadas

Não existe aprovação genérica para instalar bibliotecas de:

- UI kits completos;
- state managers adicionais;
- ORMs adicionais;
- date libraries;
- charting;
- rich-text editors;
- realtime;
- queues;
- feature flags.

Quando uma funcionalidade real exigir uma delas, comparar alternativas e atualizar **este mesmo documento** se a escolha se tornar padrão do projeto.

## 12. Tecnologias rejeitadas neste estágio

### Next.js

**Não adotado no Beta.**

Não existe requisito atual de SSR, RSC ou backend acoplado ao framework web. A arquitetura já definiu API separada e deploy independente. A hipótese é que React + Vite atenda ao recorte; esforço e compatibilidade continuam por verificar.

Revisitar se requisitos reais de rendering/SEO alterarem essa premissa.

### NestJS

**Não adotado no Beta.**

A equipe é pequena e a arquitetura pede controllers finos, domínio independente e baixa complexidade acidental. A proposta é avaliar Fastify para HTTP; o esforço e a adequação continuam por verificar.

Revisitar apenas se requisitos comprovados de módulos/decorators/ecossistema justificarem a camada adicional.

### ORM completo

**Não adotado inicialmente.**

SQL explícito em adaptadores é a hipótese inicial e preserva controle de queries. Reavaliar se volume de modelagem repetitiva ou migrations tornar o custo manual maior que o benefício.

### Segundo state manager

**Não aprovado.**

Adicionar somente se estado global real não puder ser modelado adequadamente com as ferramentas oficiais.

## 13. Reconciliação após a decisão de Infraestrutura

Na narrativa, a infraestrutura propõe Supabase para PostgreSQL/Auth/Storage, Cloudflare Pages para web, Cloud Run para API e Resend para e-mail.

Essa proposta preserva a arquitetura e prevê integrações específicas do fornecedor e localizadas:

**Passos ilustrativos:**

1. @supabase/supabase-js.
2. —  permitido em adapters de Auth/Storage e integração cliente apenas com credencial pública apropriada.
3. —  service role/secret somente no servidor.
4. pg.
5. —  conexão PostgreSQL da API pelo endpoint/pooler aprovado.
6. resend SDK.
7. —  permitido somente no adapter de Notifications.

A UI e o domínio não passam a depender de Supabase ou Resend por causa dessa aprovação.

Se o fornecedor mudar no futuro, o objetivo é trocar adapters e configuração, não reescrever regras de aprendizagem.

## 14. Saída para Fundação

```text
TL-STACK-001 — TypeScript (versão a validar) aprovado.
TL-STACK-002 — Node.js (versão a validar) aprovado.
TL-STACK-003 — React (versão a validar) + Vite (versão a validar) + React Router (versão a validar) aprovados para web.
TL-STACK-004 — Fastify (versão a validar) aprovado para API.
TL-LIB-001 — Zod (versão a validar) é validação/contrato proposto no exemplo.
TL-LIB-002 — pg é driver SQL ilustrativo da API.
TL-LIB-003 — TanStack Query é a proposta de cache de dados remotos da web.
TL-LIB-004 — React Hook Form é solução aprovada para formulários que justificarem.
TL-TEST-001 — Vitest é runner unit/integration.
TL-TEST-002 — Testing Library é padrão de component behavior tests.
TL-TEST-003 — Playwright é E2E/smoke.
TL-TOOL-001 — pnpm workspaces é workspace/package management.
TL-TOOL-002 — ESLint + TypeScript ESLint + Prettier materializam lint/format.
TL-TOOL-003 — sem monorepo orchestrator no FND inicial.
```

## Critério de qualidade

Em um projeto real, a fonte tecnológica aprovada e verificada deve permitir iniciar a fundação sem inventar escolhas. Neste exemplo, versões e compatibilidade continuam pendentes; o executor deve resolver essas lacunas antes de instalar.

Ao mesmo tempo, ele não recebe autorização para instalar dependências especializadas não previstas apenas porque “podem ser úteis”.
