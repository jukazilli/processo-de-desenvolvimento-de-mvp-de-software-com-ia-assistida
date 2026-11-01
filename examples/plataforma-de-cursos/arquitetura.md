---
document_id: DOC-07
title: Engenharia e Arquitetura
status: fictional-example
version: 2.0.0
depends_on:
  - DOC-02
  - DOC-03
  - DOC-05
  - DOC-06
governs:
  - engineering
  - architecture
  - repository-structure
  - boundaries
  - technology-selection-inputs
  - infrastructure-needs
---

# Engenharia e Arquitetura

> **Estudo fictício, versão 2.0.** Requisitos, decisões, aprovações e cenários abaixo são ilustrativos. Nenhuma aplicação, pesquisa com usuários, contratação, implantação ou teste deste produto foi executado. Consulte o [índice e a autoridade de cada assunto](README.md).

## 1. Forças de engenharia

### ENG-001 — Isolamento entre empresas

Dados de uma empresa nunca podem ser expostos a outra por erro de consulta, navegação ou autorização.

### ENG-002 — Operação por equipe pequena

O Beta será mantido por uma equipe pequena. Baixa complexidade operacional possui prioridade alta.

### ENG-003 — Conteúdo reutilizável

Cursos e materiais precisam existir independentemente da turma e do cliente para serem reutilizados com controle de versão e atribuição contextual.

### ENG-004 — Progresso auditável

Conclusões, avaliações e certificados precisam possuir histórico suficiente para explicar o estado exibido.

### ENG-005 — Evolução para integrações

O sistema deve permitir futura integração com software corporativo sem acoplar o domínio de aprendizagem a detalhes internos do software corporativo no Beta.

### ENG-006 — Deploy independente de web e API

Frontend e backend devem poder evoluir e ser implantados separadamente quando necessário.

### ENG-007 — Experiência responsiva

Administração prioriza desktop/tablet; aluno deve conseguir consumir a trilha em mobile web.

### ENG-008 — Segurança por contexto autenticado

Tenant e permissões devem derivar de identidade autenticada e vínculos persistidos, não de campos confiados ao cliente.

### ENG-009 — Crescimento inicial moderado

Beta esperado abaixo de 500 usuários, mas a modelagem não deve depender de um único cliente ou turma.

## 2. Alternativas arquiteturais consideradas

### Microsserviços

**Rejeitado no Beta.** A escala e o tamanho da equipe não justificam custo operacional, contratos distribuídos e observabilidade adicional.

### Aplicação monolítica única sem fronteiras

**Rejeitada.** Seria simples inicialmente, mas aumentaria risco de misturar conteúdo, tenant, aprendizagem e infraestrutura.

### Monólito modular com web e API separadas

**Escolhida.** Mantém operação simples, permite limites claros entre componentes do domínio e preserva deploy independente do frontend e backend.

Essa decisão é arquitetural. A linguagem, os runtimes e os frameworks concretos serão escolhidos depois no documento de tecnologias.

## 3. Estratégia de repositório

**Monorepo.**

Motivos:

- web e API compartilham contratos;
- regras de domínio e contratos precisam permanecer consistentes;
- um único CI pode validar limites entre componentes e contratos;
- equipe pequena se beneficia de mudanças atômicas;
- deploy continua podendo ser independente por aplicação.

Estrutura lógica inicial:

```text
/apps
  /web
  /api
/packages
  /domain
  /contracts
  /design-tokens
  /config
/infra
/tooling
/docs
```

Pastas específicas de fornecedor não são decisão deste documento. Se a infraestrutura aprovada exigir organização adicional, ela deve respeitar esses limites entre componentes e ser reconciliada sem transformar fornecedor em dependência do domínio.

A estrutura física final pode ser refinada na Fundação sem alterar silenciosamente o modelo arquitetural.

## 4. Módulos de domínio

### Identity & Access

Autenticação, memberships, roles e permissões.

### Tenancy

Empresas/clientes e vínculo de usuários.

### Catalog

Cursos, módulos, aulas e materiais.

### Learning Paths

Trilhas, critérios de atribuição e versão aplicável.

### Cohorts

Turmas, instrutores, participantes e datas.

### Enrollment & Progress

Matrículas, progresso, retomada e conclusão.

### Assessments

Quizzes, tentativas, regras de aprovação e tarefas práticas.

### Certification

Elegibilidade, emissão e registro de certificados.

### Notifications

Convites e mensagens transacionais essenciais.

## 5. Fronteiras de dependência

Controladores recebem a requisição e chamam serviços de aplicação. Regras de domínio não importam infraestrutura. Contratos de acesso a serviços externos são implementados por adaptadores; a composição da aplicação conecta essas partes.

`packages/domain` não deve importar framework web, SDK de banco, SDK de autenticação ou fornecedor de e-mail.

`apps/web` não acessa credenciais administrativas nem superfícies privadas por mecanismo privilegiado.

A API resolve autorização usando identidade autenticada e memberships persistidos.

## 6. API

Estilo inicial: REST JSON com contratos explícitos e versionados por código quando necessário.

Regras:

- endpoints de tenant validam contexto autenticado;
- paginação em coleções potencialmente grandes;
- validação de entrada na borda;
- erros previsíveis possuem códigos estáveis;
- idempotência para operações em que retry possa duplicar efeito, como convite ou emissão de certificado.

O framework HTTP concreto pertence ao documento de tecnologias.

## 7. Dados

A arquitetura exige **persistência relacional** para o núcleo transacional do produto.

Motivos:

- relações fortes entre organização, membership, turma, matrícula e progresso;
- constraints de integridade;
- transações para operações críticas;
- consultas auditáveis e paginação previsível;
- índices coerentes com isolamento por tenant.

Entidades principais esperadas:

```text
users
organizations
organization_memberships
courses
course_modules
lessons
learning_paths
learning_path_items
organization_modules
cohorts
cohort_members
course_enrollments
lesson_progress
assessments
assessment_attempts
practical_assignments
assignment_submissions
certificates
```

A tecnologia relacional concreta, driver/query layer e mecanismo de migrations são decisões do documento de tecnologias. O fornecedor é decisão de Infraestrutura.

A nomenclatura final deve seguir o Documento 06 e o modelo de dados executável.

## 8. Consistência e auditoria

- progresso de aula deve ser idempotente;
- certificado só é emitido após critérios oficiais satisfeitos;
- mudanças críticas de permissões e validações manuais precisam de trilha de auditoria mínima;
- alterações de schema são feitas por migrations versionadas.

## 9. Segurança

Limite de confiança simplificada:

**Passos ilustrativos:**

1. Browser.
2. depois  user session.
3. Web/API pública.
4. depois  authorized service identity.
5. Database / private services.

Regras:

- secrets apenas no servidor;
- autorização não depende apenas da UI;
- acesso a tenant é verificado no backend e, quando aplicável, reforçado na camada de dados;
- least privilege em serviços;
- arquivos privados usam URLs assinadas ou mecanismo equivalente quando necessário;
- logs evitam dados pessoais desnecessários.

## 10. Frontend

- composição por feature/domínio, não por pasta genérica de componentes;
- limites explícitos entre servidor e cliente se a tecnologia escolhida possuir essa distinção;
- estado global apenas quando houver necessidade real;
- cache e invalidação seguem semântica de dados;
- componentes visuais seguem Documento 04 e Princípios.

O framework de frontend, router, mecanismo de server state e bibliotecas concretas pertencem ao documento de tecnologias.

## 11. Decisões verificáveis

**Passos ilustrativos:**

1. Decisão: packages/domain não depende de frameworks.
2. —  verificação de dependências.
3. Decisão: tenant vem do contexto autorizado.
4. —  testes negativos de acesso cross-tenant.
5. Decisão: cliente não possui segredo administrativo.
6. —  secret scan + check de env pública.
7. Decisão: bugs de autorização não regressam.
8. —  testes de integração cross-tenant.

## 12. Decisões iniciais da narrativa

### ADR-001 — Monorepo

**Aceita para explorar o planejamento na narrativa; adoção real pendente.** Compartilhamento de contratos e equipe pequena justificam um único repositório.

### ADR-002 — Monólito modular

**Aceita para explorar o planejamento na narrativa; adoção real pendente.** Menor custo operacional com limites entre componentes preservados.

### ADR-003 — API separada do frontend

**Aceita para explorar o planejamento na narrativa; adoção real pendente.** Permite deploy independente e prepara integrações futuras sem adotar polyrepo.

### ADR-004 — Sem integração automática no Beta

**Aceita para explorar o planejamento na narrativa; adoção real pendente.** O domínio de aprendizagem deve estabilizar antes de automatizar validação externa.

## 13. Saída para o documento de tecnologias

A arquitetura produz restrições para seleção tecnológica, sem escolher o conjunto de tecnologias por preferência.

```text
TL-NEED-001 — Web e API devem compartilhar contratos tipados sem acoplar o domínio a framework.
TL-NEED-002 — packages/domain precisa permanecer executável/testável sem UI, HTTP, banco ou SDK de fornecedor.
TL-NEED-003 — web e API precisam de build e deploy independentes dentro do mesmo monorepo.
TL-NEED-004 — entradas externas precisam de validação durante a execução além de tipos estáticos.
TL-NEED-005 — a persistência principal deve ser relacional, com transações, constraints e índices.
TL-NEED-006 — o conjunto de tecnologias deve sustentar testes unitários, integração, E2E e verificações de dependências automatizados.
TL-NEED-007 — equipe pequena favorece ferramentas de desenvolvimento coesa e baixa quantidade de frameworks sobrepostos.
TL-NEED-008 — frontend responsivo não possui requisito de SSR no Beta; não adicionar SSR apenas por hábito.
TL-NEED-009 — API deve operar de forma stateless na superfície HTTP.
TL-NEED-010 — integrações futuras com software corporativo devem entrar por adapters/ports, sem contaminar domínio.
```

Essas necessidades devem ser consideradas em [tecnologias](tecnologias.md) antes da escolha de linguagens, runtimes, frameworks e bibliotecas.

## 14. Inventário de necessidades de infraestrutura

```text
INF-NEED-001 — repositório Git com CI
INF-NEED-002 — hosting web com HTTPS/CDN
INF-NEED-003 — runtime gerenciado compatível com o conjunto de tecnologias aprovado para API
INF-NEED-004 — banco relacional gerenciado
INF-NEED-005 — autenticação
INF-NEED-006 — storage privado para materiais quando necessário
INF-NEED-007 — envio de e-mail transacional
INF-NEED-008 — secrets por ambiente
INF-NEED-009 — logs e rastreamento de erros
INF-NEED-010 — staging compartilhável
INF-NEED-011 — backup/restore compatível com o estágio
```

Arquitetura define **o que tecnicamente precisamos e quais fronteiras devem existir**. A pessoa responsável pelas tecnologias define **com quais tecnologias essas decisões serão implementadas**. Infraestrutura define **onde o conjunto de tecnologias aprovado será executado**.

## Critério de qualidade

Outra equipe deve conseguir ler este documento e compreender:

- forças de engenharia;
- modelo arquitetural;
- estratégia de repositório;
- módulos;
- limites entre componentes;
- requisitos de dados;
- limites de confiança;
- critérios que o conjunto de tecnologias precisa satisfazer;
- necessidades de infraestrutura.

Ela não deve precisar inventar a arquitetura, mas também não deve encontrar framework, library ou fornecedor escolhido prematuramente por preferência.

## Comparação e limites da decisão

A [comparação ilustrativa](comparacao-e-decisao.md) registra alternativas, lacunas, consequências e condição de revisão. Não há protótipo ou medição de complexidade executados. As escolhas deste estudo não dispensam avaliação de solução existente, requisitos e capacidade da equipe real.
