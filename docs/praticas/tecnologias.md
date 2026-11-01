# Escolha das tecnologias

Este capítulo preserva as regras técnicas detalhadas do processo. As [etapas numeradas](../../README.md) orientam quando aplicá-las; consulte o [glossário](../glossario.md) para os termos técnicos. As escolhas concretas dependem do projeto.

## Pergunta central

> **Com quais linguagens, runtimes, frameworks, bibliotecas e ferramentas a arquitetura aprovada deve ser implementada para maximizar qualidade de código, manutenibilidade, testabilidade, segurança e desempenho dentro das restrições reais do projeto?**

## Objetivo

Transformar as decisões de engenharia e arquitetura em uma **stack tecnológica explícita, coerente e justificável**, eliminando a liberdade do agente de escolher bibliotecas, frameworks ou ferramentas de forma oportunista durante a implementação.

O registro de decisões tecnológicas do projeto funciona como o contrato tecnológico do projeto.

Ele responde:

```text
Engenharia
"O que o sistema precisa suportar?"
        ↓
Arquitetura
"Como o sistema será estruturado?"
        ↓
escolha das tecnologias
"Com quais tecnologias vamos implementar essa estrutura?"
```

A escolha tecnológica não deve anteceder a compreensão do problema técnico.

## Entradas necessárias

A escolha das tecnologias deve consumir, no mínimo:

- `práticas de desenvolvimento do projeto`, para respeitar o padrão de qualidade e escrita do código;
- `decisões de qualidade e arquitetura do projeto`, como fonte primária das forças, fronteiras e decisões estruturais;
- decisões relevantes de UI/Design System quando a seleção de tecnologia de frontend depender delas;
- decisões relevantes de UX quando jornadas exigirem offline, realtime, mídia, acessibilidade, gestos ou comportamento específico de plataforma;
- restrições organizacionais, legais, de licenciamento ou segurança já aprovadas.

A escolha das tecnologias **não pode alterar silenciosamente** o registro de qualidade e arquitetura para tornar uma tecnologia preferida mais conveniente.

Se uma tecnologia desejada exigir mudança arquitetural, a decisão deve retornar ao fluxo documental anterior.

## O que deve definir

Conforme o projeto, o documento deve definir explicitamente:

### Linguagens e runtimes

- linguagem principal de cada aplicação/superfície;
- runtime de frontend, backend, worker, mobile ou desktop;
- versão principal ou política de versão;
- política de LTS quando aplicável;
- nível de strictness/type safety;
- interoperabilidade entre runtimes quando houver mais de um.

### Frameworks

- framework de frontend;
- framework de backend/API;
- framework mobile/desktop quando existir;
- estratégia de rendering quando aplicável;
- framework ou mecanismo de jobs/workers quando necessário;
- justificativa de cada escolha.

### Bibliotecas oficiais por responsabilidade

O responsável técnico deve evitar que cada entrega do projeto escolha uma biblioteca diferente para resolver o mesmo problema.

Definir, quando necessário, a tecnologia oficial para:

- validação de schemas;
- contratos e serialização;
- acesso a dados/ORM/query builder;
- migrations;
- data fetching/cache de servidor no cliente;
- state management;
- formulários;
- roteamento;
- datas e fusos horários;
- internacionalização;
- autenticação no código quando a arquitetura já definir o modelo;
- upload/mídia;
- filas/jobs;
- logging;
- observabilidade;
- feature flags;
- testes unitários;
- testes de integração;
- E2E;
- mocks;
- componentes de UI quando houver justificativa;
- gráficos, editor rico, mapas ou outras capacidades especializadas realmente necessárias.

A ausência de uma biblioteca é também uma decisão válida. Se a plataforma ou framework já resolve adequadamente o problema, preferir não adicionar dependência.

### Toolchain

Definir, conforme aplicável:

- package manager;
- workspace/monorepo tooling;
- bundler/build system;
- lint;
- formatter;
- typecheck;
- test runner;
- coverage;
- dependency audit;
- secret scanning;
- geração de código quando necessária;
- automações locais que sustentam o padrão de desenvolvimento.

### Compatibilidade e versões

O documento deve registrar uma matriz suficiente para evitar combinações incompatíveis.

Exemplo:

| Camada | Tecnologia | Versão/política | Motivo | Restrições relevantes |
| --- | --- | --- | --- | --- |
| Linguagem | `<definir>` | `<definir>` | qualidade/type safety | — |
| Runtime API | `<definir>` | LTS ou política aprovada | estabilidade | compatibilidade do framework |
| Web | `<definir>` | major aprovada | UX/rendering | runtime suportado |
| Validação | `<definir>` | compatível | contratos | usada em boundaries |
| Testes | `<definir>` | compatível | feedback rápido | integração com build |

Não é necessário fixar cada patch eternamente no documento. O lockfile materializa o estado exato instalado. O documento deve preservar as versões ou políticas de compatibilidade que representam uma decisão técnica relevante.

## Pesquisa atual é obrigatória para escolhas materiais

Frameworks, bibliotecas, runtimes e ferramentas mudam rapidamente.

Antes de aprovar e registrar uma escolha material, a IA deve pesquisar fontes atuais, priorizando:

1. documentação oficial;
2. política de suporte/LTS;
3. release notes relevantes;
4. compatibilidade entre versões;
5. situação de manutenção do projeto;
6. advisories de segurança quando relevantes;
7. licença;
8. documentação e qualidade do ecossistema.

Não selecionar tecnologia apenas com base em memória de treinamento do modelo, popularidade histórica ou uso em um projeto anterior.

A pesquisa deve ser especialmente cuidadosa quando a escolha afetar:

- arquitetura;
- segurança;
- performance;
- tamanho de bundle;
- compatibilidade de runtime;
- lock-in;
- capacidade de testes;
- manutenção futura;
- licenciamento.

## Critérios de seleção

Cada escolha relevante deve ser avaliada com base no que o projeto realmente precisa.

Critérios possíveis:

- aderência ao registro de qualidade e arquitetura;
- capacidade de produzir código claro e previsível;
- type safety quando pertinente;
- qualidade da documentação;
- maturidade;
- manutenção ativa;
- segurança;
- testabilidade;
- desempenho;
- ergonomia sem esconder comportamento importante;
- tamanho e custo de runtime/bundle;
- interoperabilidade;
- facilidade de observabilidade;
- capacidade de automação;
- curva de aprendizado da equipe;
- disponibilidade de profissionais;
- portabilidade;
- lock-in;
- licença;
- custo de atualização;
- compatibilidade com a infraestrutura provável.

Quando houver alternativas relevantes, usar comparação explícita.

| Critério | Peso | Opção A | Opção B | Opção C |
| --- | ---: | ---: | ---: | ---: |
| aderência arquitetural | | | | |
| legibilidade/manutenção | | | | |
| type safety | | | | |
| testabilidade | | | | |
| desempenho | | | | |
| segurança | | | | |
| maturidade/manutenção | | | | |
| complexidade adicionada | | | | |
| impacto operacional | | | | |
| lock-in | | | | |

A pontuação serve para expor trade-offs. Não deve criar precisão matemática artificial.

## Uma biblioteca por responsabilidade, salvo justificativa

A stack deve reduzir liberdade acidental durante a implementação.

Exemplo desejado:

```text
Schema validation → uma solução oficial
Data access       → uma solução oficial
Unit tests        → um runner oficial
E2E               → uma solução oficial
Formatting        → uma configuração oficial
```

Evitar:

```text
módulo A usa biblioteca X
módulo B usa biblioteca Y
módulo C implementa manualmente
```

para a mesma responsabilidade sem motivo arquitetural.

Exceções são permitidas quando plataformas diferentes realmente exigirem soluções diferentes, mas devem ser explícitas.

## Contratos de uso importam tanto quanto a escolha

Não basta escrever:

```text
"Usaremos biblioteca X."
```

O documento deve explicar **onde e para quê** ela pode ser usada.

Exemplo conceitual:

```text
Validação de entrada
→ todos os dados que atravessam boundary externo são validados pelo mecanismo oficial.

Acesso a dados
→ módulos de domínio não importam o client/ORM diretamente; adapters fazem essa mediação.

State management
→ estado local de componente permanece local; store global só é usada para estado realmente compartilhado.
```

Isso evita que a mesma tecnologia seja utilizada de formas incompatíveis em diferentes partes do projeto.

## Dependências devem ser minimizadas

O responsável técnico não deve produzir um catálogo de bibliotecas "úteis".

Toda dependência relevante precisa de uma necessidade concreta.

Antes de aprovar uma biblioteca, perguntar:

1. qual requisito ou decisão arquitetural ela atende?
2. o runtime/framework já resolve isso adequadamente?
3. já existe uma dependência aprovada para essa responsabilidade?
4. a biblioteca melhora qualidade ou apenas reduz algumas linhas?
5. qual custo ela adiciona em bundle, segurança, atualização e complexidade?
6. é possível substituí-la sem romper o domínio?

Uma stack menor e coerente normalmente é preferível a uma stack extensa com múltiplas abstrações sobrepostas.

## Tecnologias rejeitadas também devem ser registradas quando a decisão for material

Exemplo:

```markdown
### TL-DEC-004 — Não adicionar segundo state manager

Contexto:
A stack já possui uma solução oficial para estado compartilhado e o novo caso pode ser
resolvido por estado local ou cache de dados.

Decisão:
Não adicionar nova biblioteca.

Motivo:
Evitar dois modelos mentais, dependência duplicada e aumento de bundle.

Revisitar quando:
A solução existente não conseguir atender um requisito comprovado.
```

Esse registro impede que um agente futuro reabra a mesma escolha sem contexto.

## Relação com Infraestrutura

A escolha das tecnologias escolhe a **stack de implementação**. Infraestrutura escolhe os **serviços e ambientes que executarão essa stack**.

```text
responsável técnico:
Node-compatible runtime necessário
        ↓
Infraestrutura:
comparar provedores capazes de executar esse runtime
```

A Infraestrutura não deve trocar framework, linguagem ou biblioteca oficial apenas para acomodar um provedor preferido.

Se uma restrição real de infraestrutura tornar a stack inviável, deve ocorrer reconciliação:

```text
restrição de infraestrutura
        ↓
impacta stack?
        ↓
sim
        ↓
reabrir decisão do responsável técnico
        ↓
impacta arquitetura?
        ↓
se sim, reabrir registro de qualidade e arquitetura
        ↓
aprovação humana
```

## Saída para Fundação e Backlog

A escolha das tecnologias deve produzir decisões suficientemente objetivas para gerar FND e checks.

Exemplos:

```text
TL-STACK-001 — Linguagem/runtime principal aprovados.
TL-STACK-002 — Framework web aprovado.
TL-STACK-003 — Framework/API aprovado.
TL-LIB-001   — Validação de schemas possui solução oficial.
TL-LIB-002   — Acesso a dados possui solução oficial.
TL-TEST-001  — Runner unitário aprovado.
TL-TEST-002  — E2E aprovado.
TL-TOOL-001  — Package manager e workspace tooling aprovados.
```

Essas decisões podem originar itens como:

```text
FND — fixar versões e lockfile
FND — criar workspace
FND — configurar lint/format/typecheck
FND — configurar test runner
FND — configurar boundary checks
FND — instalar apenas dependências oficiais aprovadas
```

O executor não deve escolher uma alternativa tecnológica diferente durante o FND apenas porque conhece outra biblioteca.

## Critério de qualidade da escolha das tecnologias

O documento está maduro quando outro engenheiro ou agente consegue montar a toolchain e iniciar a implementação sem precisar decidir novamente:

- linguagem;
- runtime;
- framework principal de cada superfície;
- package manager;
- ferramentas de qualidade;
- bibliotecas centrais por responsabilidade;
- regras de uso dessas bibliotecas;
- política de versões;
- alternativas rejeitadas relevantes.

Ao mesmo tempo, o documento não deve tentar prever toda dependência futura. Bibliotecas especializadas podem ser acrescentadas quando um requisito real surgir, seguindo o mesmo processo de avaliação, aprovação e consistência documental.

## Comparação e evidências

Conferir pacote, origem, documentação e compatibilidade da versão. Separar capacidade publicada de comportamento comprovado no projeto e justificar dependências e alternativas rejeitadas. Consultar [pesquisa e benchmarking](../pesquisa-e-benchmarking.md) e [verificação com IA](../verificacao-com-ia.md). Reaproveitar evidências atuais suficientes e registrar lacunas relevantes.

[Voltar ao guia](../../README.md)
