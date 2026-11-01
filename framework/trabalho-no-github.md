# Operação do trabalho no GitHub

Usar a estrutura que o projeto já possui quando ela atende ao objetivo. A configuração mínima tem Issues, prioridades, critérios de aceite e vínculos para PRs e fontes oficiais. Projects é útil para visualizar andamento e ciclos, mas não é obrigatório.

## Da decisão ao próximo item pronto

1. Reunir as decisões e requisitos aprovados pertinentes. Uma lacuna pode originar uma Issue de pesquisa, sem exigir aprovação de uma solução inexistente.
2. Procurar Issue equivalente antes de criar outra. Definir objetivo, limites, origem, resultado e evidência esperada usando o [modelo de trabalho](modelos/issue.md).
3. Dividir um objetivo grande somente quando isso permitir responsáveis, dependências ou aceites próprios. Criar vínculo nativo de sub-Issue quando disponível e conferir sua existência.
4. Ordenar por prioridade, explicitar dependências e refinar o próximo trabalho. O distante pode ter menos detalhe; o próximo precisa de contexto suficiente.
5. Antes de executar, confirmar responsável, fontes acessíveis, decisões suficientes, aceite, ações autorizadas e dependências resolvidas ou exceções aceitas.

Um checklist com links não comprova vínculo nativo de pai e filho. Se a ferramenta não puder criar ou ler a hierarquia, registrar a limitação. Não declarar subordinação criada com base apenas em texto.

## Hierarquia útil

| Nível ilustrativo | Função | Quando criar |
| --- | --- | --- |
| Iniciativa ou objetivo | Resultado maior e índice de partes | Quando agrupa várias entregas independentes |
| Funcionalidade, jornada ou tela | Escopo coerente com contrato ou resultado próprio | Quando ajuda a manter decisões e acompanhamento |
| Tarefa ou estado | Trabalho assumível, com aceite e evidência | Quando exige execução ou revisão independente |

Uma tela pode ter vários estados na mesma Issue se o contrato e a revisão forem conjuntos. Não criar uma Issue para cada variação visual só para repetir a árvore de pastas. O objetivo é facilitar assumir e revisar o trabalho, não maximizar a quantidade de cartões.

## Tipos e prioridades

Tipos possíveis: Funcionalidade, Bug, Documentação, Pesquisa técnica, Infraestrutura e Design. Usar labels ou campos já disponíveis; não presumir que todos os recursos de organização e tipos estejam habilitados na conta.

Uma convenção simples de prioridade pode usar P0 para incidente ou bloqueio crítico que exige tratamento imediato, P1 para trabalho prioritário da próxima entrega e P2 para a fila normal. A equipe define critérios e responsável pela triagem; severidade técnica e prioridade de negócio podem ser diferentes. Não preencher prioridade por aparência do título.

## Status sugeridos

Esta é uma proposta de significado, não a configuração observada de um Projects. Mapear os estados existentes antes de alterar campos.

| Status | Significado e entrada | Para avançar |
| --- | --- | --- |
| Backlog | Trabalho selecionado para a fila; pode precisar de refinamento | Fontes, escopo, aceite e dependências suficientes |
| Pronto | Outra pessoa consegue assumir sem inventar decisões relevantes | Escolha de execução e responsável definidos |
| Em progresso | Trabalho ativo no escopo da Issue, inclusive investigação | Resultado do recorte e evidências preparados para revisão |
| Em revisão | Resultado preparado, aguardando revisão, auditoria, integração ou consolidação pertinente | Aceite e verificações do escopo confirmados; fontes atualizadas |
| Feito | Aceite do escopo, evidências, consistência e consolidação documental concluídos | Encerramento rastreável; evolução vira novo trabalho |

Roadmap e Planejado podem ser adicionados se houver necessidade de separar ideias futuras de oportunidades investigadas. Nesse caso, Roadmap guarda oportunidade sem compromisso; Planejado indica objetivo, escopo e horizonte avaliados, ainda não selecionados para execução. A seleção para Backlog é deliberada. Manter hipóteses e estudos fora das decisões aprovadas.

Bloqueio pode ser um campo ou indicação na própria Issue: registrar causa, dependência, responsável e condição para retomar. Não criar novos estados só por conveniência de uma ferramenta. Itens sem status precisam de triagem, não de aprovação presumida.

## Quatro informações que não se substituem

- Estado operacional: por exemplo, Em revisão no Projects, com data de conferência.
- Estado da decisão: proposta, aprovada, pendente ou substituída, com escopo e vigência.
- Estado do GitHub: Issue aberta/fechada; PR em rascunho, aberta ou integrada.
- Evidência de execução: o que foi implementado, testado, validado em ambiente e liberado.

Registrar cada uma no handoff. Sem acesso ao Projects, informar não verificado e usar o estado da Issue como informação separada.

## PRs, vínculo e encerramento

Uma PR descreve o problema, a alteração e a evidência, usando o [modelo](modelos/pull-request.md). Vincular a Issue e indicar dependências de outras PRs. Se a base for outra branch em revisão, conferir novamente a base e o diff depois da integração da dependência.

No GitHub, palavras como `Closes` e `Fixes` podem acionar fechamento automático conforme o vínculo, a branch de destino e as configurações do repositório. O comportamento deve ser conferido no projeto. Usar uma referência simples quando a PR cobre apenas parte da Issue. Não fechar uma iniciativa inteira por concluir um recorte.

Um merge não comprova aprovação de produto, consolidação documental completa ou liberação. Conferir os critérios do escopo e o estado operacional antes de marcar Feito. Aprovação de design pode encerrar uma Issue de design enquanto implementação permanece em outra Issue.

## Ciclos e automações

O campo Iteração pode agrupar Issues em períodos de trabalho, por exemplo, uma semana. Isso não transforma o processo automaticamente em Scrum. Fluxo contínuo também é válido. Registrar objetivo e capacidade reais sem mover itens entre ciclos para esconder trabalho incompleto.

Antes de mudar uma automação, conferir evento, filtro, ação, permissões e efeito nos estados. Auto-adicionar itens pode ajudar na triagem. Um fluxo que transforma qualquer fechamento em Feito pode violar os critérios de consolidação; não habilitá-lo sem avaliar essa equivalência. Não mover trabalho por prioridade ou tipo como se isso comprovasse avanço.

Os guias e modelos não configuram Projects, automações ou proteções por si mesmos. Registrar sucesso somente após a ferramenta confirmar a mudança. Sem capacidade suficiente, documentar o passo pendente de forma verificável.

## Fontes técnicas

- [GitHub — Sub-Issues](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/adding-sub-issues).
- [GitHub — Vínculos entre PR e Issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/linking-a-pull-request-to-an-issue).
- [GitHub — Automação integrada de Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects/automating-your-project/using-the-built-in-automations).
- [GitHub — Fechamento automático por merge](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/managing-repository-settings/managing-auto-closing-issues).

[Governança](governanca.md) · [Handoffs](handoffs.md) · [Voltar ao guia](../README.md)
