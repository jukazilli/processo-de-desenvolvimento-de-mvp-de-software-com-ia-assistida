# Continuidade da reorganização

> Estado: R1 preparada para revisão. A estrutura nova ainda será implementada nas etapas seguintes.

Este registro permite retomar o trabalho pelo repositório, mesmo que a conversa ou o ambiente de execução mudem. O trabalho é acompanhado na [Issue #1](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/issues/1). A Issue controla o andamento; esta pasta guarda o plano, as decisões de organização e a evidência do inventário.

## Ponto de partida fixado

- Repositório: `jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida`.
- Branch de origem: `main`.
- Commit de origem: [`12c87840bcb7779e3072eb717814a7bc28c623b8`](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/tree/12c87840bcb7779e3072eb717814a7bc28c623b8).
- Blob do README original: `a5ac6dc11df6e9f4e5ecacd28173e536d2c476e9`.
- Branch desta entrega: `docs/reorganizacao-r1-inventario`.
- Escopo encontrado: README com 4.181 linhas lógicas e 15 arquivos Markdown de exemplo. A versão original continua disponível no commit acima.

## O que foi preparado em R1

- [Plano de execução](plano.md): cinco entregas com critérios de conclusão, dependências e estrutura de 14 etapas do método.
- [Inventário](inventario.md): origem e destino proposto de todos os grupos e títulos do README, mais os 15 arquivos de exemplo.
- [Glossário de revisão](glossario.md): termos a simplificar e termos técnicos que precisam de definição.
- [Referências](referencias.md): fontes externas do planejamento e limites de sua aplicação.
- Ajustes editoriais restritos no README: título mais explícito, descrição genérica do propósito, link para esta continuidade e correção do endereço usado na ativação.
- Correção do mesmo endereço no exemplo de conversa. O conteúdo e a numeração desse exemplo ainda precisam da revisão R5.

## Estado de preservação

O inventário marca destinos como **propostos**. Isso comprova que o conteúdo foi localizado; não comprova que cada regra já foi transferida para a estrutura nova. A conferência de regras, exemplos, links e exceções será feita em cada entrega e consolidada em R5.

R1 não afirma que leitores externos validaram a metodologia, que o processo foi executado em outras ferramentas ou que existe uma configuração de GitHub Projects para esta reorganização.

## Verificações de R1

- Os 16 conteúdos de origem foram conferidos com seus hashes de blob Git; os hashes coincidem com o inventário remoto.
- Foram identificados 29 grupos principais e 223 títulos reais até o terceiro nível, excluindo títulos escritos dentro de blocos de exemplo.
- Foram conferidos os links relativos dos cinco documentos desta pasta e o link de entrada pelo README.
- O diff dos arquivos preexistentes foi revisado: somente o README e a fonte de ativação na conversa fictícia receberam os ajustes editoriais listados acima.
- Uma busca pelos nomes de projetos particulares conhecidos não encontrou ocorrências no Markdown atual da branch após o ajuste de propósito.
- A disponibilidade de todos os links externos não foi verificada novamente nesta entrega. A migração semântica completa e a validação por leitores externos continuam pendentes.

## Próximo passo: R2

1. Consultar a Issue #1, esta continuidade, o plano e o inventário.
2. Conferir se a PR de R1 foi integrada ou se existe uma branch de continuação; preservar o trabalho ainda não integrado.
3. Conferir diferenças da `main` em relação ao commit de origem. Se o conteúdo de origem mudou, reconciliar a mudança no inventário antes de reescrever.
4. Implementar a entrada do guia e as 14 etapas numeradas, com caminhos para projeto novo, materiais existentes, protótipo e software já em operação.
5. Migrar as seções por grupo, conferindo seus subtítulos e regras. Atualizar o destino real e a evidência no inventário.
6. Usar o glossário como orientação editorial; preservar identificadores e comandos que funcionem como contratos técnicos até adaptar seus consumidores.
7. Atualizar esta continuidade com arquivos alterados, verificações feitas, pendências e próximo passo, e publicar uma PR revisável.

## Questões já identificadas

- Etapa não equivale a documento: um documento pode ser atualizado em vários ciclos; uma etapa pode aproveitar materiais existentes sem gerar um arquivo novo.
- UX deve esclarecer jornadas antes do detalhamento de UI. Princípios de experiência são definidos e validados nessas etapas e continuam aplicáveis depois.
- A governança começa na entrada e acompanha o trabalho inteiro. A etapa 10 refina e organiza o backlog para execução.
- O backlog do método novo terá autoridade em Issues; o arquivo local de backlog e a matriz paralela devem ser substituídos por vínculos rastreáveis, com exceções justificadas para necessidades específicas.
- As etapas 12 e 13 se repetem a cada entrega. Planejar testes começa na etapa 06; testar não fica adiado até o fim.
- Instruções específicas para ferramentas terão guias próprios. Cada ferramenta precisa confirmar as capacidades disponíveis; configurações e habilidades locais não são presumidas em outro ambiente.
- O exemplo existente é declarado fictício. Sua revisão deve retirar dependências de contexto particular, atualizar os nomes e demonstrar também uma entrada com materiais já disponíveis.

## Ao encerrar qualquer entrega

Registrar na Issue e na PR: escopo realmente concluído; arquivos e commits; regras preservadas ou substituídas com justificativa; evidências; verificações não executadas; pendências; próxima entrega. Não marcar o método completo como concluído enquanto houver conteúdo sem destino conferido.
