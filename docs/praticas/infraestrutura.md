# Planejamento e preparação de infraestrutura

Este capítulo preserva as regras técnicas detalhadas do processo. As [etapas numeradas](../../README.md) orientam quando aplicá-las; consulte o [glossário](../glossario.md) para os termos técnicos. As escolhas concretas dependem do projeto.

## Pergunta central

> **Onde e com quais serviços a arquitetura e a stack aprovadas serão executadas, considerando crescimento, custo, segurança e operação desejada pelo humano?**

## Objetivo

Transformar o inventário de necessidades produzido pelo registro de qualidade e arquitetura e as decisões da escolha das tecnologias em uma infraestrutura pesquisada, compatível, aprovada e executável pelos itens FND do backlog.

A separação é:

```text
ENGENHARIA
"Quais propriedades técnicas precisamos suportar?"
        ↓
ARQUITETURA
"Como o software será estruturado para suportá-las?"
        ↓
ESCOLHA DAS TECNOLOGIAS
"Com quais tecnologias implementaremos essa arquitetura?"
        ↓
INFRAESTRUTURA
"Onde e com quais serviços essa stack será executada?"
        ↓
FUNDAÇÃO
"Crie e valide o ambiente necessário."
```

## A IA deve entrevistar o humano

Infraestrutura não deve ser escolhida somente por preferência técnica do agente.

A entrevista deve ser curta e adaptada ao projeto.

### Natureza do produto

Perguntar, conforme aplicável:

- É protótipo, ferramenta interna, projeto pessoal ou produto comercial?
- Existe expectativa de muitos usuários no futuro?
- Há previsão de crescimento rápido?
- Haverá usuários externos desde o início?
- Existem dados pessoais, financeiros, médicos, profissionais ou outros dados sensíveis?
- Qual disponibilidade é esperada?

### Estratégia de custo

- Quer começar com custo zero quando possível?
- Aceita pagar desde a Fundação?
- Existe orçamento mensal aproximado?
- Prefere custo mínimo agora ou menos migração futura?
- Free tiers com limites são aceitáveis?
- Recursos pagos exigem aprovação individual?

**Regra:** contratação, upgrade de plano ou criação de recurso que possa gerar cobrança exige aprovação humana explícita.

### Local versus cloud

- Prefere começar somente em `localhost`?
- Quer staging em nuvem desde o início?
- Precisa compartilhar o ambiente com outras pessoas?
- A máquina local pode fazer parte da operação?

A IA deve explicar consequências.

```text
localhost
+ custo potencialmente menor
+ simplicidade inicial
- difícil compartilhar
- depende da máquina do usuário
- não comprova comportamento real de cloud

cloud / staging
+ ambiente reproduzível
+ acesso remoto
+ valida integrações reais
+ permite CI/CD e evidência operacional
- pode exigir contas, setup e eventualmente custo
```

### Operação

- Prefere serviços gerenciados?
- Existe equipe de DevOps?
- Quer reduzir o número de provedores?
- Deseja evitar lock-in mesmo com maior complexidade?
- Já possui provedores aprovados?

### Capacidades

Perguntar quando relevante sobre:

- realtime;
- offline;
- arquivos/mídia;
- e-mail/push/SMS/WhatsApp;
- workers;
- filas/eventos;
- scheduler;
- processamento pesado;
- IA;
- busca;
- região;
- backup/restore;
- logs/métricas/alertas.

## Pesquisa web atual é obrigatória

Preços, free tiers, quotas, regiões, planos, produtos e compatibilidades de runtime mudam.

Antes de recomendar infraestrutura para um novo projeto, a IA deve pesquisar informações atuais, preferencialmente em fontes oficiais:

1. documentação oficial;
2. pricing oficial;
3. quotas e limits;
4. regiões;
5. runtimes e versões suportadas;
6. compatibilidade com frameworks/tecnologias aprovados;
7. segurança/compliance quando relevante;
8. SLA/status quando necessário.

A pesquisa deve responder:

- o serviço continua disponível?
- suporta a stack aprovada?
- existe free tier ou crédito inicial?
- quais limites afetam o projeto?
- quando começa a cobrança?
- a região necessária existe?
- existe alternativa mais simples?
- possui API/CLI/IaC?
- existem restrições relevantes para produção?

Nunca aprovar e registrar simplesmente:

```text
"Esse serviço é grátis."
```

Preferir:

```text
"Na pesquisa realizada em AAAA-MM-DD, o provedor oferecia camada gratuita
com os seguintes limites relevantes [...]. Revalidar antes da contratação."
```

## A IA deve comparar alternativas

Quando houver mais de uma opção razoável, apresentar de duas a quatro alternativas.

| Critério | Opção A | Opção B | Opção C |
| --- | --- | --- | --- |
| compatibilidade com a stack | | | |
| custo inicial | | | |
| camada gratuita | | | |
| facilidade de setup | | | |
| operação | | | |
| escala | | | |
| automação | | | |
| lock-in | | | |
| regiões | | | |
| adequação ao projeto | | | |

A recomendação deve explicar por que a alternativa escolhida combina com as respostas do humano, com as necessidades arquiteturais e com a stack aprovada.

## Perfil de infraestrutura de referência

A metodologia pode sugerir como ponto de partida, quando compatível e após revalidação atual:

- **GitHub** — repositório, pull requests e CI;
- **Supabase** — PostgreSQL gerenciado, autenticação e recursos de backend quando adequados;
- **Cloudflare Pages ou hosting web gerenciado equivalente** — frontend quando compatível;
- **Google Cloud Run ou runtime serverless/containerizado equivalente** — APIs e workers quando necessários;
- **GitHub Actions** — verificações obrigatórias e automação de entrega;
- **Terraform ou IaC equivalente** — quando a complexidade justificar;
- **Playwright** — E2E, validação visual e setup humano-assistido quando apropriado.

Esse perfil é referência, não obrigação.

Nunca escolher um provedor apenas porque ele foi usado em outro projeto. A infraestrutura também não pode reabrir silenciosamente a stack definida pelo responsável técnico.

## O plano deve mapear a infraestrutura completa

Conforme aplicável, documentar:

### Repositório e entrega

- provedor Git;
- branches;
- proteções;
- CI;
- estratégia de promoção.

A **estrutura lógica do repositório** já foi decidida no registro de qualidade e arquitetura. A **toolchain e a stack** foram definidas na escolha das tecnologias. Aqui são definidos os serviços operacionais ligados a elas.

### Ambientes

- local;
- development remoto, se existir;
- staging;
- production;
- segregação entre ambientes.

### Frontend

- provedor;
- compatibilidade com framework/runtime aprovado;
- região quando aplicável;
- build;
- domínio;
- variáveis públicas;
- CDN/cache.

### Backend/API

- runtime compatível com a stack aprovada;
- provedor;
- escalabilidade;
- exposição pública/privada;
- health checks;
- secrets;
- logs.

### Banco de dados

- tecnologia definida ou restrita pela arquitetura/responsável técnico quando aplicável;
- provedor;
- instância/projeto;
- ambientes;
- migrations;
- backup;
- restore;
- região;
- modelo de acesso;
- política de credenciais.

### Autenticação

- provedor;
- métodos habilitados;
- compatibilidade com o modelo arquitetural e SDKs aprovados quando aplicável;
- SMTP/e-mail quando necessário;
- redirect URLs;
- MFA quando aplicável;
- separação de chaves públicas e privadas.

### Storage e mídia

- provedor;
- buckets;
- acesso público/privado;
- limites;
- retenção.

### Workers, jobs, filas e eventos

- necessidade;
- runtime compatível;
- scheduler;
- fila;
- retry;
- DLQ quando aplicável;
- idempotência.

### Observabilidade

- logs;
- métricas;
- erros;
- alertas;
- tracing quando necessário;
- integração compatível com a stack aprovada.

### Segurança

- secrets manager;
- IAM;
- least privilege;
- scanning;
- backups;
- exposição de serviços;
- segregação de ambiente.

### Custos

- recursos gratuitos;
- recursos potencialmente cobrados;
- gatilhos de upgrade;
- alertas/budget quando disponíveis;
- aprovações necessárias para escalar.

## O plano gera a Fundação — FND

Depois da aprovação da infraestrutura, o backlog em Issues da etapa 10 deve transformar o plano e as decisões tecnológicas em habilitadores FND.

Exemplo:

```text
FND-001 — Criar repositório e proteção básica
FND-002 — Fixar toolchain, versões e lockfile conforme escolha das tecnologias
FND-003 — Configurar CI inicial
FND-004 — Criar projeto de banco de staging
FND-005 — Configurar migrations
FND-006 — Criar aplicação web de staging
FND-007 — Criar API de staging
FND-008 — Configurar secrets
FND-009 — Configurar autenticação mínima
FND-010 — Criar observabilidade mínima
FND-011 — Validar backup/restore aplicável
FND-012 — Smoke test da fundação
```

Os IDs reais devem ser derivados das necessidades do projeto.

FND não termina quando as contas foram criadas. Termina quando existe evidência de que o ambiente está utilizável.

```text
repositório criado
+
toolchain conforme responsável técnico
+
CI executando
+
banco acessível pelo mecanismo aprovado
+
migrations funcionando
+
serviços implantados
+
segredos fora do código
+
staging acessível
+
smoke tests aprovados
+
rastreabilidade reconciliada
=
FUNDAÇÃO OPERACIONAL
```

## Automação do setup

A prioridade deve ser:

```text
API / CLI / IaC oficial
        ↓ se insuficiente
conector autorizado / OAuth
        ↓ se insuficiente
Playwright em sessão autenticada pelo humano
        ↓ se bloqueado
passo a passo manual seguro
```

Playwright é útil para:

- abrir o painel correto;
- navegar depois de autenticação humana;
- configurar opções não expostas por API;
- validar visualmente o ambiente;
- executar smoke/E2E;
- reduzir trabalho manual repetitivo.

Não deve ser usado para contornar controles de segurança.

## Login e credenciais — humano no circuito

Se uma etapa exigir login, MFA, CAPTCHA, aceite legal, compra, cartão ou visualização única de segredo, a automação deve devolver essa ação ao humano.

Fluxo:

```text
Agente abre/prepara a página
        ↓
Humano faz login diretamente no provedor
        ↓
Humano conclui MFA/CAPTCHA/aceite quando necessário
        ↓
Agente continua na sessão já autorizada
```

O usuário não deve enviar pelo chat:

- senhas;
- service role keys;
- private keys;
- API secrets;
- refresh tokens;
- recovery codes;
- tokens permanentes;
- dados de cartão.

Quando um segredo precisar ser criado, preferir armazená-lo diretamente no secret manager, GitHub Secrets ou mecanismo equivalente, sem fazê-lo transitar pelo chat.

Se a IA não conseguir concluir uma etapa, deve fornecer um mini-runbook seguro dizendo:

- qual painel abrir;
- qual menu acessar;
- onde clicar;
- o que criar ou selecionar;
- qual valor não sensível preencher;
- o que **não** copiar para o chat;
- como confirmar que a etapa terminou;
- qual evidência segura permite continuar.

## Custos exigem aprovação explícita

Classificar ações de infraestrutura como:

```text
GRATUITA / FREE TIER
POTENCIALMENTE COBRÁVEL
COBRÁVEL
DESCONHECIDA — REVALIDAR
```

Se houver dúvida, tratar como potencialmente cobrável.

O agente não pode contratar, fazer upgrade ou criar recurso que possa gerar cobrança sem informar finalidade, modelo de cobrança conhecido e obter aprovação humana explícita.

[Voltar ao guia](../../README.md)
