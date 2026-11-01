# Plano de reorganização

> Direção aprovada para iniciar a execução em etapas. Este arquivo descreve a migração; o processo publicado continua sendo o README até a integração das mudanças correspondentes.

## Objetivo e público

Permitir que uma pessoa com conhecimento técnico em desenvolvimento de software entenda e use o processo sem conhecer suas conversas de origem, projetos particulares ou configurações de uma máquina. A IA apoia planejamento, documentação, implementação e verificação; decisões relevantes e aprovações continuam com responsáveis humanos.

Usar linguagem direta. Apresentar a finalidade antes do termo técnico, definir termos necessários e fornecer exemplos fictícios completos. Remover referências de origem vinculadas a projetos particulares. Manter nomes de ferramentas apenas onde ajudam a executar uma instrução específica.

## Regras de preservação

1. Localizar cada seção na versão de origem e atribuir um destino antes de reescrevê-la.
2. Conferir também seus subtítulos, listas, exemplos, exceções e condições de aplicabilidade. Mover um título não comprova preservação das regras.
3. Preservar aprovação humana, distinção entre evidência e hipótese, limites de autorização, rastreabilidade e verificações proporcionais ao risco.
4. Registrar qualquer regra alterada, fundida ou removida com origem, justificativa, destino e impacto. Não excluir conteúdo apenas para encurtar o guia.
5. Separar guia de uso, regras permanentes, modelos e instruções de ferramentas. Numerar as etapas do trabalho com uma sequência única.
6. Evitar duas fontes oficiais para a mesma informação. Ao mudar a autoridade de um arquivo para uma Issue, registrar a transição e conferir vínculos.
7. Aprovar e registrar decisões em unidades revisáveis. Uma instrução humana pode aprovar o conteúdo e autorizar seu registro ao mesmo tempo quando isso for explícito.
8. Usar as autorizações já dadas para executar o escopo aprovado. Nova aprovação é necessária quando uma escolha altera produto, custo, risco ou escopo além dessa autorização.

## Entregas da reorganização

| Entrega | Conteúdo | Critério de conclusão |
| --- | --- | --- |
| R1 — Inventário e continuidade | Versão de origem, mapa de conteúdo, glossário, referências e este plano; correções editoriais iniciais | Todos os grupos e títulos reais do README e os 15 exemplos identificados; diferenças limitadas e verificadas; PR com checkpoint |
| R2 — Guia e etapas | Entrada pelo estado atual; 14 etapas numeradas; linguagem acessível; destinos da documentação técnica | Cada etapa informa objetivo, entradas, atividades, saída, critério de conclusão e condições para reaproveitar ou não aplicar; conteúdo original reconciliado |
| R3 — Governança e transferência de contexto | Documentação incremental; Issues, sub-Issues, Projects e PRs; decisão oficial; modelos e instruções para agentes | Um colaborador consegue assumir uma Issue sem depender da conversa; cada informação tem autoridade definida; não há backlog local concorrente |
| R4 — Pesquisa, comparação e verificação | Benchmarking por etapa; fontes atuais; alternativas; prevenção e detecção de erros de IA | Decisões relevantes têm evidências e justificativas; critérios de pesquisa e validação definidos; exemplos não inventam dados de usuário, preços ou compatibilidade |
| R5 — Exemplos e revisão final | Atualização dos exemplos; casos de entrada; links; numeração; cobertura das regras e revisão editorial | Toda origem tem destino conferido ou mudança justificada; exemplos seguem o método; limitações e validações externas pendentes declaradas |

Cada entrega usa branch e PR próprias. Se depender de uma PR ainda não integrada, indicar a dependência e a base real, ou manter a continuidade no mesmo rascunho de forma explícita. Não abrir uma branch da `main` antiga e descartar trabalho não integrado.

## Estrutura prevista do método

Os nomes e caminhos finais serão implementados em R2. Esta tabela define a sequência e as responsabilidades; as etapas podem ser revisitadas conforme o aprendizado.

| Etapa | Nome | Entrega esperada |
| --- | --- | --- |
| 01 | Escolher o ponto de partida e organizar o projeto | Inventário de materiais, responsáveis, fontes oficiais, restrições, permissões e caminho de entrada |
| 02 | Entender o problema, os usuários e as evidências | Problema, público, pesquisa disponível, dúvidas, hipóteses e avaliação de viabilidade |
| 03 | Definir objetivo, proposta e escopo do produto | Briefing, valor esperado, prioridades, limites e critérios de sucesso |
| 04 | Mapear jornadas e validar a experiência — UX | Princípios de experiência, necessidades, fluxos, estados, acessibilidade e plano de validação |
| 05 | Definir interface e sistema visual — UI | Hierarquia, telas, componentes, identidade, referências e estados visuais |
| 06 | Definir requisitos de qualidade e riscos | Segurança, privacidade, desempenho, operação, práticas de código e estratégia de testes |
| 07 | Desenhar a arquitetura da solução | Estrutura, módulos, dados, integrações, limites e decisões com alternativas |
| 08 | Escolher e validar as tecnologias | Linguagens, frameworks, bibliotecas, ferramentas, versões e regras de uso |
| 09 | Planejar infraestrutura, custos e segurança | Ambientes, fornecedores, limites, credenciais, custos, implantação e recuperação |
| 10 | Organizar o trabalho no GitHub | Issues e sub-Issues, dependências, critérios de aceite, prioridades e ciclos quando úteis |
| 11 | Preparar a fundação do projeto | Repositório e ambiente configurados, automações e primeira implantação técnica verificável |
| 12 | Desenvolver por ciclos e entregas pequenas | Implementação de itens prontos, revisão, testes e documentação atualizada |
| 13 | Validar em pré-produção e liberar | Verificações, evidências, aprovação de liberação e plano de retorno |
| 14 | Operar, aprender e atualizar o produto | Monitoramento, feedback, incidentes, aprendizado e novos itens de trabalho |

As etapas 12–14 formam um ciclo recorrente. Um novo aprendizado pode reabrir uma decisão anterior por revisão explícita. O método deve permitir ciclos com prazo definido ou fluxo contínuo; não chamar o processo de Scrum apenas por usar iterações.

Princípios, formatos, verificações e instruções de ferramentas ficam identificados como regras ou guias de apoio. Conteúdos centrais de experiência, tecnologia e infraestrutura pertencem às etapas numeradas correspondentes, sem etapas escondidas em complementos.

## Entrada por materiais existentes

A etapa 01 faz uma análise do que já existe. Cada área recebe uma situação: suficiente e verificada; parcial; ausente; não aplicável com justificativa. Registrar fonte, data/versão, responsável, evidência de aprovação e lacunas.

| Situação de entrada | Caminho a demonstrar |
| --- | --- |
| Ideia inicial | Entender problema e público, pesquisar e delimitar a primeira proposta |
| Requisitos existentes sem briefing | Ler requisitos e materiais de origem; esclarecer lacunas; construir ou validar o briefing a partir deles |
| Telas, assets ou protótipo | Inventariar materiais; distinguir aparência, comportamento e hipóteses; confirmar regras com o responsável |
| Código ou aplicação em operação | Auditar estado atual, documentação e evidências; distinguir comportamento observado de decisão aprovada; planejar lacunas e mudanças |

Reaproveitar evidências reduz retrabalho. Material existente não comprova automaticamente sua atualidade ou aprovação. Não reabrir pesquisa já suficiente; investigar lacunas relevantes. Uma etapa pode aproveitar artefatos existentes e concluir sem produzir um documento novo.

Registrar a justificativa de uma etapa não aplicável. Identificação de fontes, avaliação de riscos aplicáveis, critérios de aceite e evidências proporcionais à entrega continuam necessárias. Um estudo pode encerrar antes de implantação se esse for seu objetivo declarado.

## Modelo de documentação e trabalho

Definir na etapa 01 onde cada informação tem autoridade. O modelo principal a desenvolver em R3 é:

| Informação | Local e responsabilidade |
| --- | --- |
| Decisões gerais aprovadas | README do produto ou índice curto que aponta para documentos oficiais; não duplicar o conteúdo |
| Regras detalhadas e documentos técnicos | Markdown versionado, criado conforme a necessidade; decisões arquiteturais importantes em registros próprios |
| Detalhes de tela mantidos em Issue | Uma Issue responsável, com índice explícito para contratos e comentários aprovados; informar essa autoridade no índice do produto |
| Proposta, pesquisa, tarefa, bug e histórico | Issue com escopo, fontes, critérios de aceite, pendências e evidências |
| Andamento e agrupamento por ciclo | GitHub Projects; status operacional não substitui aprovação de decisão |
| Alteração em código, documentos e assets | Branch e PR vinculadas à Issue; revisão e evidências |
| Rastreabilidade | Vínculos entre decisão/requisito, Issue, PR, código, teste e evidência; relatório adicional só quando houver necessidade real |

O backlog vive em Issues. Um arquivo de tarefas exportado pode ser uma cópia datada para consulta, nunca uma segunda fila editada em paralelo. Sem acesso ao GitHub, preparar material para importação e declarar que a fila ainda não está publicada; não alegar operação sincronizada.

Documentação incremental significa atualizar a informação oficial conforme as decisões são aprovadas e o comportamento é comprovado. Discutir uma proposta não a torna regra. Fechar uma Issue, mesclar uma PR, aprovar um visual e liberar software representam estados distintos.

## Modelo de transferência de contexto

Cada etapa e Issue pronta para execução devem informar: objetivo e limites; responsável; repositório, branch e versões; entradas e decisões aprovadas; hipóteses; evidências; dependências; critérios de aceite; ações autorizadas; resultados esperados; riscos e pendências.

O executor confirma quais fontes leu e quais capacidades tem disponíveis. Ao terminar, registra arquivos/commits, ações realmente executadas, verificações realizadas e não realizadas, resultados, pendências e próximo passo. Um resumo de conversa serve como orientação, acompanhado das fontes oficiais acessíveis.

O núcleo será escrito por responsabilidades. Guias específicos podem explicar como transferir contexto para ChatGPT, Codex, Gemini ou outra ferramenta, sem presumir que habilidades locais foram instaladas ou lidas automaticamente em outro ambiente. Não afirmar compatibilidade homologada sem evidência de execução.

## Pesquisa e comparação

R4 deve incluir comparação proporcional ao impacto nas etapas de produto, UX/UI, engenharia, arquitetura, tecnologias e infraestrutura. Registrar pergunta, critérios, alternativas, fontes, contexto, limites, escolha, consequências e data. Usar fontes primárias para especificações técnicas, preços, limites, APIs e versões.

Benchmarking não elimina erros de IA e não comprova adequação ao projeto. Pesquisas, protótipos, testes, medições e revisão especializada complementam as referências. A priorização de revisão por risco é contextual; não alegar um ranking estatístico universal de etapas em que modelos alucinam mais.

## Verificação de cada entrega

- Comparar alterações com o inventário e conferir regras, condições e exceções migradas.
- Conferir numeração, nomes, glossário, links e consistência entre guia e exemplos.
- Buscar referências a projetos particulares no texto publicado e removê-las de modo rastreável.
- Confirmar que o backlog tem uma fonte e que etapas/documentos não foram confundidos.
- Percorrer os casos de entrada descritos acima usando os arquivos reais do guia.
- Registrar a natureza de cada verificação. Uma revisão editorial ou simulação documental não equivale a validação por usuários externos, teste de software ou execução em ferramentas de terceiros.
- Atualizar o checkpoint e a Issue; publicar uma PR com escopo e limitações compreensíveis sem esta conversa.
