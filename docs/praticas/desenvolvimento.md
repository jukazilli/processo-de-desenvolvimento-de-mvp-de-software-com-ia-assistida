# Padrões de desenvolvimento

Este capítulo preserva as regras técnicas detalhadas do processo. As [etapas numeradas](../../README.md) orientam quando aplicá-las; consulte o [glossário](../glossario.md) para os termos técnicos. As escolhas concretas dependem do projeto.

## Pergunta central

> **Como humanos e agentes de IA podem programar neste projeto?**

## Objetivo

Definir regras operacionais de implementação e estabelecer um padrão de código compreensível, consistente, reutilizável, testável e sustentável, independentemente de quem o escreveu ou de quem fará sua manutenção no futuro.

O padrão de desenvolvimento não deve apenas listar ferramentas de lint, build ou testes. Ele deve funcionar como o **contrato de escrita do código**.

A regra central é:

> **Código é comunicação entre pessoas e máquinas. A IA está sujeita ao mesmo padrão de engenharia exigido de um desenvolvedor humano experiente.**

O resultado esperado é uma base que possa ser entendida por um engenheiro competente de qualquer país, equipe ou época sem depender da memória de quem implementou a funcionalidade e sem apresentar sinais de código produzido sem critério por geração automática.

## Deve conter, quando aplicável

- linguagem e runtime quando já forem uma restrição previamente aprovada;
- política de versões e de fixação de toolchain;
- regras para o package manager definido pelo responsável técnico;
- strictness/type safety ou equivalente;
- organização de módulos;
- convenções de nomes no código;
- idioma técnico do código;
- regras de código claro e coeso;
- critérios de legibilidade;
- limites de dependência;
- regras de reaproveitamento e abstração;
- tratamento de erros;
- logging e observabilidade;
- política de dependências;
- critérios de desempenho;
- migrations;
- política de segredos;
- segurança de cliente e servidor;
- padrão de testes;
- testes de regressão;
- mocks;
- lint;
- formatting;
- typecheck;
- build;
- política de branches;
- commits;
- pull requests;
- revisão de código;
- critérios de conclusão;
- instruções específicas para agentes.

O padrão de desenvolvimento pode impor restrições tecnológicas quando elas já forem decisões de produto, organização ou compliance, mas **não é a camada responsável por escolher a stack completa do projeto**. A seleção concreta de linguagens, runtimes, frameworks, bibliotecas e tooling pertence à escolha das tecnologias, depois que a engenharia e a arquitetura estiverem definidas.

## Princípio de legibilidade universal

O código deve ser escrito para ser lido antes de ser escrito para impressionar.

Preferir:

```text
readable > clever
explicit > implicit
cohesive > fragmented
existing convention > invented convention
small coherent change > broad speculative rewrite
measured optimization > premature optimization
```

Uma implementação não é considerada boa apenas porque compila, passa nos testes ou resolve o caso feliz.

Ela também deve permitir que outro desenvolvedor compreenda rapidamente:

- o que o código faz;
- por que ele existe;
- onde uma regra de negócio está localizada;
- quais dependências utiliza;
- quais invariantes preserva;
- quais efeitos colaterais produz;
- como deve ser testado;
- como pode ser alterado sem quebrar comportamento não relacionado.

A complexidade inevitável deve ficar explícita. Complexidade acidental deve ser removida.

## Inglês como idioma técnico do código

O idioma técnico padrão do código-fonte deve ser **inglês**.

Devem ser escritos em inglês, salvo exceção justificada:

- nomes de variáveis;
- funções e métodos;
- classes;
- interfaces e types;
- enums;
- eventos;
- comandos;
- nomes de módulos e packages;
- arquivos técnicos de código;
- nomes de testes;
- comentários;
- docstrings;
- mensagens internas para desenvolvedores;
- identificadores de logs estruturados quando não forem texto destinado ao usuário.

Exemplo preferido:

```ts
const remainingSets = workout.totalSets - completedSets;

function calculateRestDuration(exercise: Exercise): number {
  return exercise.restSeconds ?? DEFAULT_REST_SECONDS;
}
```

Evitar misturar idiomas:

```ts
const seriesRestantes = treino.totalSets - completedSets;

function calcularRestTime(exercicio: Exercise): number {
  // Calcula o descanso padrão
  return exercicio.restSeconds ?? DEFAULT_REST_SECONDS;
}
```

### Exceções

Essa regra não obriga traduzir conteúdo que **precisa permanecer no idioma ou formato do domínio externo**, por exemplo:

- texto visível ao usuário, que segue a linguagem definida pela UX;
- códigos fiscais, legais ou regulatórios;
- nomes oficiais de campos de uma integração externa;
- payloads de terceiros;
- nomes legados que façam parte de um contrato que não pode ser alterado;
- termos de domínio cuja tradução alteraria o significado oficial.

Mesmo nesses casos, o código ao redor deve continuar legível e a exceção deve permanecer localizada.

## Nomes no código devem revelar intenção

Nomes devem explicar a responsabilidade do elemento sem exigir que o leitor abra sua implementação para descobrir o que ele significa.

### Funções e métodos

Preferir verbos que expressem ação ou resultado:

```ts
createWorkoutPlan()
validateSessionToken()
calculateTrainingVolume()
archiveExercise()
```

Evitar:

```ts
doStuff()
processData()
handleThing()
execute()
runLogic()
```

quando o contexto não torna a intenção inequívoca.

### Booleanos

Devem ser lidos como afirmações:

```ts
isAuthenticated
hasPendingChanges
canEditWorkout
shouldStartRestTimer
```

### Coleções

Devem deixar claro o que contêm:

```ts
activeExercises
pendingMigrations
authorizedApplications
```

em vez de nomes vagos como:

```ts
items
data
list
values
```

quando o escopo não torna o significado evidente.

### Abreviações

Não criar abreviações particulares para economizar caracteres.

Preferir nomes conhecidos pelo domínio e pela comunidade técnica. Abreviações universalmente reconhecidas, como `id`, `url`, `api` ou termos oficiais do domínio, podem ser usadas conforme a convenção da linguagem e do projeto.

## código claro e coeso é requisito, não preferência estética

O projeto deve favorecer:

- responsabilidade clara;
- alta coesão;
- baixo acoplamento;
- dependências explícitas;
- fluxo de controle compreensível;
- funções com propósito identificável;
- módulos com fronteiras coerentes;
- ausência de código morto;
- ausência de duplicação sem justificativa;
- estruturas de dados adequadas ao problema;
- tratamento explícito de estados inválidos;
- separação entre regra de negócio e detalhe de infraestrutura quando a arquitetura assim exigir.

Evitar:

- funções gigantes com responsabilidades diferentes;
- arquivos que acumulam regras não relacionadas;
- condicionais profundamente aninhadas quando o fluxo pode ser simplificado;
- números e strings mágicas;
- parâmetros booleanos ambíguos;
- efeitos colaterais escondidos;
- dependências globais desnecessárias;
- abstrações genéricas que não possuem semântica real;
- `utils`, `helpers`, `common` ou equivalentes como depósitos sem responsabilidade definida;
- camadas criadas apenas para parecer que existe arquitetura;
- generalização antecipada para funcionalidades que ainda não existem.

Não há um número universal de linhas que transforme automaticamente uma função em ruim. O critério é **coesão e facilidade de compreensão**. Se uma unidade exige múltiplos contextos mentais para ser entendida, deve ser avaliada para decomposição.

## Comentários devem explicar o porquê

Comentários e docstrings técnicas devem ser escritos em inglês.

Comentário não deve narrar código óbvio.

Evitar:

```ts
// Increment counter
counter++;
```

Preferir comentário apenas quando existe contexto que o código sozinho não consegue carregar de forma segura:

```ts
// Keep the operation id stable across retries to preserve idempotency.
const operationId = existingOperationId ?? createOperationId();
```

Comentários são apropriados para explicar, por exemplo:

- restrição externa;
- decisão não óbvia;
- workaround temporário;
- invariantes importantes;
- motivo de uma otimização;
- comportamento estranho de biblioteca ou provider;
- regra regulatória difícil de inferir.

Regras:

- não deixar código comentado; Git já preserva histórico;
- comentário desatualizado é defeito e deve ser corrigido ou removido;
- `TODO`, `FIXME` ou equivalente não deve funcionar como esquecimento silencioso; quando representar dívida real, deve possuir contexto suficiente e, quando apropriado, referência rastreável a Issue/backlog;
- não gerar blocos de comentários artificiais apenas para explicar cada passo produzido pela IA.

## Antes de criar código, procurar o que já existe

A IA não deve presumir que precisa criar uma nova função, componente, type, serviço ou abstração.

Antes de implementar, deve procurar no repositório por:

- comportamento equivalente;
- componentes existentes;
- funções de domínio;
- validators;
- adapters;
- hooks;
- contracts/types;
- schemas;
- helpers especializados;
- testes relacionados;
- padrões usados em módulos vizinhos.

O fluxo esperado é:

```text
necessidade nova
      ↓
existe implementação semanticamente equivalente?
      ├── sim → reutilizar ou estender com segurança
      │
      └── não
           ↓
existe duplicação real que justifica abstração?
      ├── sim → extrair responsabilidade coerente
      │
      └── não → implementar localmente de forma simples
```

### Reutilizar não significa forçar abstração

Duas estruturas visualmente parecidas não são necessariamente o mesmo conceito.

A reutilização é adequada quando comportamento, invariantes e motivo de mudança são compatíveis.

Não criar uma abstração compartilhada apenas porque dois blocos possuem algumas linhas iguais se eles representam regras diferentes e provavelmente evoluirão por motivos diferentes.

Preferir composição a hierarquias artificiais quando a composição mantiver responsabilidades mais claras.

## Duplicação deve ser analisada, não normalizada

Copy/paste não pode ser o mecanismo padrão de velocidade da IA.

Ao identificar lógica repetida, o agente deve perguntar:

1. é realmente a mesma regra?
2. as duas ocorrências devem mudar juntas quando o comportamento mudar?
3. já existe um lugar oficial para essa responsabilidade?
4. a extração melhora legibilidade ou apenas reduz linhas?
5. a nova abstração terá nome e contrato claros?

Se a resposta indicar uma regra única, reutilizar ou extrair.

Se forem conceitos diferentes que apenas coincidem hoje, manter separados pode ser mais correto.

O objetivo é evitar simultaneamente:

```text
copy/paste indiscriminado
        e
abstração prematura indiscriminada
```

## Dependências devem possuir justificativa

A IA não deve instalar uma biblioteca para resolver uma capacidade trivial que já pode ser atendida pela plataforma, pelo runtime ou por dependência existente de forma adequada.

Antes de adicionar dependência, verificar:

- a capacidade já existe no projeto?
- a plataforma já resolve?
- a biblioteca é compatível com a versão instalada?
- é mantida?
- aumenta bundle, superfície de ataque ou complexidade operacional?
- será utilizada de forma suficiente para justificar o custo?
- introduz lock-in ou contrato desnecessário?

Quando a tecnologia instalada possuir documentação local ou versão diferente do conhecimento de treinamento do modelo, a IA deve consultar a documentação correspondente à versão efetivamente instalada antes de escrever código.

## Desempenho deve ser tratado com evidência e responsabilidade

Código limpo não significa ignorar desempenho.

A IA deve evitar desde o início anti-padrões evidentes, como:

- complexidade desnecessariamente alta em caminhos frequentes;
- N+1 queries;
- requisições de rede redundantes;
- leitura ou escrita repetitiva sem necessidade;
- serialização excessiva;
- loops que recalculam invariantes;
- renders evitáveis em superfícies críticas quando demonstravelmente relevantes;
- carregamento de dados muito maior que o necessário;
- dependências pesadas para tarefas pequenas;
- consultas sem índices quando o padrão de acesso e o volume justificarem indexação.

Ao mesmo tempo, a IA não deve sacrificar clareza por micro-otimizações especulativas.

O fluxo esperado é:

```text
correção e legibilidade
        ↓
eliminar ineficiências óbvias
        ↓
medir quando existir caminho crítico
        ↓
identificar gargalo real
        ↓
otimizar
        ↓
medir novamente
```

Uma otimização não óbvia que reduza legibilidade deve possuir justificativa técnica e evidência suficiente para que outro mantenedor entenda por que ela existe.

## Tratamento de erros deve ser explícito

Evitar código que engole falhas apenas para manter o fluxo aparentemente funcionando.

Não fazer:

```ts
try {
  await syncWorkout();
} catch {
  // Ignore
}
```

O projeto deve definir quando:

- retornar erro de domínio;
- lançar exceção;
- converter erro externo;
- realizar retry;
- registrar log;
- mostrar feedback ao usuário;
- interromper operação;
- degradar funcionalidade de maneira segura.

Logs técnicos não devem expor segredos, tokens, dados pessoais desnecessários ou payloads sensíveis.

Mensagens internas e estruturas de erro devem ser previsíveis e rastreáveis.

## Testes fazem parte da escrita do código

Testes não são uma etapa decorativa adicionada depois da implementação.

O padrão de desenvolvimento deve definir, conforme a natureza do projeto:

- quais regras exigem teste unitário;
- quais boundaries exigem integração;
- quais jornadas críticas exigem E2E;
- quais contratos exigem testes positivos e negativos;
- quais riscos de segurança exigem testes específicos;
- quais bugs corrigidos exigem regressão.

Regra importante:

> **Bug corrigido que pode reaparecer deve, sempre que tecnicamente viável, deixar um teste de regressão ou check capaz de detectar a mesma classe de falha.**

Nomes de testes e descrições técnicas devem ser escritos em inglês e descrever comportamento, não detalhes acidentais da implementação.

Exemplo:

```ts
it('rejects a workout completion when no exercise was recorded', async () => {
  // ...
});
```

Evitar testes frágeis que apenas espelham a implementação interna e quebram sem mudança de comportamento.

## A IA deve respeitar o estilo existente antes de introduzir um novo

Antes de editar uma área madura do projeto, a IA deve inspecionar código vizinho e identificar:

- nomes no código;
- estrutura de arquivos;
- padrões de importação;
- estratégia de erro;
- estilo de testes;
- composição de componentes;
- convenções de domínio;
- tooling já instalado.

Se o padrão existente for coerente e não violar uma decisão oficial, a IA deve segui-lo.

Se encontrar um padrão ruim ou conflitante, não deve criar silenciosamente um terceiro padrão. Deve corrigir de forma controlada ou registrar a necessidade de refatoração conforme o impacto.

```text
consistência local saudável
        >
invenção de um novo estilo a cada implementação
```

## Anti-padrões típicos de código gerado por IA

A revisão deve procurar e remover sinais de geração automática sem curadoria, como:

- duplicação de lógica que já existia no repositório;
- criação de tipos equivalentes com nomes diferentes;
- arquivos gigantes gerados de uma vez;
- abstrações para cenários hipotéticos nunca solicitados;
- wrappers que apenas repassam argumentos sem responsabilidade real;
- `try/catch` genérico ao redor de grandes blocos;
- uso indiscriminado de `any`, casts ou supressões para silenciar o type system;
- comentários excessivos narrando sintaxe;
- funções chamadas `processData`, `handleData`, `helper`, `utils` sem semântica clara;
- código morto ou imports não utilizados;
- placeholders que parecem implementação concluída;
- TODOs sem rastreabilidade;
- criação de dependências desnecessárias;
- reescrita de arquivos inteiros quando uma alteração localizada resolveria;
- padrões diferentes para resolver o mesmo problema em arquivos próximos;
- tratamento feliz sem considerar estados de erro já previstos nos documentos;
- otimizações inventadas sem medir necessidade;
- código excessivamente genérico que aumenta custo cognitivo para uma necessidade simples.

A IA não recebe liberdade para gerar código sem revisão e deixar a organização para uma revisão futura.

Qualidade estrutural faz parte da própria entrega.

## Contrato operacional da IA antes de escrever código

Antes de começar uma implementação, o agente deve executar mentalmente ou por tooling o seguinte ciclo:

```text
1. ler requisito e documentos de origem
        ↓
2. inspecionar módulo e código vizinho
        ↓
3. procurar componentes, tipos e funções reutilizáveis
        ↓
4. identificar convenções locais
        ↓
5. escolher a menor alteração coerente
        ↓
6. implementar seguindo nomes no código, arquitetura e código claro e coeso
        ↓
7. criar/atualizar testes
        ↓
8. revisar o próprio diff como um reviewer humano experiente
        ↓
9. executar lint, typecheck, testes e gates aplicáveis
        ↓
10. remover redundância, código morto, debug e artefatos temporários
```

A velocidade de geração nunca possui precedência sobre a compreensibilidade da base.

## Auto-revisão obrigatória do diff

Antes de considerar uma alteração pronta, a IA deve revisar o próprio diff perguntando:

- existe uma forma mais simples de expressar a mesma regra?
- criei algo que já existia?
- introduzi duplicação?
- algum nome está vago ou genérico?
- a função ou módulo possui mais de uma responsabilidade?
- existe comportamento implícito que deveria estar explícito?
- comentários explicam motivos ou apenas narram código?
- existe código morto, debug, placeholder ou TODO esquecido?
- introduzi uma dependência sem necessidade?
- alterei arquivos fora do escopo sem justificativa?
- os erros estão tratados de acordo com o projeto?
- a solução respeita boundaries arquiteturais?
- testes cobrem a regra e os casos de falha relevantes?
- existe impacto de desempenho óbvio?
- outro engenheiro entenderia este diff sem precisar conversar comigo?

Esse passo deve ser tratado como parte da implementação, não como atividade opcional.

## Critério de qualidade humana

O objetivo não é tentar enganar detectores de IA ou imitar imperfeições humanas.

O objetivo é que uma revisão técnica não encontre os problemas normalmente associados a código automático sem curadoria.

Um reviewer humano não deveria concluir "isso foi feito por IA" por encontrar:

- nomes no código genérico;
- comentários artificiais;
- abstrações sem necessidade;
- inconsistência com o projeto;
- duplicação evitável;
- código excessivo para um problema simples;
- dependências escolhidas sem contexto;
- ausência de tratamento de falhas;
- testes superficiais;
- performance negligenciada;
- arquivos reescritos sem motivo.

O código deve parecer pertencente ao projeto porque **segue as decisões, linguagem, convenções e qualidade do projeto**, independentemente de ter sido escrito por humano ou IA.

## critérios de conclusão mínima para qualidade de código

Além dos critérios específicos da funcionalidade, uma alteração de código só deve ser considerada pronta quando, conforme aplicável:

- nomes técnicos estão em inglês e revelam intenção;
- comentários/docstrings técnicos estão em inglês e são realmente necessários;
- não existe duplicação evitável;
- abstrações possuem responsabilidade clara;
- código existente foi reaproveitado quando semanticamente adequado;
- nenhuma dependência nova foi adicionada sem justificativa;
- não existe código morto, debug ou import não utilizado;
- não existem erros silenciosamente ignorados;
- regras críticas possuem testes;
- correções de bugs possuem regressão quando viável;
- lint/format/typecheck/build/testes aplicáveis passam;
- boundaries arquiteturais são respeitadas;
- riscos óbvios de performance foram avaliados;
- o diff foi auto-revisado;
- a alteração pode ser compreendida sem depender da conversa que a originou.

## Regra para agentes

Quando uma tecnologia instalada possuir documentação local ou versão diferente do conhecimento de treinamento do modelo, a IA deve consultar a documentação correspondente à versão efetivamente instalada antes de escrever código.

A IA deve considerar o padrão de desenvolvimento uma **restrição de execução**, não uma recomendação opcional. Se uma solicitação induzir código que viole os padrões definidos, o agente deve procurar uma implementação compatível ou explicitar o conflito antes de criar dívida silenciosa.

## Separação entre Técnicas, Engenharia, Arquitetura e escolha das tecnologias

As práticas de desenvolvimento do projeto definem **como o código deve ser escrito e mantido**.

O registro de qualidade e arquitetura define **quais propriedades técnicas o sistema precisa suportar e como ele será estruturado arquiteturalmente**.

As decisões tecnológicas do projeto definem **com quais tecnologias essa arquitetura será implementada**.

O plano de infraestrutura do projeto define **onde essa combinação será executada e como será preparada operacionalmente**.

Exemplo:

```text
Técnica:
O projeto exige type safety, nomes no código em inglês, testes de regressão e dependências justificadas.

Engenharia:
O aplicativo precisa suportar uso offline e reconciliação posterior sem duplicar operações.

Arquitetura:
Persistência local + IDs de operação + comandos idempotentes + sincronização explícita.

escolha das tecnologias:
Selecionar linguagem, runtime e bibliotecas que suportem esse modelo com contratos fortes,
testabilidade, compatibilidade com a plataforma e baixa complexidade acidental.

Infraestrutura:
Selecionar os serviços e ambientes capazes de executar a stack aprovada com segurança,
custo e operação compatíveis com o projeto.
```

[Voltar ao guia](../../README.md)
