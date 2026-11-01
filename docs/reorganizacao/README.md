# Continuidade da reorganização

> Estado: R4 preparada para revisão, dependente de R3. R5 continua pendente.

A [Issue #1](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/issues/1) controla o andamento e aponta para as PRs e commits atuais. Este checkpoint guarda contexto de retomada; a fila não é duplicada aqui.

## Base e cadeia de dependências

- Origem: `12c87840bcb7779e3072eb717814a7bc28c623b8`; README original com blob `a5ac6dc11df6e9f4e5ecacd28173e536d2c476e9`.
- R1: `667a7668ea1761879ae6e05bb7d4716d7ff74f79`, branch `docs/reorganizacao-r1-inventario`, PR #2.
- R2: `085fc5f1ea05407e270c79a7fdb68ed45595f3c8`, branch `docs/reorganizacao-r2-etapas`, PR #3.
- R3: `7622778161b784c36bf7769520536a31b10ba28e`, branch `docs/reorganizacao-r3-governanca`, PR #4.
- R4: branch `docs/reorganizacao-r4-benchmarking`, criada de R3; sua PR depende da branch de R3 enquanto ela não estiver integrada.
- No início de R4, as PRs #2–#4 estavam abertas, sem merge, e a main no commit de origem. Conferir novamente antes de integrar ou criar a próxima branch.

## O que já foi preparado

R1 fixou a origem, inventariou 29 grupos, 223 títulos e os 15 arquivos do estudo fictício. R2 organizou a entrada e as 14 etapas, preservando regras técnicas detalhadas. R3 definiu governança incremental, operação no GitHub, handoffs e nove modelos reutilizáveis. Ver as reconciliações anteriores para destinos e mudanças justificadas.

R4 acrescenta:

- [Pesquisa e benchmarking](../pesquisa-e-benchmarking.md), com método, critérios, alternativas, contexto, reaproveitamento e condições para reavaliar.
- [Verificação com IA](../verificacao-com-ia.md), distinguindo fonte, observação, inferência, estimativa, proposta e execução comprovada.
- [Catálogo de fontes](../fontes-de-referencia.md), com doze referências primárias, versões ou natureza contínua e limites de aplicação.
- [Modelo de comparação](../modelos/comparacao.md), ligado ao modelo de pesquisa; o conjunto tem agora dez modelos reutilizáveis e seu índice.
- Orientações próprias nas 14 etapas, seções adicionais nos cinco capítulos técnicos e vínculos na governança, handoffs, instruções e modelos pertinentes.
- [Reconciliação R4](reconciliacao-r4.md), incluindo decisões de aplicação e limites.

## Conferência e limites

A conferência documental cobre navegação, links relativos, campos das etapas e do registro, YAML dos três templates de Issue e preservação de fontes, IDs e rótulos. As etapas e capítulos técnicos receberam adições identificáveis; o conteúdo anterior é conferido por comparação com R3. Os 15 arquivos do exemplo anterior permanecem sem alteração nesta entrega.

Os percursos documentais consideram reuso de material suficiente, afirmação de API sem versão conferida, preço desconhecido, imagem sem prova de usabilidade e comparação sem experimento executado. O resultado não comprova validação por leitores externos, teste de produto, instalação de habilidades ou configuração externa.

As fontes primárias foram consultadas para sustentar orientações e limites. Não foi produzida taxa de alucinação do método, ranking universal por etapa, estimativa de preço para um produto concreto ou alegação de conformidade integral com padrões citados.

## Próximo passo: R5

1. Ler a Issue #1, AGENTS, README, regras, governança, este checkpoint, o plano, inventário e reconciliações pertinentes.
2. Conferir PRs, comentários, branches e commits. Preservar a cadeia R1 → R2 → R3 → R4 e trabalho não integrado; após cada integração, conferir a base e o diff da dependente.
3. Revisar os 15 arquivos do exemplo fictício e seus vínculos, atualizando nomes, numeração, papéis e operação de trabalho para o método novo. Retirar dependências de contexto particular e distinguir decisões ilustrativas de escolhas validadas.
4. Demonstrar o caminho de projeto novo e o de uma pessoa com requisitos ou outros materiais prontos. Não obrigar descoberta do zero, renomeação de IDs ou uma nova pesquisa suficiente já existente.
5. Substituir a fila e matriz locais do exemplo por demonstrações de Issues, hierarquia, aceite e vínculos, sem criar backlog operacional concorrente nem inventar Issues reais ou testes executados.
6. Incorporar exemplos de comparação, decisão e handoff com fontes ou hipóteses identificadas. Um resultado fictício não pode ser apresentado como pesquisa, preço ou validação reais.
7. Conferir a cobertura de todos os grupos do inventário, termos, campos de compatibilidade, links, instruções, modelos e exemplos. Registrar cada mudança final e suas condições; manter a versão de origem acessível no histórico Git.
8. Percorrer os cenários de uso e registrar resultados documentais e limitações. Validação por leitores externos só pode ser declarada se realmente ocorrer.
9. Atualizar checkpoint e Issue, publicar PR revisável e conferir o conteúdo remoto. A preparação das entregas não equivale à integração das PRs nem à configuração de ambientes externos.

## Fontes de retomada

[Plano](plano.md) · [Inventário](inventario.md) · [Reconciliação R2](reconciliacao-r2.md) · [Reconciliação R3](reconciliacao-r3.md) · [Reconciliação R4](reconciliacao-r4.md) · [Referências correntes](../fontes-de-referencia.md) · [Histórico de referências](referencias.md)
