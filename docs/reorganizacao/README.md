# Continuidade da reorganização

> Estado: R2 preparada para revisão, dependente de R1. Os aprofundamentos de R3–R5 continuam pendentes.

Este checkpoint permite retomar pelo repositório quando a conversa, pessoa ou ferramenta mudar. A [Issue #1](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/issues/1) controla o trabalho. Esta pasta guarda plano, decisões de organização e evidências da migração.

## Versões e dependência

- Repositório: `jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida`.
- Origem histórica: [`12c87840bcb7779e3072eb717814a7bc28c623b8`](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/tree/12c87840bcb7779e3072eb717814a7bc28c623b8); README com blob `a5ac6dc11df6e9f4e5ecacd28173e536d2c476e9`.
- R1: commit `667a7668ea1761879ae6e05bb7d4716d7ff74f79`, branch `docs/reorganizacao-r1-inventario`, [PR #2](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/pull/2), ainda aberta na conferência de início de R2.
- R2: branch `docs/reorganizacao-r2-etapas`, criada do commit de R1. A PR usa a branch de R1 como base para isolar o recorte desta entrega.
- A `main` foi conferida no início de R2 e permanecia no commit de origem. Conferir novamente antes de integrar ou criar a próxima branch.

## Entregas preparadas

R1 fixou a origem, inventariou os 29 grupos principais e 223 títulos do README e os 15 arquivos de exemplo, propôs vocabulário e corrigiu referências editoriais e endereços de ativação. Os 16 conteúdos de origem foram conferidos com seus hashes Git. Os sete arquivos publicados na PR #2 foram relidos e coincidiram com os conteúdos preparados.

R2 implementa:

- [Entrada do guia](../../README.md), com caminhos para ideia, requisitos, telas, código e correção pequena.
- Quatorze [etapas numeradas](../../README.md), cada uma com objetivo, entradas, atividades, registros, conclusão, reaproveitamento e transferência.
- [Regras comuns](../regras-do-processo.md) e [glossário de leitura](../glossario.md).
- Capítulos detalhados de [experiência](../praticas/experiencia.md), [desenvolvimento](../praticas/desenvolvimento.md), [arquitetura](../praticas/arquitetura.md), [tecnologias](../praticas/tecnologias.md) e [infraestrutura](../praticas/infraestrutura.md), preservando listas, exemplos e exceções da origem.
- [Uso com IA](../ferramentas/uso-com-ia.md) e [capacidades de apoio](../ferramentas/capacidades.md), com versão, leitura verificável e compatibilidade de rótulos de relatório.
- [Reconciliação dos 29 grupos](reconciliacao-r2.md), destinos reais e justificativas de mudanças.
- Aviso no [estudo fictício anterior](../../examples/ava-omem/README.md), cuja atualização completa pertence a R5.

## Conferência documental de R2

Foram conferidos a sequência 01–14, os campos comuns de cada etapa, os links relativos e blocos de código nos arquivos Markdown, a presença dos conjuntos de regras técnicas e a preservação dos rótulos anteriores de relatório e de preparação técnica. Os documentos do exemplo permanecem preservados; sua apresentação recebeu o aviso da estrutura anterior.

Os capítulos técnicos transferem o detalhamento existente em vez de substituir todas as regras por resumos. A [reconciliação R2](reconciliacao-r2.md) registra as mudanças deliberadas: caminhos de entrada, sequência UX/UI, backlog em Issues, separação de etapas e documentos, leitura por conjunto completo aplicável e papel genérico das ferramentas.

Esta é uma verificação documental. Não houve validação com leitores externos, instalação de habilidades, alteração de configurações externas nem execução do método em outras ferramentas. A disponibilidade de todos os links externos não foi revalidada nesta entrega. A integração das PRs ainda depende do estado real no GitHub.

## Próximo passo: R3

1. Ler a Issue #1, este checkpoint, o [plano](plano.md) e a [reconciliação R2](reconciliacao-r2.md).
2. Conferir as PRs e branches de R1 e R2, a `main`, comentários e alterações posteriores. Preservar o trabalho ainda não integrado. Se R1 for integrada, conferir o redirecionamento da base da PR de R2 para a `main` antes de integrar o segundo recorte.
3. Elaborar os modelos operacionais de governança incremental: fontes por assunto, aprovação, substituição, índice da Issue, estado do trabalho e evidência de conclusão.
4. Especificar os modelos de Issue, PR e transferência de contexto. Distinguir pesquisa, design, implementação e liberação; adotar hierarquias apenas quando úteis.
5. Detalhar a operação de Issues/Projects sem inventar uma configuração existente. Projects acompanha; não se torna uma segunda fonte de aprovação de produto.
6. Conferir integração com instruções de agentes e habilidades locais. Preservar nomes de documentos, IDs e campos consumidos até adaptar seus consumidores; não alegar atualização externa sem evidência.
7. Atualizar regras e etapas afetadas, reconciliação, checkpoint e Issue; publicar uma PR com dependência correta e verificações realizadas.

R4 aprofundará benchmarking, fontes e controles de erros de IA por etapa. R5 atualizará os exemplos e consolidará a revisão final, com validação externa declarada apenas se ocorrer.

## Referências da continuidade

- [Plano](plano.md): responsabilidades e critérios das cinco entregas.
- [Inventário de origem](inventario.md): títulos, linhas e blobs imutáveis.
- [Glossário de revisão](glossario.md): correspondência entre vocabulário antigo e novo.
- [Fontes do planejamento](referencias.md): referências primárias e limites de aplicação.

Ao encerrar uma entrega, registrar na Issue e na PR o escopo real, commits, evidências, verificações realizadas e pendentes, conflitos e próximo passo. O checkpoint orienta a retomada; o andamento continua na Issue para evitar um backlog concorrente.
