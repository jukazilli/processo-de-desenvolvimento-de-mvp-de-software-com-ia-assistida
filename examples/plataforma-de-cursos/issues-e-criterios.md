---
document_id: DOC-08
title: Issues e critérios de aceite
status: fictional-example
version: 2.0.0
depends_on:
  - DOC-06
  - DOC-07
  - TECH-LEAD-VISION
  - Infraestrutura_e_Plano_de_Fundacao
---

# Issues e critérios de aceite

> **Estudo fictício, versão 2.0.** Requisitos, decisões, aprovações e cenários abaixo são ilustrativos. Nenhuma aplicação, pesquisa com usuários, contratação, implantação ou teste deste produto foi executado. Consulte o [índice e a autoridade de cada assunto](README.md).

## Como usar este catálogo didático

Este arquivo exemplifica o conteúdo de **29 Issues**, com IDs preservados para demonstrar rastreabilidade. Não é a fila de um projeto em execução; nenhum desses registros foi criado no GitHub. Não há números reais de Issues, PRs, commits do produto ou resultados de testes.

Ao adotar: adaptar os critérios ao produto, publicar cada atividade necessária como Issue e conferir paridade de ID, fonte, objetivo, aceite, dependências, risco e evidências. A partir daí, andamento, prioridade e ciclo vivem no GitHub. Não atualizar este catálogo como uma segunda fila. Requisitos duráveis ficam na fonte oficial indicada pelo projeto.

Uma Issue de agrupamento pode reunir Fundação ou uma jornada, com sub-Issues ou links para os itens. Projects é opcional. Status operacional, aprovação de decisão, estado da PR e evidência de implementação/liberação são dimensões distintas; ver [rastreabilidade](rastreabilidade.md).

### Exemplo preenchido de Issue: FND-001

- **Objetivo:** preparar apenas a estrutura do repositório para o primeiro incremento.
- **Fontes:** [arquitetura](arquitetura.md), DOC-07; decisão ilustrativa ADR-001/002/003.
- **Escopo:** pastas, regras de dependência e instruções de verificação; sem instalar bibliotecas ou criar serviços externos.
- **Aceite e evidência esperada:** critérios FND-001 abaixo; diff revisável e commit real quando executado.
- **Operação ilustrativa:** Pronto, se as entradas e autorizações estiverem suficientes no projeto adotante.
- **Aprovação:** proposta de arquitetura aprovada apenas dentro da narrativa; não é autorização para um projeto real.
- **Implementação e QA:** não iniciados; nenhum resultado executado.
- **PR e evidência:** ausentes; preencher com links reais na execução, sem inventar números.
- **Documentação afetada:** índice da arquitetura e instruções locais somente se o resultado os alterar.
- **Dependência:** decisões técnicas verificadas e autorização para esse recorte; não depende de criar nuvem.

Os critérios abaixo são expectativas, não resultados. Fundação existente e suficiente é conferida e reutilizada; não se recria tudo antes de corrigir um bug.

# Fundação

## FND-001 — Inicializar estrutura arquitetural do monorepo

**Origem:** DOC-07  
**Objetivo:** criar o esqueleto físico definido pela arquitetura sem antecipar a instalação da ferramentas de desenvolvimento, que pertence ao item seguinte.

### Critérios de aceite

- `apps/web` e `apps/api` existem como superfícies separadas;
- `packages/domain`, `packages/contracts`, `packages/design-tokens` e `packages/config` são criados quando previstos pela estrutura aprovada;
- `/infra`, `/tooling` e `/docs` possuem lugar explícito quando aplicáveis;
- nenhum diretório específico do fornecedor é introduzido como dependência estrutural do domínio;
- limites entre componentes e responsabilidade lógico do Documento 07 podem ser reconhecidos pela árvore;
- nenhumo conjunto de tecnologias alternativa é escolhida durante este item.

### Testes/evidência

- inspeção/diff da árvore;
- revisão de conformidade com o Documento 07;
- commit pequeno contendo apenas o esqueleto arquitetural.

**Dependências:** nenhuma.

---

## FND-002 — Fixar conjunto de tecnologias, workspace e ferramentas de desenvolvimento

**Origem:** DOC-06, TECH-LEAD-VISION  
**Objetivo:** tornar o ambiente reproduzível e materializar as decisões tecnológicas aprovadas sobre a estrutura criada em FND-001.

### Critérios

- Node.js (versão a validar) fixado no mecanismo aprovado;
- pnpm fixado e workspace configurado;
- TypeScript (versão a validar) configurado em strict;
- React (versão a validar)/Vite (versão a validar) preparados em `apps/web`;
- Fastify (versão a validar) preparado em `apps/api`;
- packages compartilhados entram no workspace sem violar limites entre componentes;
- lockfile versionado;
- ESLint/TypeScript ESLint e Prettier configurados;
- clean install funciona;
- build mínimo das superfícies iniciais funciona;
- nenhuma biblioteca concorrente é adicionada para responsabilidade já registrada na fonte oficial.

**Dependência:** FND-001.

---

## FND-003 — Criar verificações de qualidade locais

**Origem:** DOC-06, TECH-LEAD-VISION  

### Critérios

Comandos equivalentes a:

```text
format:check
lint
typecheck
test
build
check:boundaries
```

- Vitest disponível para testes rápidos;
- Playwright preparado quando o primeiro smoke/E2E for elegível;
- gates falham de forma legível.

**Dependência:** FND-002.

---

## FND-004 — Configurar CI

**Origem:** DOC-06, TECH-LEAD-VISION, Infraestrutura  

### Critérios

- GitHub Actions executa os gates definidos;
- pull/commit candidato executa validações necessárias;
- falha bloqueia promoção;
- pipeline não imprime secrets;
- cache, se usado, não compromete reprodutibilidade.

**Dependência:** FND-003.

---

## FND-005 — Criar banco/auth de staging

**Origem:** DOC-07, TECH-LEAD-VISION, Infraestrutura  

### Critérios

- projeto Supabase de staging aprovado pelo humano;
- PostgreSQL/Auth disponíveis;
- região e identificação do ambiente registradas;
- credenciais não transitam pelo chat;
- conexão da API pelo mecanismo aprovado validada;
- credencial administrativa não chega ao frontend.

**Dependência:** FND-004.

---

## FND-006 — Migrations baseline de identidade e tenant

**Origem:** DOC-06, DOC-07, TECH-LEAD-VISION, Infraestrutura  

### Critérios

- migrations SQL versionadas;
- mecanismo de aplicação compatível com Supabase e CI;
- organizações e memberships modeladas;
- constraints mínimas;
- política de autorização inicial;
- teste negativo cross-tenant;
- migration state reproduzível a partir do Git.

**Dependência:** FND-005.

---

## FND-007 — Publicar web em staging

**Origem:** TECH-LEAD-VISION, Infraestrutura  

### Critérios

- React/Vite build publicado no Cloudflare Pages;
- HTTPS;
- health/smoke page acessível;
- variáveis públicas revisadas;
- nenhum secret presente no bundle;
- deploy identificável por commit/SHA quando possível.

**Dependência:** FND-004.

---

## FND-008 — Publicar API em staging

**Origem:** DOC-07, TECH-LEAD-VISION, Infraestrutura  

### Critérios

- Node.js/Fastify (versões a validar) publicado no Google Cloud Run;
- health endpoint;
- serviço stateless;
- conexão autorizada com PostgreSQL;
- secrets apenas no runtime;
- logs estruturados mínimos;
- CORS/origins conforme ambiente;
- recurso potencialmente cobrável só é criado após aprovação humana.

**Dependências:** FND-005, FND-006.

---

## FND-009 — Configurar e-mail transacional de teste

**Origem:** DOC-07, TECH-LEAD-VISION, Infraestrutura  

### Critérios

- Resend aprovado/configurado;
- domínio/remetente de teste validado;
- SDK restrito ao adapter de Notifications;
- secret armazenado fora do código;
- mensagem de teste enviada sem expor credencial.

**Dependência:** FND-004.

---

## FND-010 — Smoke test da Fundação

**Origem:** DOC-06, DOC-07, TECH-LEAD-VISION, Infraestrutura  

### Critérios

- web acessível;
- API saudável;
- banco responde;
- migration state válido;
- auth baseline funciona;
- CI aprovado;
- teste cross-tenant negativo passa;
- conjunto de tecnologias instalada corresponde ao documento de tecnologias;
- fornecedores implantados correspondem à Infraestrutura aprovada;
- logs mínimos estão acessíveis sem exposição de dados sensíveis.

**Dependências:** FND-006, FND-007, FND-008, FND-009.

### Evidência

CI + staging + registro de execução.

---

# Identidade e Tenancy

## AUTH-001 — Primeiro acesso por convite

**Origem:** DOC-02, DOC-05  
**Objetivo:** permitir que aluno aceite convite e acesse o contexto correto.

### Critérios

- convite associa e-mail à empresa/turma prevista;
- usuário autenticado não escolhe tenant arbitrário;
- convite expirado possui tratamento claro;
- usuário existente pode aceitar novo vínculo permitido.

### Testes

- sucesso;
- convite inválido;
- convite expirado;
- tentativa de usar convite de outro destinatário quando aplicável.

**Dependência:** FND-010.

---

## TEN-001 — Criar empresa

### Critérios

- somente papel autorizado da consultoria cria;
- nome obrigatório;
- duplicidade provável sinalizada;
- empresa nasce sem expor dados de outras organizações.

**Dependência:** AUTH-001.

---

## TEN-002 — Configurar módulos do software corporativo contratados

### Critérios

- módulos podem ser associados/removidos por usuário autorizado;
- histórico de mudança crítica é auditável;
- configuração alimenta atribuição de trilhas.

**Dependência:** TEN-001.

---

## TEN-003 — Gestor vê somente sua empresa

### Critérios

- acesso cross-tenant é negado no backend;
- UI não apresenta seletor de outras empresas;
- testes negativos cobrem leitura e mutação.

**Dependência:** AUTH-001.

---

# Conteúdo e Trilhas

## CNT-001 — Criar curso reutilizável

### Critérios

- título, descrição e status;
- curso não pertence a uma turma específica;
- edição respeita permissões;
- exclusão não é ação primária.

**Dependência:** AUTH-001.

---

## CNT-002 — Organizar módulos e aulas

### Critérios

- curso possui módulos ordenados;
- módulo possui aulas ordenadas;
- aula suporta conteúdo previsto pelo Beta;
- ordem é persistida de forma determinística.

**Dependência:** CNT-001.

---

## CNT-003 — Adicionar materiais por link/PDF

### Critérios

- validação de tipo/tamanho quando upload existir;
- arquivos privados não se tornam públicos por padrão;
- link externo é validado como URL.

**Dependência:** CNT-002.

---

## TRL-001 — Criar trilha

### Critérios

- trilha possui itens ordenados;
- pode reutilizar cursos;
- critérios de público são legíveis;
- publicação exige conteúdo válido.

**Dependência:** CNT-001.

---

## TRL-002 — Sugerir trilha compatível com empresa/perfil

### Critérios

- critérios usados são visíveis ao consultor;
- sugestão não é aplicada silenciosamente;
- módulos contratados incompatíveis são sinalizados.

**Dependências:** TRL-001, TEN-002.

---

# Turmas e Matrículas

## CLS-001 — Criar turma

### Critérios

- vinculada a uma empresa;
- instrutor e período opcionais/conforme regra;
- turma não duplica conteúdo-base;
- só usuários autorizados criam.

**Dependência:** TEN-001.

---

## CLS-002 — Matricular usuários e atribuir trilha

### Critérios

- usuário deve pertencer à empresa correta;
- trilha é revisada antes da confirmação;
- operação repetida não duplica matrícula.

**Dependências:** CLS-001, TRL-002.

---

# Experiência de Aprendizagem

## LRN-001 — Exibir Minha trilha

### Critérios

- aluno vê trilha atual;
- próxima atividade fica evidente;
- concluídos e pendentes são distinguíveis sem depender só de cor;
- nenhum dado de outro tenant aparece.

**Dependência:** CLS-002.

---

## LRN-002 — Registrar conclusão de aula

### Critérios

- conclusão é idempotente;
- data/usuário são registrados;
- progresso recalculado de forma consistente;
- próxima atividade é apresentada.

**Dependência:** LRN-001.

---

## ASM-001 — Realizar quiz

### Critérios

- tentativa persiste respostas conforme política;
- envio calcula resultado;
- regra de aprovação é explícita;
- falha de rede não deve apagar respostas quando evitável.

**Dependência:** LRN-001.

---

## ASM-002 — Registrar tarefa prática

### Critérios

- instrução é clara;
- aluno registra submissão permitida;
- status pode exigir validação manual;
- Beta não consulta software corporativo automaticamente.

**Dependência:** LRN-001.

---

## ASM-003 — Validar tarefa prática

### Critérios

- somente instrutor/consultoria autorizada valida;
- aprovação/reprovação registra ator e data;
- devolução pode conter orientação;
- aluno é informado do novo estado.

**Dependência:** ASM-002.

---

# Acompanhamento e Certificação

## OBS-001 — Consultor acompanha turma

### Critérios

- identifica não iniciados, em andamento, bloqueados e concluídos;
- tarefas aguardando validação recebem prioridade;
- filtros não cruzam tenants;
- dados agregados correspondem ao estado individual.

**Dependências:** LRN-002, ASM-001.

---

## OBS-002 — Gestor acompanha equipe

### Critérios

- somente sua empresa;
- visualização por turma/trilha;
- sem acesso a autoria de conteúdo;
- permissões de convite respeitam configuração da consultoria.

**Dependências:** TEN-003, LRN-002.

---

## CERT-001 — Emitir certificado elegível

### Critérios

- sistema verifica todos os requisitos da trilha;
- emissão repetida não duplica certificado;
- registro possui identificador estável;
- aluno consegue acessar comprovante.

**Dependências:** LRN-002, ASM-001, ASM-003 quando aplicável.

---

# Seleção do próximo incremento no GitHub

Para um projeto novo, preparar o menor caminho verificável: acesso autorizado do aluno a uma trilha e sua próxima atividade, incluindo apenas a fundação necessária. Manter o restante no backlog e definir dependências explícitas. Não chamar a divisão por área de incremento entregue: um incremento precisa de resultado verificável em seu escopo.

Para um produto existente, conferir quais critérios já possuem evidência e abrir somente trabalho faltante. O próximo item é selecionado nas Issues prontas, por prioridade e dependências. Os IDs FND-001 a FND-010 não obrigam executar novamente uma base existente.

Ciclos com prazo ou fluxo contínuo são opções da equipe. Nenhum cronograma, estimativa ou liberação foi comprovado por este exemplo.
