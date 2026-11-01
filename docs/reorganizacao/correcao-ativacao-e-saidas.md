# Correção: framework operacional, explicação e saídas

> Integrada à main pela PR #7, por autorização do responsável, no merge commit `d8cba5eb1541514f32100aa5c67d60bb99705db7`. Base de preparação: `e2eb7f94e09faf1dfcc7424e7851b78b31e427f3`. A branch corretiva e as cinco branches R1–R5 permanecem preservadas.

## Problema e direção autorizada

A versão integrada explicava atividades, mas deixava a ativação e o artefato de saída dependentes de escolhas de quem adotasse o método. A solicitação corretiva fixou: README como o próprio processo consumido pela IA; docs como explicação para pessoas; entrada curta que inicia a análise; conteúdo revisável a cada etapa; um documento principal incremental do produto.

## Separação implementada

- **README:** ativação, interpretação da entrada, condução e os 14 contratos operacionais, com campos específicos e destino de saída. Sem inventário ou andamento da migração no topo.
- **framework:** detalhamento operacional preservado, modelos e compatibilidade. Carregamento por atividade; sem outra porta de ativação obrigatória.
- **docs:** propósito, como usar/revisar, organização, fontes e histórico. Páginas de etapas explicam a entrega e apontam para a seção correspondente no README.
- **Produto desenvolvido:** `docs/PROJETO.md` como saída padrão, com seções de etapa, fontes e continuidade; não criado na documentação deste método.

## Destinos dos materiais operacionais

Os caminhos anteriores foram preservados como páginas explicativas com link ao destino, sem outra cópia editável da regra. Os cinco capítulos técnicos, templates e capacidades não foram resumidos. Seus textos foram preservados com ajuste de links; extensões do contrato são identificadas nos módulos afetados.

| Caminho anterior | Destino operacional |
| --- | --- |
| `docs/regras-do-processo.md` | [framework/regras-do-processo.md](../../framework/regras-do-processo.md) |
| `docs/governanca.md` | [framework/governanca.md](../../framework/governanca.md) |
| `docs/trabalho-no-github.md` | [framework/trabalho-no-github.md](../../framework/trabalho-no-github.md) |
| `docs/handoffs.md` | [framework/handoffs.md](../../framework/handoffs.md) |
| `docs/pesquisa-e-benchmarking.md` | [framework/pesquisa-e-benchmarking.md](../../framework/pesquisa-e-benchmarking.md) |
| `docs/verificacao-com-ia.md` | [framework/verificacao-com-ia.md](../../framework/verificacao-com-ia.md) |
| `docs/praticas/arquitetura.md` | [framework/praticas/arquitetura.md](../../framework/praticas/arquitetura.md) |
| `docs/praticas/experiencia.md` | [framework/praticas/experiencia.md](../../framework/praticas/experiencia.md) |
| `docs/praticas/infraestrutura.md` | [framework/praticas/infraestrutura.md](../../framework/praticas/infraestrutura.md) |
| `docs/praticas/desenvolvimento.md` | [framework/praticas/desenvolvimento.md](../../framework/praticas/desenvolvimento.md) |
| `docs/praticas/tecnologias.md` | [framework/praticas/tecnologias.md](../../framework/praticas/tecnologias.md) |
| `docs/modelos/pull-request.md` | [framework/modelos/pull-request.md](../../framework/modelos/pull-request.md) |
| `docs/modelos/instrucoes-para-agentes.md` | [framework/modelos/instrucoes-para-agentes.md](../../framework/modelos/instrucoes-para-agentes.md) |
| `docs/modelos/handoff.md` | [framework/modelos/handoff.md](../../framework/modelos/handoff.md) |
| `docs/modelos/bug.md` | [framework/modelos/bug.md](../../framework/modelos/bug.md) |
| `docs/modelos/issue.md` | [framework/modelos/issue.md](../../framework/modelos/issue.md) |
| `docs/modelos/indice-da-issue.md` | [framework/modelos/indice-da-issue.md](../../framework/modelos/indice-da-issue.md) |
| `docs/modelos/comparacao.md` | [framework/modelos/comparacao.md](../../framework/modelos/comparacao.md) |
| `docs/modelos/README.md` | [framework/modelos/README.md](../../framework/modelos/README.md) |
| `docs/modelos/decisao.md` | [framework/modelos/decisao.md](../../framework/modelos/decisao.md) |
| `docs/modelos/pesquisa.md` | [framework/modelos/pesquisa.md](../../framework/modelos/pesquisa.md) |
| `docs/modelos/checkpoint.md` | [framework/modelos/checkpoint.md](../../framework/modelos/checkpoint.md) |
| `docs/ferramentas/capacidades.md` | [framework/ferramentas/capacidades.md](../../framework/ferramentas/capacidades.md) |
| `docs/ferramentas/uso-com-ia.md` | [framework/continuidade-e-compatibilidade.md](../../framework/continuidade-e-compatibilidade.md) |

As atividades das 14 páginas anteriores foram transferidas para as etapas do README. Entradas, ações, pesquisa, conteúdo a registrar, aceite e condições de reaproveitamento foram comparados com a base, normalizando somente os caminhos dos links e os níveis de títulos. Os detalhes de transferência e módulos pertinentes continuam no contrato; a expressão de destino livre foi substituída pela saída padrão explícita.

## Mudanças de regra e limites

| Regra anterior | Correção | Preservação e limite |
| --- | --- | --- |
| Prompt inicial detalhado a adaptar | Uma entrada curta com objetivo, link, etapa e materiais opcionais | Acesso e versão precisam ser reais; sem acesso à fonte essencial não alegar carregamento |
| Resposta inicial principalmente de confirmação | Situar o recorte e começar a análise possível | Perguntar o necessário; entregar parcial quando faltar evidência; não inventar pesquisa |
| Saída poderia ser documento, Issue ou escolha do projeto sem padrão | Seção revisável de `docs/PROJETO.md` do produto | Fontes existentes são preservadas até migração explícita; anexos continuam possíveis por necessidade |
| Conhecimento distribuído em documentos ou comentários | Consolidação incremental no principal, com links a discussão/evidências nas Issues | Sem fila concorrente ou cópia de contrato cuja autoridade ainda esteja em outro local |
| Etapas em docs como instrução e explicação misturadas | Contrato operacional no README; explicação de revisão em docs | Os 14 conjuntos de atividades e critérios foram preservados, com saídas explícitas |
| Modelos sugerindo documentos próprios por formato | Modelos podem ser blocos da seção correspondente | Templates de Issue mantêm YAML e funções; publicar o modelo não instala configuração externa |
| Falta de repositório sem caminho claro | Markdown revisável na conversa, ainda não salvo | Não bloqueia análise nem autoriza escrita, contratação, merge ou publicação |

A aprovação de conteúdo e a autorização para registrar podem vir na mesma instrução. Rascunho salvo não equivale a aprovação; mudança de trecho já aprovado deve preservar a decisão anterior até revisão. O conhecimento pode conter hipóteses, desde que identificadas, sem promover proposta automaticamente.

## Percursos documentais conferidos

| Entrada ou evento | Comportamento definido | Saída verificável nos arquivos |
| --- | --- | --- |
| Ideia de pets + iniciar discovery | Avaliação breve da 01 e trabalho da 02 | Exemplo parcial com hipótese explícita, fontes e continuidade, sem demanda inventada |
| Executar somente a primeira etapa | Avaliar materiais e lacunas, sem obrigar discovery completo | Seção 01 com ponto de partida e próximo recorte |
| Requisitos sem briefing | Aproveitar requisitos e esclarecer lacunas | Seção 03 consolidada a partir das fontes, sem pesquisa do zero por rotina |
| Materiais existentes + etapa 04 | Conferir dependências e trabalhar UX | Seção 04, reutilizando fontes suficientes |
| Pasta ou link inacessível | Informar lacuna, pedir fonte acessível e trabalhar apenas no que independe dela | Rascunho parcial, sem alegar leitura da pasta |
| Sem repositório do produto | Iniciar análise e apresentar Markdown | Rascunho ainda não salvo; destino esperado identificado |
| Issue resolvida | Conferir aceite e consolidar somente conhecimento durável afetado | Seções e fontes atualizadas na mesma entrega, sem copiar backlog |
| Retomar em outra conversa/ferramenta | Conferir seção 16 e fontes atuais | Próxima ação, versões, evidências e limites; habilidades locais não presumidas |

O exemplo anterior com documentos separados continua acessível como material existente e histórico de IDs; seu índice aponta para o padrão atual e para o exemplo de saída única. Não se apresentam os dois como padrões operacionais concorrentes.

## Validação e próximo passo

Foram conferidos links e anchors locais, títulos, sequência das etapas, campos do modelo, YAML dos três templates de Issue, preservação dos materiais movidos, IDs e 18 campos legados. Resultados e contagens ficam registrados na Issue #1 e na PR. As verificações são documentais; não houve teste com leitor externo, implantação, execução do produto fictício ou homologação em ChatGPT/Codex/Gemini.

A PR corretiva foi integrada sem conflitos. A árvore resultante coincidiu com a árvore revisada da PR #7; o registro posterior altera somente o estado da integração nos dois documentos de continuidade. Próximo passo: experimentar com uma entrada real e verificar leitura das fontes, conteúdo da primeira saída e persistência no destino. Registrar a evidência antes de alegar validação externa. Não alterar nem excluir as cinco branches anteriores.

[Checkpoint](README.md) · [Documentação](../README.md) · [Processo](../../README.md) · [Exemplo atual](../../examples/ativacao/README.md)
