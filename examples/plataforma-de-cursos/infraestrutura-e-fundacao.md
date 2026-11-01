---
document_id: Infraestrutura_e_Plano_de_Fundacao
title: Infraestrutura e Plano de Fundação — plataforma de cursos
status: fictional-example
version: 2.0.0
depends_on:
  - DOC-06
  - DOC-07
  - TECH-LEAD-VISION
---

# Infraestrutura e Plano de Fundação — plataforma de cursos

> **Estudo fictício, versão 2.0.** Requisitos, decisões, aprovações e cenários abaixo são ilustrativos. Nenhuma aplicação, pesquisa com usuários, contratação, implantação ou teste deste produto foi executado. Consulte o [índice e a autoridade de cada assunto](README.md).

## 1. Respostas simuladas para dimensionamento

- produto pode evoluir para oferta comercial;
- começar com custo zero quando for seguro e coerente;
- staging em nuvem desde o início;
- menos de 500 usuários no Beta;
- dados pessoais básicos e dados de aprendizagem;
- preferência por serviços gerenciados;
- sem equipe DevOps dedicada;
- qualquer recurso pago exige aprovação humana explícita.

## 2. Tecnologias recebidas do planejamento técnico

A infraestrutura não escolhe novamente o conjunto de tecnologias.

**Passos ilustrativos:**

1. Web         —  React (versão a validar) + Vite (versão a validar) + React Router (versão a validar).
2. API         —  Node.js (versão a validar) + Fastify (versão a validar).
3. Contratos   —  Zod (versão a validar).
4. Banco       —  PostgreSQL.
5. DB driver   —  pg em adapters.
6. Tests       —  Vitest + Testing Library + Playwright.
7. Workspace   —  pnpm workspaces.

O objetivo desta etapa é escolher **fornecedores e ambientes capazes de executar esse conjunto de tecnologias**.

## 3. Estratégia geral

**Passos ilustrativos:**

1. GitHub.
2. GitHub Actions.
3. Cloudflare Pages — web SPA.
4. Google Cloud Run — API Node/Fastify.
5. Supabase — PostgreSQL/Auth/Storage.
6. Resend — e-mail transacional.
7. staging validado.

Essa composição foi escolhida para manter baixa complexidade operacional e limites entre componentes compatíveis com o Documento 07.

## 4. Pesquisa de fornecedores ainda necessária

Os nomes abaixo compõem uma simulação de contratação, não uma oferta atual conferida. Não foram consultados preços, regiões, cotas ou elegibilidade da conta deste produto. **Custo de todos os serviços: desconhecido — revalidar.** Gratuidade e compatibilidade não podem ser presumidas pelo nome do plano.

| Responsabilidade | Candidato ilustrativo | Confirmar na adoção real |
| --- | --- | --- |
| Banco, autenticação e arquivos | Supabase | Versões, região, isolamento, backups, limites e custo total |
| Hospedagem da web | Cloudflare Pages | Build, domínio, limites, uso comercial e custos associados |
| Execução da API | Google Cloud Run | Runtime, região, conectividade, conta de cobrança e excedentes |
| E-mail | Resend | Remetente, cotas, entrega, privacidade e preço |
| Repositório e CI | GitHub e Actions | Plano, visibilidade, minutos, armazenamento e proteção aplicável |

Consultar a documentação oficial do serviço escolhido, datar o registro e comparar alternativa existente ou gerenciada. Aplicar o [modelo de comparação](comparacao-e-decisao.md). Nenhum recurso pode ser criado a partir desta tabela; contratação depende da decisão e autorização do projeto real.

## 5. Decisões de fornecedor

### Repositório e CI

- GitHub;
- monorepo conforme Documento 07;
- GitHub Actions para CI;
- branch `main` protegida quando o plano/ambiente permitir;
- PR como caminho padrão de promoção depois da Fundação.

### Web

- Cloudflare Pages;
- deploy do build estático produzido por Vite;
- HTTPS;
- domínio técnico de staging;
- somente variáveis destinadas ao cliente podem entrar no bundle;
- nenhum secret administrativo na web.

### API

- Google Cloud Run;
- Node.js (versão a validar) dentro do runtime/container aprovado;
- Fastify (versão a validar);
- serviço stateless;
- `min instances = 0` no estágio inicial salvo necessidade medida;
- health endpoint;
- secrets somente no ambiente do serviço;
- logs estruturados;
- região a escolher após conferir disponibilidade, dados, latência e custo; sem região homologada neste exemplo.

A escolha do fornecedor acontece **antes do FND**. O FND valida e cria o recurso aprovado; ele não abre novamente uma disputa entre Workers, Cloud Run ou outros fornecedores sem uma restrição nova.

### Banco/Auth/Storage

- Supabase;
- PostgreSQL como banco relacional proposto no documento de tecnologias;
- Auth gerenciado;
- Storage privado para materiais não públicos;
- migrations SQL versionadas no repo;
- Supabase CLI pode executar as migrations aprovadas na Fundação sem transformar o domínio em dependente do fornecedor;
- `pg` na API para acesso relacional via conexão/pooler aprovado;
- `@supabase/supabase-js` somente nos adapters de Auth/Storage e, no cliente, apenas com credencial pública apropriada;
- service role ou segredo equivalente nunca entra no frontend.

### E-mail

- Resend;
- SDK do fornecedor restrito ao adapter de Notifications;
- domínio de envio validado;
- secret somente no runtime seguro.

### Observabilidade

Para o FND:

- logs estruturados da API no Cloud Run;
- logs de deploy/execução do CI;
- captura de falhas críticas de web/API por mecanismo aprovado durante a Fundação;
- alertas mínimos para falha de deploy e erro crítico;
- nenhum payload sensível em logs.

Se uma ferramenta externa adicional de error tracking for necessária e puder gerar custo, ela exige nova decisão explícita; não é instalada silenciosamente.

## 6. Contratos de compatibilidade a verificar

| Relação proposta | Evidência necessária | Situação real deste exemplo |
| --- | --- | --- |
| Web e hospedagem | Build reproduzível, rotas, variáveis públicas e smoke do candidato | Não executado |
| API e runtime | Versão suportada, inicialização, health check e recursos | Não executado |
| API e banco | Conexão, pool, transação, migração e autorização negativa | Não executado |
| Autenticação e arquivos | Sessão, permissão, credenciais e isolamento | Não executado |
| CI e ambiente de teste | Execução ligada ao commit, resultado e logs seguros | Não executado |

Se a execução real contradisser a proposta, registrar impedimento na Issue e revisar a decisão responsável. A IA não troca tecnologia ou fornecedor silenciosamente.

## 7. Ambientes

### Local

Desenvolvimento e testes rápidos, usando serviços locais/emulados quando isso não cria comportamento diferente do contrato real.

### Staging

Obrigatório desde a Fundação, porque será usado pela consultoria e por usuários piloto.

- web: Cloudflare Pages staging;
- API: Cloud Run staging;
- banco/auth/storage: projeto Supabase de staging;
- e-mail: configuração de teste do Resend.

### Production

Não será criado automaticamente no primeiro setup.

Staging precisa produzir evidências antes de qualquer promoção. A criação de produção exige revisão de custo, backup/restore, disponibilidade, privacidade, domínio e observabilidade.

## 8. Segurança de credenciais

Nenhuma senha, service role key, private key, refresh token ou API secret deve ser enviada pelo chat.

Fluxo para setup humano-assistido:

**Passos ilustrativos:**

1. agente abre/prepara painel.
2. humano autentica diretamente.
3. MFA/CAPTCHA ficam com o humano.
4. agente continua na sessão autorizada.

Preferência de automação:

**Passos ilustrativos:**

1. API/CLI/IaC.
2. OAuth/conector.
3. Playwright em sessão autorizada.
4. runbook manual seguro.

## 9. Itens de Fundação derivados

Os IDs abaixo são mantidos consistentes com o Documento 08 deste exemplo.

```text
FND-001 — inicializar monorepo conforme DOC-07
FND-002 — fixar conjunto de tecnologias/ferramentas de desenvolvimento conforme Escolhas de tecnologias
FND-003 — configurar verificações de qualidade locais
FND-004 — configurar CI
FND-005 — criar banco/auth de staging
FND-006 — criar migrations baseline e autorização de tenant
FND-007 — publicar web em staging
FND-008 — publicar API em staging com secrets/logs mínimos
FND-009 — configurar e-mail transacional de teste
FND-010 — executar smoke test consolidado da Fundação
```

Secrets e observabilidade mínima são critérios transversais dos itens que criam os respectivos runtimes, não IDs concorrentes com significados diferentes.

## 10. Verificação de custo

Antes de criar qualquer recurso:

```text
FREE / INCLUÍDO
POTENCIALMENTE COBRÁVEL
COBRÁVEL
DESCONHECIDO — REVALIDAR
```

Qualquer estado diferente de `FREE / INCLUÍDO` exige explicação e aprovação humana antes da ação.

Neste exemplo, todos os custos continuam desconhecidos. Na adoção real, classificar cada recurso e seus excedentes antes da ação; não presumir autorização financeira pela escolha ilustrativa de um fornecedor.

## 11. Fundação pronta

A Fundação não está pronta apenas porque contas existem.

```text
repo conforme arquitetura
+
conjunto de tecnologias/ferramentas de desenvolvimento conforme Tech Lead
+
CI executando
+
banco e migrations funcionando
+
auth/tenant baseline validado
+
web e API em staging nos fornecedores aprovados
+
secrets fora do código e do chat
+
logs mínimos
+
smoke tests aprovados
+
rastreabilidade reconciliada
=
FND_READY
```

Qualquer troca de fornecedor ou tecnologia durante a Fundação precisa voltar para a camada documental responsável antes de se tornar novo padrão.
