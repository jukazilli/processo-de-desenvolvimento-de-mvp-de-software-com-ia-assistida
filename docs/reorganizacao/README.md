# Continuidade da reorganização

> Estado: R1–R5 integradas à main pelas PRs #2–#6, por autorização do responsável. Todas as cinco branches foram preservadas. Validação por leitores externos permanece pendente.

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

## Retomada após integração

1. Ler AGENTS, README, regras, governança, Issue #1, este checkpoint e os documentos afetados.
2. Conferir branches, comentários, commits, PRs e trabalho não integrado; usar fontes atuais antes de editar.
3. Revisar [R2](reconciliacao-r2.md), [R3](reconciliacao-r3.md), [R4](reconciliacao-r4.md) e [R5](reconciliacao-r5.md), incluindo critérios do plano e inventário.
4. A integração foi autorizada e concluída na ordem R1 → R2 → R3 → R4 → R5. Para mudanças futuras, conferir a base e o escopo antes de integrar.
5. Verificar a versão integrada e registrar revisão externa e problemas concretos em Issues, mantendo o histórico.

[Plano](plano.md) · [Inventário](inventario.md) · [Fontes correntes](../fontes-de-referencia.md) · [Histórico de fontes](referencias.md) · [Exemplo](../../examples/plataforma-de-cursos/README.md)

## Registro da integração

As cinco PRs foram redirecionadas para main quando necessário e integradas em ordem, com merge commits. A árvore da main após a PR #6 coincidiu integralmente com a árvore revisada de R5 (`c7ceb0ec8eb21d508eb5aa6e38d1ebfae43eb94c`). As cinco branches foram consultadas e permanecem nos commits de referência, sem exclusão ou alteração.

| Entrega | PR | Merge commit |
| --- | --- | --- |
| R1 | #2 | `92578f91214abb6c841cdedd311fe93327fcb511` |
| R2 | #3 | `b632b9cbfbfcb67f143bcb18262769f6b7ecd1b3` |
| R3 | #4 | `f0d9d9bbfd05dfd7d06a19ea7533e09c80ff81b0` |
| R4 | #5 | `f509ec4963d1a6420e10b71edaff5785a9a3f879` |
| R5 | #6 | `a472bee42cdd951cfe30ac24552fc521d5131de1` |

Os registros de preparação acima descrevem a origem e os limites das entregas. Não havia checks de CI configurados nos commits consultados; a verificação foi documental e de integridade Git. Este registro não declara teste de aplicação ou validação externa.

## Correção posterior: ativação e documento incremental

Após a integração de R1–R5, o responsável identificou a mistura entre explicação do método e instruções operacionais, além da ausência de saída padrão. A correção foi integrada à main pela PR #7, por autorização do responsável, no merge commit `d8cba5eb1541514f32100aa5c67d60bb99705db7`. A branch `fix/ativacao-e-saidas-do-framework` e as cinco branches anteriores foram preservadas.

Ver [escopo, destinos e verificações](correcao-ativacao-e-saidas.md). O README passa a ser a entrada da IA e o contrato das 14 etapas; `docs/` explica adoção e revisão; `framework/` guarda o detalhamento operacional. A saída padrão fica no produto como `docs/PROJETO.md`, com uma seção por etapa e atualização incremental ligada às Issues.

A Issue #1 aponta para PR/commit atuais e resultados das conferências. A árvore da main após o merge coincidiu integralmente com a árvore revisada da PR #7 (`1a4ca17aaf99265b5fc8b54a83a0ca811a42434c`). Antes de continuar, conferir fontes e comentários atuais. Validação com entradas reais e leitores externos continua pendente.
