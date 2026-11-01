# Continuidade da reorganização

> Estado: R3 preparada para revisão, dependente de R2. R4 e R5 continuam pendentes.

A [Issue #1](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/issues/1) acompanha o trabalho e aponta para as PRs e commits atuais. Este checkpoint guarda contexto de retomada, sem funcionar como outro backlog.

## Versões e dependências

- Origem histórica: `12c87840bcb7779e3072eb717814a7bc28c623b8`; blob original do README `a5ac6dc11df6e9f4e5ecacd28173e536d2c476e9`.
- R1: commit `667a7668ea1761879ae6e05bb7d4716d7ff74f79`, branch `docs/reorganizacao-r1-inventario`, PR #2.
- R2: commit `085fc5f1ea05407e270c79a7fdb68ed45595f3c8`, branch `docs/reorganizacao-r2-etapas`, PR #3.
- R3: branch `docs/reorganizacao-r3-governanca`, criada do commit de R2. Sua PR usa a branch de R2 como base enquanto a dependência estiver aberta.
- No início de R3, as PRs #2 e #3 permaneciam abertas, sem merge, e a main no commit de origem. Conferir o estado atual e as bases antes de integrar ou iniciar a próxima branch.

## O que está preparado

R1 inventariou 29 grupos, 223 títulos e os 15 arquivos do estudo fictício, fixando fontes e blobs. R2 implementou a entrada e 14 etapas, regras comuns, glossário e capítulos técnicos, com destinos e mudanças justificados na [reconciliação R2](reconciliacao-r2.md).

R3 acrescenta:

- [Governança incremental](../governanca.md): responsabilidades, fonte por assunto, aprovação e vigência, substituições, documentação junto com a entrega e conclusão por escopo.
- [Operação no GitHub](../trabalho-no-github.md): fila, hierarquia, tipos, prioridades, status, PRs, ciclos e limites das automações.
- [Handoffs](../handoffs.md): fontes, versões, autorização, estado real e próximo passo, incluindo adaptação para ferramentas e controle de contexto.
- [Modelos](../modelos/README.md): nove modelos reutilizáveis e seu índice; trabalho, bug, pesquisa, índice de Issue, decisão, PR, handoff, checkpoint e instruções para agentes.
- [AGENTS deste repositório](../../AGENTS.md) e template curto de PR em `.github/pull_request_template.md`, preparados para a manutenção do método.
- Vínculos nos capítulos e etapas aplicáveis e a [reconciliação R3](reconciliacao-r3.md).

Os três modelos de Issue estão prontos para adaptação e cópia; não foram instalados como seletores no repositório do produto. Configurações locais, habilidades e Projects externos não foram alterados. O efeito do template de PR deste repositório depende da integração e conferência no GitHub.

## Verificação e limites

A conferência documental cobre links relativos, numeração, blocos de código, cabeçalhos YAML dos templates, campos necessários de aceite/evidência/continuidade e preservação dos identificadores técnicos e de relatório. Os capítulos técnicos e o exemplo anterior continuam preservados, salvo os vínculos e avisos explicitamente registrados nas reconciliações.

Foram percorridas as instruções para pesquisa concluída com decisão pendente, design aprovado sem implementação, implementação com liberação separada e PR dependente. Isso verifica a clareza do procedimento; não comprova uso com leitores externos, renderização dos seletores do GitHub ou adoção das instruções em outras ferramentas.

As fontes oficiais de GitHub usadas para templates, hierarquia, PRs e automações estão registradas nas [referências](referencias.md). R4 aprofundará a pesquisa e a comparação em outras etapas. Não afirmar validação externa ou configuração sem evidência correspondente.

## Próximo passo: R4

1. Ler a Issue #1, este checkpoint, AGENTS, README, regras, governança, [plano](plano.md) e reconciliações pertinentes.
2. Conferir a cadeia de PRs R1 → R2 → R3 e as branches atuais, inclusive comentários, merges e trabalho ainda não integrado. Preservar as alterações anteriores; usar a base real mais recente.
3. Detalhar benchmarking e comparação proporcional ao impacto nas etapas de produto, UX/UI, qualidade, arquitetura, tecnologias e infraestrutura.
4. Criar modelo de registro de comparação: pergunta, critérios, alternativas, fontes, data/versão, contexto, evidência, incertezas, recomendação, decisão e condição de reavaliação. Integrar ao modelo de pesquisa sem duplicar fontes.
5. Definir prevenção e detecção de erros de IA por tipo de tarefa: evidência de usuário, compatibilidade, versões, custos, segurança, testes e comportamento observado. Evitar ranking estatístico de alucinação sem dados.
6. Pesquisar fontes primárias atuais para as afirmações técnicas que forem acrescentadas; explicar limites e o que precisa de experimento, medição ou validação humana.
7. Atualizar capítulos, vínculos, reconciliação, checkpoint e Issue. Publicar PR revisável e conferir o conteúdo remoto.

R5 atualizará o estudo fictício completo para a estrutura, governança e pesquisa novas e consolidará a revisão final. A validação por leitores externos deve permanecer pendente até realmente ocorrer.

## Fontes de retomada

[Plano](plano.md) · [Inventário](inventario.md) · [Reconciliação R2](reconciliacao-r2.md) · [Reconciliação R3](reconciliacao-r3.md) · [Glossário de revisão](glossario.md) · [Referências](referencias.md)

Ao encerrar o próximo recorte, registrar arquivos/commits, evidências, verificações realizadas e pendentes, dependências e próxima ação na Issue e neste checkpoint. O índice da Issue aponta para a continuidade vigente.
