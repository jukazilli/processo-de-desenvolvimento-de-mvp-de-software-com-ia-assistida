# 12. Desenvolver por ciclos e entregas pequenas

**Objetivo:** Implementar mudanças pequenas, verificáveis e coerentes com os objetivos do produto.

## Entradas

- Issue pronta, decisões e critérios de aceite acessíveis.
- Fundação suficiente para o item ou exceção aprovada com limites claros.

## Como realizar

1. Selecionar o item priorizado e conferir fontes, versões, dependências, escopo autorizado e padrões locais.
2. Procurar código e componentes equivalentes antes de criar funções, tipos, arquivos ou dependências novos.
3. Implementar a menor mudança coerente. Para funcionalidades, preferir capacidade de ponta a ponta, incluindo as camadas necessárias; pesquisa e preparação têm resultados próprios.
4. Criar ou atualizar os testes pertinentes, revisar o próprio diff e executar verificações aplicáveis de código, segurança, arquitetura e tecnologias.
5. Atualizar documentação afetada e vínculos da Issue e da PR na mesma entrega. Registrar hipóteses e decisões novas como propostas até sua aprovação.
6. Registrar resultados, erros e impedimentos. Se uma descoberta altera escopo ou decisão relevante, apresentar o impacto ao responsável antes de ampliar a mudança.

## O que registrar

- PR pequena e revisável, vinculada à Issue.
- Código, documentos e testes coerentes, com evidências e limitações.
- Candidato identificado por commit ou artefato para validação.

## Critério de conclusão

A mudança satisfaz o aceite no escopo proposto, respeita os padrões, foi revisada e possui evidência das verificações. A liberação depende da etapa 13 quando aplicável.

## Aproveitar ou não aplicar

A equipe pode usar ciclos com prazo ou fluxo contínuo. Uma iteração é o período de trabalho; um incremento é a capacidade entregue. Não chamar a entrega de “fatia” sem explicar seu resultado.

## Transferência para a próxima atividade

Transferir o candidato, mudanças de dados, evidências e plano de verificação à etapa 13. O que falta concluir permanece rastreado, mesmo ao terminar um ciclo.

## Orientação detalhada

Consultar o capítulo de [padrões de desenvolvimento](../praticas/desenvolvimento.md) para as regras e exemplos aplicáveis. Esse capítulo aprofunda a etapa; ele não cria uma etapa adicional.

Aplicar as [regras do processo](../regras-do-processo.md). O formato do registro pode ser um documento, Issue ou atualização de material existente, conforme a fonte oficial escolhida para o assunto. O número da etapa não obriga criar um arquivo com esse número.

---

[Voltar ao guia](../../README.md) · [Etapa anterior](11-fundacao.md) · [Próxima etapa](13-validacao-e-liberacao.md)
