# Capacidades de apoio para ferramentas de IA

Este guia descreve capacidades que podem ser implementadas por instruções, habilidades, agentes ou automações equivalentes. Não pressupõe que estejam instaladas ou validadas no seu ambiente. O guia principal define as etapas; estas capacidades apoiam sua execução.

A metodologia não deve depender de frameworks privados ou nomes exclusivos de uma máquina.

Ela deve documentar **as capacidades necessárias** para que outro ambiente compatível possa recriá-las como skills, agents, comandos, checks ou automações equivalentes.

```text
PROCESSO OFICIAL
        ↓
define capacidades
        ↓
SKILLS
habilidades reutilizáveis e pequenas
        ↓
AGENTS
orquestram responsabilidades maiores
```

## Diferença entre habilidade e agente

### Habilidade (skill)

Uma skill é uma habilidade reutilizável com gatilho, entradas, regras, saída e limites claros.

Exemplos:

- verificar consistência documental;
- comparar screenshot com referência;
- detectar padrão de bug recorrente;
- validar fronteiras arquiteturais.

### Agente (agent)

Um agent é um papel operacional que coordena documentos, ferramentas e várias skills para alcançar um objetivo maior.

Exemplos:

- conduzir a Fundação;
- executar uma entrega do backlog;
- revisar uma release;
- auditar arquitetura;
- revisar qualidade visual.

## Skill recomendada — `document-consistency`

### Objetivo

Manter documentação, backlog, vínculos de rastreabilidade, código, testes e evidências coerentes entre si.

Deve verificar, conforme aplicável:

- documentos oficiais;
- backlog;
- vínculos de rastreabilidade;
- Issues relevantes;
- código alterado;
- testes;
- CI/staging;
- documentação derivada.

Não permitir inconsistências como:

```text
Issue = concluída em implementação
PR = sem vínculo com critérios de aceite
Teste = inexistente
Pré-produção = sem evidência
```

Também deve detectar:

- implementação que contradiz arquitetura;
- stack instalada que contradiz a escolha das tecnologias;
- UI que contradiz Princípios;
- backlog sem origem documental;
- requisito removido ainda tratado como ativo;
- documento descrevendo comportamento inexistente;
- código entregue sem atualização de rastreabilidade.

A skill não pode mascarar um bug atualizando o documento automaticamente para combinar com o runtime incorreto. Antes deve determinar qual camada possui precedência.

## Skill recomendada — `backlog-evidence-audit`

### Objetivo

Determinar se um item foi realmente entregue.

```text
requisito
   ↓
critérios de aceite
   ↓
implementação existe?
   ↓
testes cobrem critérios?
   ↓
gates aprovados?
   ↓
staging é necessário e foi validado?
   ↓
evidência é suficiente?
```

Estados úteis:

```text
NOT_STARTED
IN_PROGRESS
IMPLEMENTED_NOT_VALIDATED
VALIDATED
BLOCKED
```

Não inferir `VALIDATED` apenas porque existe commit.

## Skill recomendada — `architecture-conformance`

### Objetivo

Transformar decisões do registro de qualidade e arquitetura em verificações recorrentes.

Exemplo:

```text
Decisão:
packages/domain não depende de frameworks.

Skill:
verifica imports proibidos.
```

Outro exemplo:

```text
Decisão:
cliente não possui segredo administrativo.

Skill:
verifica variáveis públicas, bundles e padrões de secrets.
```

Quando uma decisão ainda não possuir check automatizável, a skill deve registrar a lacuna como oportunidade de tooling.

## Skill recomendada — `foundation-readiness`

### Objetivo

Determinar se a Fundação está realmente pronta para receber funcionalidades.

Pode verificar:

- estrutura do repo conforme arquitetura;
- stack e toolchain conforme escolha das tecnologias;
- lockfile;
- CI;
- branches/proteções quando acessíveis;
- banco;
- migrations;
- auth mínima;
- serviços;
- secrets;
- staging;
- observabilidade mínima;
- smoke tests;
- rastreabilidade operacional.

Resultado:

```text
FND_READY
FND_PARTIAL
FND_BLOCKED
```

## Skill de aprendizado — `discover-to-skill`

### Objetivo

Detectar quando um conhecimento descoberto durante uma ocorrência no projeto possui valor suficiente para virar habilidade reutilizável.

A finalidade é reduzir retrabalho, contexto repetido e gasto de tokens em problemas já compreendidos.

Um evento é candidato quando, por exemplo:

- o mesmo bug ocorreu novamente;
- o mesmo diagnóstico exige raciocínio extenso repetidamente;
- um setup é realizado de forma semelhante em vários projetos;
- existe erro previsível que pode ser detectado antes de build/deploy;
- uma regra de revisão se repete;
- a correção pode virar check determinístico;
- um incidente revelou uma classe de problema, e não apenas um caso isolado.

Fluxo:

```text
ocorrência real
        ↓
IA resolve
        ↓
há valor de reutilização?
        ↓
procurar skill/check existente
        ↓
registrar Issue com causa e prevenção
        ↓
acionar mecanismo de criação de skill disponível
        ↓
criar teste/check quando possível
        ↓
executar consistência documental
```

Exemplo:

```text
Bug reaparece em migrations
        ↓
IA reconhece a mesma causa raiz
        ↓
correção novamente consome contexto e tokens
        ↓
discover-to-skill classifica como reutilizável
        ↓
registra Issue
        ↓
registra causa, detecção e prevenção
        ↓
cria skill/check/teste
        ↓
próxima ocorrência pode ser detectada antes
```

Antes de criar uma nova skill, verificar se já existe capacidade equivalente.

Nem todo bug deve virar skill. Problema isolado, improvável de repetir e sem valor geral permanece como correção normal.

Pergunta de decisão:

> **Se esse evento ocorrer novamente, queremos que a IA gaste praticamente o mesmo raciocínio para resolvê-lo?**

Se a resposta for não, existe candidato para skill, check, runbook ou automação.

### Issue como memória operacional

Uma ocorrência reutilizável pode ser registrada em Issue com estrutura semelhante a:

```markdown
## Problema recorrente

## Sintoma

## Causa raiz

## Como detectar

## Como corrigir

## Como prevenir

## Onde ocorreu

## Potencial de automação
```

A Issue funciona como memória auditável do incidente, não como substituto da documentação oficial.

## Skill visual — `visual-reference-to-spec`

### Objetivo

Transformar uma referência visual em informação estruturada e comparar essa referência com a UI real do projeto.

Pode receber:

- screenshot;
- wireframe;
- aplicativo de referência;
- tela aprovada;
- protótipo visual.

Primeiro deve decompor a referência, conforme observável:

- arquitetura da informação;
- hierarquia;
- tarefa mental aparente;
- densidade;
- espaçamento;
- alinhamento;
- grid;
- tipografia relativa;
- superfícies;
- navegação;
- posição de CTAs;
- ações secundárias;
- estados;
- padrões de componentes;
- sinais de marca.

Depois deve cruzar a referência com:

- `princípios de experiência do projeto`;
- decisões de interface da etapa 05;
- Design System;
- tarefa mental da tela.

A referência visual não possui precedência automática sobre os princípios do produto.

Por fim, deve comparar a referência com screenshot da implementação e gerar delta objetivo:

| Aspecto | Referência | Implementação | Delta | Severidade |
| --- | --- | --- | --- | --- |
| CTA | persistente inferior | topo | viola direção | alta |
| densidade | baixa | cards aninhados | excessiva | alta |
| tipografia | hierarquia clara | pesos semelhantes | fraca | média |

A saída deve explicar **o que mudar e por quê**, relacionando a correção às decisões oficiais. Não apenas dizer "deixe igual à imagem".

Referências externas servem para inspiração e análise de padrões. A skill deve evitar copiar cegamente identidade proprietária, assets ou textos distintivos quando o objetivo é construir identidade própria.

## Habilidades complementares

### `issue-to-knowledge`

Converte Issues relevantes encerradas em conhecimento persistente quando houver valor além do ticket, podendo gerar:

- runbook;
- ADR;
- check;
- teste de regressão;
- atualização de arquitetura;
- atualização de técnicas;
- atualização da escolha das tecnologias;
- nova skill.

Nem toda Issue exige nova documentação.

### `ui-principles-audit`

Revisa uma tela contra os princípios específicos da aplicação, avaliando:

- tarefa mental dominante;
- competição entre CTAs;
- densidade;
- linguagem;
- visibilidade da ação principal;
- exposição de ações destrutivas;
- consistência com a personalidade da marca;
- comportamento responsivo;
- sinais de UI genérica.

Os achados devem ser relacionados a princípios identificáveis, não ao gosto subjetivo do agente.

## Agentes recomendados

### `document-steward-agent`

Coordena consistência documental, reconciliação de status, precedência e ausência de fontes concorrentes.

Pode usar `document-consistency`, `backlog-evidence-audit` e `issue-to-knowledge`.

### `architecture-review-agent`

Revisa forças de engenharia, alternativas arquiteturais, estrutura de repo, boundaries, ADRs e conformidade arquitetural.

### `foundation-orchestrator-agent`

Consome Técnicas + Engenharia/Arquitetura + escolha das tecnologias + Infraestrutura + itens FND e conduz o setup, respeitando gates humanos para autenticação, custo e ações destrutivas.

### `backlog-implementation-agent`

Executa uma entrega oficial do backlog, lê origens documentais, implementa, testa, produz evidência e atualiza rastreabilidade.

### `visual-quality-agent`

Coordena análise de referência, princípios, decisões de interface da etapa 05, screenshots e correções de fidelidade/identidade.

### `release-audit-agent`

Valida se uma release possui critérios, testes, gates, staging, evidência e rastreabilidade suficientes antes da promoção.

## Regra de portabilidade

A metodologia define o comportamento esperado das capacidades, não a implementação privada de uma máquina.

Cada ambiente pode implementá-las por skills, agents, comandos ou checks equivalentes, desde que preserve o contrato de comportamento e os gates humanos definidos aqui.

As descrições são requisitos de capacidade, não arquivos instaláveis. Conferir acesso, comandos e evidências antes de afirmar execução. Consultar os [handoffs](../handoffs.md) e o [modelo de instruções para agentes](../modelos/instrucoes-para-agentes.md) para adaptar e conferir a integração.

[Voltar ao guia](../../README.md)
