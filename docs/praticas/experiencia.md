# Princípios, jornadas e interface

As etapas 04 e 05 distinguem princípios de decisão, comportamento e aparência. Os princípios orientam as duas áreas; as jornadas esclarecem comportamento antes do detalhamento visual, e o aprendizado pode levar a revisão. Ver [glossário](../glossario.md).

## Princípios de experiência

### Pergunta central

> **Quando houver mais de uma solução de interface possível, qual decisão combina melhor com a experiência que esta aplicação quer oferecer?**

### Natureza do documento

Os princípios de experiência formam um **conjunto de regras de decisão específico da aplicação**.

Esses princípios não especificam telas individualmente. Eles orientam as decisões que serão depois materializadas pela Direção de UI, pelo Design System e pela Especificação de UX.

Os princípios devem ser definidos de acordo com o contexto, a identidade e o comportamento desejado para aquela aplicação.

### Eixos obrigatórios

#### Baixa carga cognitiva

A experiência deve minimizar:

- memorização;
- procura visual;
- interpretação desnecessária;
- comparação simultânea;
- excesso de escolhas;
- mudança de contexto;
- necessidade de reaprender padrões entre telas.

Exemplo de princípio:

```text
A ação principal necessária para concluir uma tarefa deve permanecer
perceptível durante a execução daquela tarefa.
```

Aplicação possível:

```text
Formulário longo
+ ação principal = salvar
+ risco de o botão sair da área visível
→ preferência por ação persistente no rodapé.
```

O princípio orienta a decisão. Ele não obriga que todos os botões de todas as telas tenham a mesma posição sem considerar o contexto.

#### Baixa densidade

Baixa densidade não significa apenas aumentar espaços vazios. Significa reduzir a quantidade de elementos que disputam atenção simultaneamente.

O documento deve orientar:

- quantidade de informações primárias;
- hierarquia visual;
- progressão de complexidade;
- exposição de ações raras;
- uso de detalhes sob demanda;
- redução de controles redundantes.

#### Linguagem do usuário

A aplicação deve falar sobre a tarefa que o usuário quer realizar, e não sobre a estrutura interna do software.

Preferir:

```text
Salvar treino
Adicionar exercício
Concluir série
```

Evitar:

```text
Persistir alterações
Adicionar entidade
Finalizar registro
```

Esse princípio vale para títulos, CTAs, erros, confirmações, empty states, onboarding, ajuda contextual e feedbacks.

#### Comunicação e personalidade da marca

A personalidade da marca deve influenciar a experiência completa, não somente textos promocionais.

Devem ser documentados atributos como, por exemplo:

- séria;
- alegre;
- energética;
- próxima;
- técnica;
- calma;
- premium;
- objetiva.

Esses atributos podem orientar:

- tom de voz;
- tipografia;
- hierarquia;
- densidade;
- movimentos e microinterações;
- ícones;
- feedbacks;
- ritmo da navegação;
- grau de celebração;
- cores;
- ilustrações;
- intensidade visual.

A intenção é remover o aspecto de interface genérica e dar identidade reconhecível ao produto.

### Os princípios devem ser avaliáveis

Evitar princípios vagos como:

```text
A interface deve ser simples.
```

Preferir estruturas como:

```markdown
## P-UX-004 — Uma tarefa mental dominante

### Objetivo
Permitir que o usuário identifique rapidamente o que deve fazer.

### Regra
Cada estado principal de uma tela deve possuir uma tarefa mental dominante.

### Critérios
- deve existir apenas uma CTA de maior hierarquia;
- ações secundárias não devem competir visualmente com a principal;
- informação sem utilidade imediata deve perder hierarquia;
- ações destrutivas não devem dominar visualmente a tela, salvo quando a própria tarefa for confirmar uma exclusão.

### Perguntas de avaliação
1. O objetivo da tela é reconhecível rapidamente?
2. Mais de uma ação compete pela atenção?
3. Existe informação visível sem utilidade para a tarefa atual?
4. O usuário precisa lembrar algo de outra tela para continuar?
```

### Papel no processo

```text
IDENTIDADE DA MARCA
        +
COMPORTAMENTO HUMANO
        +
PRINCÍPIOS DE EXPERIÊNCIA
        ↓
DECISÕES DE UI/UX
```

## Jornadas e comportamentos

### Pergunta central

> **Como o usuário percorre, executa e conclui a experiência?**

### Objetivo

Especificar jornadas, user stories, estados, transições, erros e exceções.

### Deve conter

- jornadas;
- user stories;
- fluxos;
- estados;
- transições;
- loading;
- empty state;
- erros;
- sucesso;
- confirmações;
- validações;
- interrupções;
- retomadas;
- acessibilidade comportamental;
- gestos quando aplicáveis;
- comportamento por plataforma;
- microcopy crítica.

### Exemplo de jornada

```text
Selecionar exercício
        ↓
Iniciar
        ↓
Exibir série atual
        ↓
Ajustar carga/repetições se necessário
        ↓
Concluir série
        ↓
Descanso
        ↓
Próxima série
        ↓
Última série?
  não ─────────┘
  sim
        ↓
Próximo exercício
```

### Exemplo de User Story

```text
Como praticante,
quero registrar cada série individualmente,
para acompanhar o que realizei sem interromper meu treino.
```

### Distinção entre os três documentos de experiência

| Documento | Função | Pergunta |
| --- | --- | --- |
| `princípios de experiência do projeto` | orientar decisões | Qual solução combina com a experiência desejada? |
| `decisões de interface do projeto` | especificar contexto, telas e hierarquia | O que deve existir e como deve ser representado? |
| `jornadas e comportamentos do projeto` | especificar jornadas e comportamento | Como o usuário percorre e conclui a experiência? |

Resumo:

```text
Princípios → orientam
Etapa 05 → especifica a interface
Etapa 04 → especifica a jornada
```

## Interface e sistema visual

### Pergunta central

> **O que deve existir na interface para suportar cada contexto e tarefa mental, e qual deve ser sua hierarquia?**

### Objetivo

Especificar contextos, telas, tarefas mentais, elementos necessários e representação visual.

Este documento é específico. Diferentemente dos Princípios, ele toma decisões concretas para superfícies e contextos.

### Deve conter

- contextos de uso;
- telas e superfícies;
- tarefa mental principal de cada tela;
- informações obrigatórias;
- ações principais;
- ações secundárias;
- ações raras ou destrutivas;
- hierarquia visual;
- estrutura de navegação local;
- componentes previstos;
- tokens e fundamentos visuais;
- tipografia;
- espaçamento;
- cores semânticas;
- densidade;
- estados visuais;
- responsividade;
- regras do Design System.

### Exemplo

```markdown
## Tela: Editar treino

### Contexto
Usuário está montando ou ajustando um treino.

### Tarefa mental principal
Montar o treino.

### Elementos obrigatórios
- nome;
- exercícios;
- adicionar exercício;
- salvar;
- excluir treino.

### Hierarquia
- Salvar: ação principal;
- Adicionar exercício: ação contextual;
- Excluir: ação destrutiva de baixa frequência.

### Decisão de interface
Salvar permanece persistente no rodapé durante formulários longos.
Excluir fica em ação secundária e não compete visualmente com Salvar.
```

### Relação com o Design System

O Design System materializa decisões. Ele não deve decidir sozinho o contexto de uso.

```text
Princípio
   +
Contexto / tarefa mental
   ↓
Decisão de UI
   ↓
Componente do Design System
```

## Comparação e evidências

Ligar a escolha visual ou comportamental à tarefa, referência e hipótese que precisam de validação. Adaptar padrões preservando identidade e conferir estados e acessibilidade; não apresentar uma imagem como prova de uso. Consultar [pesquisa e benchmarking](../pesquisa-e-benchmarking.md) e [verificação com IA](../verificacao-com-ia.md). Reaproveitar evidências atuais suficientes e registrar lacunas relevantes.

[Voltar ao guia](../../README.md)
