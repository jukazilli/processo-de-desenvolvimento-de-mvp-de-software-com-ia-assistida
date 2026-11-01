# Engenharia e arquitetura

Este capítulo preserva as regras técnicas detalhadas do processo. As [etapas numeradas](../../README.md) orientam quando aplicá-las; consulte o [glossário](../../docs/glossario.md) para os termos técnicos. As escolhas concretas dependem do projeto.

## Pergunta central

> **Quais forças técnicas o produto precisa suportar e qual estrutura arquitetural consegue atendê-las com o menor conjunto de compromissos aceitáveis?**

## Objetivo

Converter requisitos de produto, UI e UX em requisitos de engenharia e, somente depois, em uma arquitetura implementável.

## Ordem obrigatória de raciocínio

```text
Produto
   ↓
Experiência
   ↓
Requisitos de engenharia
   ↓
Forças / restrições / atributos de qualidade
   ↓
Alternativas arquiteturais
   ↓
Decisão arquitetural
   ↓
Estrutura do repositório
   ↓
Fronteiras e contratos
   ↓
Critérios para seleção tecnológica
   ↓
Inventário de necessidades de infraestrutura
```

A arquitetura é uma resposta às forças de engenharia. Não deve começar com uma tecnologia ou padrão favorito e tentar adaptar o produto a ele.

## O que deve ser avaliado primeiro — Engenharia

A parte de engenharia deve responder:

> **Quais propriedades técnicas este produto precisa possuir para funcionar, evoluir e ser operado adequadamente?**

Deve avaliar, conforme aplicável:

### Produto e escala

- quantidade esperada de usuários;
- crescimento projetado;
- picos de utilização;
- volume de dados;
- volume de mídia;
- perfil de leitura e escrita;
- necessidade de realtime;
- necessidade de offline;
- processamento assíncrono;
- integrações.

### Qualidade

- disponibilidade;
- latência;
- consistência;
- tolerância a falhas;
- resiliência;
- testabilidade;
- manutenibilidade;
- observabilidade;
- reprodutibilidade;
- auditabilidade.

### Segurança e privacidade

- tipos de dados;
- dados sensíveis;
- autenticação;
- autorização;
- segregação;
- least privilege;
- retenção;
- backup;
- restore;
- superfícies de ataque;
- requisitos regulatórios quando aplicáveis.

### Operação

- tamanho e experiência da equipe;
- tolerância a complexidade operacional;
- frequência de deploy;
- necessidade de staging;
- rollback;
- suporte;
- custo de manutenção;
- necessidade de execução local.

### Evolução

- funcionalidades futuras previsíveis;
- extensibilidade;
- integrações futuras;
- possibilidade de separação de módulos;
- migrações previsíveis;
- portabilidade desejada.

A saída deve produzir forças de engenharia explicitamente identificadas, por exemplo:

```text
ENG-001 — Uma ação concluída offline não pode ser duplicada ao sincronizar.
ENG-002 — O frontend nunca pode possuir credenciais administrativas.
ENG-003 — A API precisa ser implantável sem obrigar novo build do frontend.
ENG-004 — O Beta será mantido por equipe pequena; baixa complexidade operacional é prioridade alta.
```

## O que não deve ser escolhido antes dessa análise

Não escolher antecipadamente apenas por preferência:

```text
MVC
MVVM
Clean Architecture
Hexagonal
microservices
monorepo
Next.js
NestJS
Supabase
Cloud Run
Redis
Kafka
```

Esses nomes representam soluções possíveis. Primeiro deve existir o problema técnico que justifica a solução.

Frameworks, bibliotecas e runtimes concretos serão definidos pela escolha das tecnologias somente depois que as forças e decisões arquiteturais estiverem claras.

## O que pertence à Arquitetura

Depois das forças de engenharia, a arquitetura responde:

> **Qual estrutura técnica satisfaz melhor essas forças?**

Deve definir, conforme aplicável:

- contexto do sistema;
- aplicações e superfícies;
- módulos;
- domínio;
- contratos;
- APIs;
- dados;
- autenticação e autorização;
- cache;
- offline;
- sincronização;
- eventos;
- filas;
- integrações;
- trust boundaries;
- fronteiras de dependência;
- requisitos não funcionais materializados em decisões;
- decisões arquiteturais importantes;
- alternativas rejeitadas.

## Estratégia do repositório é decisão arquitetural

O registro de qualidade e arquitetura deve decidir explicitamente:

- repositório único simples, monorepo ou polyrepo;
- justificativa da escolha;
- estrutura de diretórios;
- aplicações existentes;
- packages/libs compartilhados;
- localização do domínio;
- contratos compartilhados;
- design tokens compartilhados quando houver;
- migrations;
- infraestrutura como código quando existir;
- tooling necessário como categoria, sem escolher ferramenta por hábito;
- testes necessários como camadas e responsabilidades;
- documentação;
- fronteiras de importação;
- ownership lógico.

Perguntas úteis:

- Web e mobile compartilham domínio ou contratos?
- API e worker compartilham runtime?
- Existe necessidade de versionamento independente?
- Times diferentes precisam publicar componentes separadamente?
- Um único CI consegue validar todo o projeto adequadamente?
- O acoplamento de releases é benéfico ou prejudicial?
- Existem bibliotecas internas realmente compartilhadas?

Exemplo de monorepo possível:

```text
/apps
  /web
  /mobile
  /api
  /worker
/packages
  /domain
  /contracts
  /design-tokens
  /config
/infra
/tooling
/docs
```

Esse exemplo não é template obrigatório. Uma única aplicação simples pode ficar melhor em:

```text
/src
/tests
/docs
```

A arquitetura deve evitar complexidade cerimonial.

## Escolha do modelo arquitetural

A IA deve identificar candidatos coerentes e comparar alternativas quando houver decisão material.

Exemplos possíveis:

- MVC;
- MVVM;
- arquitetura em camadas;
- Clean Architecture;
- Hexagonal / Ports and Adapters;
- Modular Monolith;
- microservices;
- event-driven architecture;
- CQRS;
- arquitetura orientada a serverless;
- combinação controlada de padrões.

Não existe arquitetura universal desta metodologia.

Exemplo insuficiente:

```text
Usaremos Clean Architecture porque separa responsabilidades.
```

Exemplo adequado:

```text
O domínio precisa ser compartilhável entre web, mobile e testes sem depender de framework,
banco ou HTTP. Por isso, regras de domínio serão isoladas em um package puro e integrações
entrarão por adapters. Não será adotada uma Clean Architecture cerimonial completa; apenas
as fronteiras que resolvem esse requisito serão utilizadas.
```

A decisão deve explicar quais forças resolve e quais custos introduz.

## Comparação antes da decisão

Quando houver alternativas relevantes, a IA pode usar uma matriz de decisão:

| Critério | Peso | Opção A | Opção B | Opção C |
| --- | ---: | ---: | ---: | ---: |
| simplicidade inicial | | | | |
| testabilidade | | | | |
| isolamento de domínio | | | | |
| velocidade de desenvolvimento | | | | |
| operação | | | | |
| escala | | | | |
| custo de mudança | | | | |
| adequação à equipe | | | | |

A matriz existe para explicitar trade-offs, não para criar precisão matemática artificial.

## Fronteiras devem ser verificáveis

Uma boa decisão arquitetural deve, quando possível, virar regra verificável.

```text
Decisão:
/packages/domain não depende de framework.

Verificação:
boundary check impede imports de frameworks de UI, servidores HTTP ou SDKs de infraestrutura.
```

Outro exemplo:

```text
Decisão:
clientes nunca usam credenciais administrativas.

Verificação:
secret scanning + check de variáveis públicas + teste negativo.
```

Preferir:

```text
DECISÃO
   ↓
REGRA
   ↓
TESTE / CHECK
```

## Decisões rejeitadas também devem ser registradas

Decisões arquiteturais relevantes podem usar ADR curto:

```markdown
### ADR-003 — Não adotar microservices no Beta

Status: aceita

Contexto:
Equipe pequena, domínio ainda em formação e baixo volume inicial.

Decisão:
Modular Monolith.

Motivos:
- menor custo operacional;
- transações simples;
- deploy único do backend;
- fronteiras modulares preservam opção de extração futura.

Revisitar quando:
- módulos precisarem escala independente;
- ownership por times mudar;
- frequência de deploy independente se tornar requisito.
```

Isso impede que um agente futuro reabra decisões sem contexto.

## Saída obrigatória para a escolha das tecnologias e para Infraestrutura

O registro de qualidade e arquitetura deve terminar com requisitos e restrições suficientes para que duas decisões diferentes possam acontecer sem invenção silenciosa:

```text
ARQUITETURA
        ├──→ ESCOLHA DAS TECNOLOGIAS
        │    escolhe stack, frameworks, bibliotecas e tooling
        │
        └──→ INFRAESTRUTURA
             escolhe provedores, ambientes e serviços operacionais
```

Para a escolha das tecnologias, o registro de qualidade e arquitetura pode produzir restrições como:

```text
TL-NEED-001 — O domínio compartilhado não pode depender de framework de UI ou transporte.
TL-NEED-002 — Web e API precisam de contratos tipados e validáveis em runtime.
TL-NEED-003 — O projeto precisa suportar testes unitários, integração e E2E automatizados.
TL-NEED-004 — O backend deve operar de forma stateless na superfície HTTP.
TL-NEED-005 — A solução deve minimizar complexidade operacional para uma equipe pequena.
```

Para Infraestrutura, pode produzir necessidades como:

```text
INF-NEED-001 — Banco relacional gerenciado com backup.
INF-NEED-002 — Auth com e-mail e recuperação de conta.
INF-NEED-003 — Hosting web com CDN.
INF-NEED-004 — Runtime stateless para API.
INF-NEED-005 — Runtime privado para worker.
INF-NEED-006 — Armazenamento privado.
INF-NEED-007 — CI/CD.
INF-NEED-008 — Secrets manager.
INF-NEED-009 — Observabilidade.
```

Arquitetura define **o que tecnicamente precisamos e quais fronteiras devem existir**. A escolha das tecnologias define **com quais tecnologias essas decisões serão materializadas**. A etapa de Infraestrutura define **onde e com quais serviços operacionais essa stack será executada**.

## Critério de qualidade do registro de qualidade e arquitetura

O registro de qualidade e arquitetura está maduro quando outra IA consegue lê-lo e compreender o modelo arquitetural, o tipo de repositório, as fronteiras, a intenção dos módulos, os atributos de qualidade e os critérios que a stack deverá satisfazer sem escolher tecnologias por preferência pessoal.

## Comparação e evidências

Comparar alternativas com restrições e consequências. Registrar limites e verificações, sem transformar a arquitetura de uma empresa de contexto diferente em obrigação para o projeto. Consultar [pesquisa e benchmarking](../pesquisa-e-benchmarking.md) e [verificação com IA](../verificacao-com-ia.md). Reaproveitar evidências atuais suficientes e registrar lacunas relevantes.

[Voltar ao guia](../../README.md)
