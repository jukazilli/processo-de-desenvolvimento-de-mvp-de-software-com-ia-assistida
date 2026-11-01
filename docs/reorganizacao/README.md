# Continuidade da reorganização

> Estado: R1–R5 preparadas para revisão, em PRs dependentes. Nenhuma integração ou validação por leitores externos foi realizada nesta sequência.

A [Issue #1](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/issues/1) controla o andamento e aponta para PRs e commits atuais. Este arquivo registra retomada; não duplica a fila.

## Base e dependências

| Entrega | Branch | Commit de referência | PR |
| --- | --- | --- | --- |
| Origem | main antes da reorganização | `12c87840bcb7779e3072eb717814a7bc28c623b8` | — |
| R1 | `docs/reorganizacao-r1-inventario` | `667a7668ea1761879ae6e05bb7d4716d7ff74f79` | #2 |
| R2 | `docs/reorganizacao-r2-etapas` | `085fc5f1ea05407e270c79a7fdb68ed45595f3c8` | #3 |
| R3 | `docs/reorganizacao-r3-governanca` | `7622778161b784c36bf7769520536a31b10ba28e` | #4 |
| R4 | `docs/reorganizacao-r4-benchmarking` | `3032dec85b7ee4ddd3a68e7b5769b931703c732f` | #5 |
| R5 | `docs/reorganizacao-r5-exemplos` | Consultar head da PR e Issue #1 | Base: branch de R4 |

No início de R5, main ainda estava na origem e PRs #2–#5 abertas, em rascunho, sem merge. Conferir novamente antes de integrar. Preservar a ordem R1 → R2 → R3 → R4 → R5 e conferir base/diff das dependentes após cada integração.

## O que foi preparado

- R1: inventário de 29 grupos, 223 títulos e 15 arquivos do estudo fictício; plano, termos, referências e checkpoint.
- R2: guia de entrada e 14 etapas; cinco capítulos técnicos preservados; regras, glossário e guias de ferramentas.
- R3: governança incremental, Issues/Projects/PRs, handoffs, modelos e instruções locais para manter o método.
- R4: pesquisa e benchmarking contextual, verificação com IA, 12 fontes primárias, comparação e orientações nas etapas.
- R5: exemplo genérico em 19 documentos; entrada por materiais existentes; critérios de 29 Issues e seus IDs; rastreabilidade sem matriz de status concorrente; comparação, handoff, validação e operação ilustrativos. Os 15 caminhos anteriores são encaminhamentos com origem histórica.

## Conferência e limites

As reconciliações registram destinos e alterações justificadas. Em R5, etapas, práticas técnicas, regras, governança, modelos e guias de ferramentas não foram alterados frente a R4. Conferências documentais cobrem navegação, formatos, campos e contratos; resultados e contagens estão na Issue/PR desta entrega.

Não houve implantação, execução de produto, homologação de habilidades, configuração externa ou teste com leitores. Preços, versões, compatibilidade, aprovações e execução do produto fictício não são apresentados como evidências reais. A clareza para a comunidade precisa ser acompanhada com retorno de leitores após revisão e disponibilização.

## Retomada e integração

1. Ler AGENTS, README, regras, governança, Issue #1, este checkpoint e os documentos afetados.
2. Conferir branches, comentários, commits, PRs e trabalho não integrado; usar fontes atuais antes de editar.
3. Revisar [R2](reconciliacao-r2.md), [R3](reconciliacao-r3.md), [R4](reconciliacao-r4.md) e [R5](reconciliacao-r5.md), incluindo critérios do plano e inventário.
4. Integrar somente com autorização aplicável, conferindo as dependências a cada passo. Nenhuma caixa de integração deve ser marcada apenas porque uma PR foi preparada.
5. Verificar a versão integrada e registrar revisão externa e problemas concretos em Issues, mantendo o histórico.

[Plano](plano.md) · [Inventário](inventario.md) · [Fontes correntes](../fontes-de-referencia.md) · [Histórico de fontes](referencias.md) · [Exemplo](../../examples/plataforma-de-cursos/README.md)
