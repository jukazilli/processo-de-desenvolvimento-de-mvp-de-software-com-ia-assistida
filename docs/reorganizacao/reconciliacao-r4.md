# Reconciliação de pesquisa e verificação em R4

> Estado: benchmarking, fontes e controles preparados para revisão. R5 permanece responsável pelos exemplos completos e pela consolidação final.

A base é R3, commit `7622778161b784c36bf7769520536a31b10ba28e`. No início desta entrega, a PR #4 ainda estava aberta, assim como suas dependências #3 e #2. A branch `docs/reorganizacao-r4-benchmarking` parte de R3 e mantém a dependência até a integração correspondente. Conferir a cadeia e as bases antes de integrar ou criar o próximo recorte.

## O que foi acrescentado

| Necessidade | Destino real | Tratamento |
| --- | --- | --- |
| Comparar referências sem inventar uma solução | [Pesquisa e benchmarking](../pesquisa-e-benchmarking.md) | Pergunta, critérios, alternativas, fontes, contexto, consequência e condição para reavaliar |
| Definir onde comparar e onde conferir execução | [Etapas 01–14](../../README.md) e tabela no guia de pesquisa | Orientação própria de cada etapa; escolhas materiais nas áreas técnicas e de experiência exigem comparação pertinente |
| Aproveitar pesquisa e decisões suficientes | [Pesquisa e benchmarking](../pesquisa-e-benchmarking.md) | Reuso com condições verificadas; sem pesquisa de mercado nova para toda correção |
| Aprender com referências de UX/UI | [Pesquisa e benchmarking](../pesquisa-e-benchmarking.md), [etapas 04 e 05](../etapas/04-experiencia-ux.md) | GOV.UK e IBM Carbon como referências possíveis, com adaptação à tarefa e identidade; aparência não comprova desempenho |
| Escolher critérios técnicos aplicáveis | [Fontes](../fontes-de-referencia.md), [etapa 06](../etapas/06-qualidade-e-riscos.md) | WCAG/WAI, ASVS e SSDF com escopo e versão; referência não equivale a conformidade |
| Comparar arquitetura, tecnologia e infraestrutura | [Pesquisa e benchmarking](../pesquisa-e-benchmarking.md), [capítulos técnicos](../../README.md) | Consequências, compatibilidade, origem de dependências, custos, limites e experimentos necessários |
| Conferir saídas de IA | [Verificação com IA](../verificacao-com-ia.md) | Fato, observação, inferência, estimativa e proposta distintos; checagem de fonte e resultado |
| Registrar comparação sem duplicar a fila | [Modelo de comparação](../modelos/comparacao.md), [modelo de pesquisa](../modelos/pesquisa.md) | Comentário ou documento vinculado à decisão e à Issue, com reaproveitamento de registro suficiente |
| Fixar fontes e limites | [Catálogo de referências](../fontes-de-referencia.md) | Doze fontes primárias, edições ou páginas contínuas, afirmação sustentada e limites |
| Transferir incerteza e evidência corretamente | [Governança](../governanca.md), [handoffs](../handoffs.md), [uso com IA](../ferramentas/uso-com-ia.md) | Indicar fonte, versão, verificação e limite sem converter recomendação em resultado comprovado |

## Preservação

Os grupos de pesquisa, experiência, engenharia, arquitetura, tecnologias, infraestrutura e verificações do inventário de origem foram aprofundados, mantendo os destinos de R2 e a governança de R3. As 14 etapas receberam uma seção nova, sem remoção de entradas, atividades, registros, critérios, reaproveitamento ou handoff.

Nos cinco capítulos técnicos, a mudança é uma seção de comparação e evidência antes do retorno ao guia. O conteúdo transferido da origem permanece preservado. Os 15 arquivos do exemplo anterior continuam sem alteração nesta etapa. IDs e rótulos de relatório continuam disponíveis.

O catálogo novo é a entrada corrente das referências de pesquisa e verificação. O arquivo de referências da reorganização preserva o histórico e aponta para ele, sem se apresentar como catálogo concorrente de versões atuais.

## Limites e escolhas deliberadas

- A prioridade de revisão usa impacto, incerteza e possibilidade de detecção no contexto. Não foi criado ranking estatístico de etapas que alucinam mais.
- A tabela de controles é uma adaptação proposta pelo método. As fontes não foram apresentadas como validação empírica desse processo.
- O estudo de pacotes da USENIX sustenta o fenômeno nas condições pesquisadas; seus percentuais não foram extrapolados para o método nem para os modelos atuais de qualquer equipe.
- Referências de padrões não substituem pesquisa com pessoas, avaliação de acessibilidade, testes de segurança, medições ou execução no ambiente.
- Preços e fornecedores não foram escolhidos. A metodologia exige consulta atual ao serviço, plano, versão e região no momento da decisão de cada projeto.
- Um registro curto pode atender uma escolha simples. A adição do modelo não exige novos documentos para toda tarefa nem outro backlog local.

## Verificação e próximo passo

Foram conferidos os 66 arquivos Markdown, 353 links relativos, numeração, campos do registro e YAML dos três templates existentes. Após retirar somente as novas seções de comparação da conferência, os textos das 14 etapas e dos cinco capítulos técnicos coincidem integralmente com R3. Os 15 arquivos do exemplo anterior e os 18 campos do protocolo permanecem preservados.

Foram percorridas documentalmente as instruções para material suficiente reaproveitado, API sem confirmação de versão, preço desconhecido, imagem tratada indevidamente como validação e pesquisa sem resultado de experimento. O catálogo contém doze referências primárias, sem atribuir a elas validação do método.

Esses percursos e a revisão de fontes são documentais. Não equivalem a teste de produto, validação por leitores externos, instalação de habilidades ou operação em outras ferramentas. A conferência remota dos arquivos publicados e os resultados finais ficam na Issue e na PR da entrega.

R5 deve atualizar o exemplo fictício e seus materiais, demonstrar entrada por requisitos existentes, governança de Issues, comparação e handoffs, e consolidar a auditoria de preservação e navegação. Validação externa deve permanecer declarada como pendente até acontecer.

[Continuidade](README.md) · [Inventário](inventario.md) · [Plano](plano.md)
