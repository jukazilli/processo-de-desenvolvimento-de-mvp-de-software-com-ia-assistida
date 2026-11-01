# Reconciliação operacional em R3

> Estado: governança, modelos e handoffs preparados para revisão. R4 aprofundará benchmarking e R5 atualizará os exemplos.

A base é R2, commit `085fc5f1ea05407e270c79a7fdb68ed45595f3c8`. Sua PR #3 ainda estava aberta no início desta entrega. A branch `docs/reorganizacao-r3-governanca` parte desse commit e sua PR depende da branch de R2 enquanto ela não estiver integrada. Conferir a cadeia R1 → R2 → R3 e as bases antes de integrar.

## Responsabilidades implementadas

| Necessidade | Destino | Evidência documental |
| --- | --- | --- |
| Fonte oficial por assunto e responsável | [Governança](../governanca.md) | Tabela de autoridade, papéis, vigência e resolução de conflito |
| Documentação incremental | [Governança](../governanca.md) | Atualização junto com a entrega, documentos sob demanda e consolidação proporcional |
| Índice e comentários aprovados | [Modelo de índice](../modelos/indice-da-issue.md), [decisão](../modelos/decisao.md) | Corpo curto, detalhe e histórico vinculados, substituição explícita e assets versionados |
| Backlog no GitHub | [Operação](../trabalho-no-github.md), [etapa 10](../etapas/10-trabalho-no-github.md) | Issues como fila, hierarquia útil, vínculos nativos conferidos e Projects opcional |
| Status e conclusão | [Operação](../trabalho-no-github.md), [governança](../governanca.md) | Cinco estados básicos e critérios de conclusão por tipo de trabalho |
| Propostas futuras e prioridade | [Operação](../trabalho-no-github.md) | Roadmap/Planejado opcionais, tipos e prioridades por critérios do projeto |
| Evidência e separação de estados | [Handoffs](../handoffs.md), [modelo](../modelos/handoff.md) | Andamento, aprovação, Issue/PR e execução/QA tratados separadamente |
| Transferência e controle de contexto | [Handoffs](../handoffs.md), [checkpoint](../modelos/checkpoint.md) | Fontes e versões, autorização, trabalho não integrado, evidência e próximo passo |
| Integração com agentes e habilidades | [Instruções adaptáveis](../modelos/instrucoes-para-agentes.md), [uso com IA](../ferramentas/uso-com-ia.md) | Inventário de consumidores, adaptação revisável e verificação no ambiente; sem instalação presumida |
| Manutenção deste método | [AGENTS](../../AGENTS.md), template de PR em `.github/pull_request_template.md` | Leitura, preservação, verificações documentais e checkpoint definidos |
| Formulários de trabalho reutilizáveis | [Modelos](../modelos/README.md) | Trabalho, bug e pesquisa com cabeçalho compatível com templates Markdown; adoção no destino deve ser conferida |

## Relação com o inventário de origem

Os grupos 2, 13–18, 23–25 e 28 do README original já tinham destinos em R2. R3 aprofunda seu uso operacional sem retirar os capítulos técnicos nem alterar a sequência de 14 etapas. Ver a [reconciliação R2](reconciliacao-r2.md) e o [inventário](inventario.md) para as fontes e a cobertura anteriores.

Os procedimentos foram ligados ao README, às regras comuns, ao uso com IA e às etapas 01, 10, 12, 13 e 14. O registro antigo de relatório e os IDs técnicos foram preservados. Configurações locais do usuário, habilidades instaladas e Projects privados não foram acessados ou alterados por esta entrega.

## Escolhas de aplicação

- O caminho mínimo usa uma Issue, PR quando há alteração de arquivos e evidência de conclusão. Índices, decisões e handoffs são acrescentados quando trazem clareza.
- O README só muda quando uma decisão geral ou índice pertinente precisa de atualização. Consolidação não significa reescrevê-lo para toda tarefa.
- Feito significa aceite, evidência, consistência e consolidação no escopo da Issue. Pesquisa, design, implementação e liberação podem ter entregas próprias.
- Os cinco status são uma proposta adaptável. A documentação não cria um Projects nem muda automações existentes.
- Templates genéricos de Issues ficam em `docs/modelos/`; não foram instalados como seletores de Issues do repositório do produto. O template curto de PR e o AGENTS são específicos para a manutenção deste repositório e ficam preparados nesta branch.
- A adaptação para ferramentas descreve como conferir o ambiente. Publicar um modelo não comprova que ele foi carregado por uma máquina ou por um agente.
- Fontes oficiais do GitHub foram consultadas sobre templates, hierarquia, vínculos, fechamento e automações. O método não exige fechamento automático nem avanço para Feito por merge.

## Conferência e pendências

Foram conferidos navegação, campos dos nove modelos, YAML dos três templates de Issue, consistência dos estados, IDs e rótulos preservados e ausência de referências a projetos particulares. Foram percorridos documentalmente casos de pesquisa concluída com decisão pendente, design aprovado sem backend, implementação sem liberação e PR dependente. A conferência dos links relativos abrange os 61 arquivos Markdown da branch.

Esses percursos conferem o que os documentos instruem. Não equivalem a uso com leitores externos, renderização efetiva dos templates no seletor do GitHub, configuração de Projects ou teste das instruções em outras ferramentas.

R4 deve inserir comparação estruturada e prevenção/detecção de erros de IA em cada etapa pertinente, com fontes e modelos de evidência. R5 deve adaptar o estudo fictício completo aos procedimentos e revisar a consistência final.

[Continuidade](README.md) · [Plano](plano.md)
