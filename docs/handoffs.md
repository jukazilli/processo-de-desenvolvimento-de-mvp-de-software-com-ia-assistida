# Transferir contexto e responsabilidade

Um handoff permite que outra pessoa ou ferramenta continue o trabalho com fontes acessíveis, limites e próximo passo claros. O registro curto aponta para o detalhe oficial; não precisa copiar o histórico inteiro da conversa.

## Antes de transferir

Conferir objetivo, escopo, responsável pelo aceite, decisões vigentes, fontes, versões, autorizações e dependências. Preparar o [modelo de handoff](modelos/handoff.md), adaptando o detalhe ao risco. Se o trabalho for continuar com a mesma pessoa após uma pausa, o [checkpoint](modelos/checkpoint.md) pode bastar.

| Parte | O que o próximo executor precisa saber |
| --- | --- |
| Tarefa e limites | Issue, resultado esperado, critérios de aceite e o que fica fora |
| Fontes | Repositório, documentos, decisões, comentários aprovados e assets, com versões ou commits pertinentes |
| Situação do trabalho | Branch, base da PR, alterações locais/não integradas e dependências |
| Estado real | Andamento, aprovação, estado da Issue/PR e comprovação de implementação/QA separados |
| Autorizações | Ações já autorizadas e limites de custo, acesso, publicação e mudança |
| Evidências | O que foi observado, executado e testado; condições, resultados e links seguros |
| Pendências | Dúvidas, conflitos, riscos, fontes indisponíveis e condição para desbloquear |
| Próximo passo | Ação concreta, fontes a conferir, resultado e verificação esperados |

Registrar o handoff na Issue responsável ou num documento de continuidade apontado por ela. Evitar dois registros ativos editados em paralelo. Em cada retomada, conferir o estado atual antes de confiar no resumo anterior.

## Ao receber

1. Ler a tarefa, o handoff e as instruções aplicáveis. Conferir repositório, branch, versões e trabalho não integrado antes de editar.
2. Ler o README, regras do processo e o conjunto completo de etapas, práticas e fontes pertinentes. Seguir vínculos de dependência; não presumir que o índice contém as regras detalhadas.
3. Conferir decisões e evidências, separando aprovação de aparência, implementação, testes e operação. Informar fontes inacessíveis e limitações que afetem o próximo passo.
4. Confirmar o que será executado dentro da autorização existente. Se houver lacuna relevante fora desse escopo, apresentar impacto e alternativas ao responsável, continuando partes independentes já autorizadas.
5. Executar e atualizar o registro com o resultado real. Um texto dizendo que uma verificação foi feita não substitui sua evidência.

## Entre planejamento e execução

O planejamento entrega objetivo, decisões, versões, Issue pronta, dependências e aceite. O executor confere a preparação técnica e o código existente antes de implementar. Mudança de arquitetura, tecnologia, comportamento ou custo além da autorização retorna ao responsável com contexto e alternativas.

Ao terminar o recorte, o executor entrega PR/commit, documentos alterados, evidências, verificações e próximo passo. A revisão confere o aceite e a consistência. A liberação recebe o candidato identificado, condições do ambiente, mudanças de dados, riscos e plano de retorno.

## Entre ChatGPT, Codex, Gemini e outras ferramentas

Transferir responsabilidades e fontes, não uma memória presumida. Confirmar que a ferramenta consegue ler o repositório, as Issues, os assets e os capítulos necessários; verificar habilidades, instruções e comandos realmente disponíveis. Uma ferramenta sem acesso a Projects não pode afirmar que conferiu ou alterou o quadro.

O [modelo de instruções para agentes](modelos/instrucoes-para-agentes.md) pode ser adaptado ao mecanismo reconhecido pelo ambiente. Alguns ambientes consultam arquivos por convenção; outros exigem instrução explícita. A presença de um arquivo ou checklist não comprova leitura. Registrar as fontes consumidas e uma conferência concreta do contrato da tarefa.

Para adaptar instruções existentes: inventariar seus arquivos e consumidores; mapear nomes antigos para as responsabilidades atuais; preservar IDs e rótulos enquanto houver dependência; fazer uma mudança revisável; verificar no ambiente de destino; registrar limitações. Não alegar que habilidades locais foram atualizadas por publicar um modelo neste repositório.

Os [rótulos anteriores de relatório](ferramentas/uso-com-ia.md) permanecem disponíveis para compatibilidade. Não há obrigação de usar um plano pago ou ferramenta específica para ler o método; a execução depende de capacidades, acesso e verificação adequados.

## Controlar o volume de contexto

Manter checkpoint curto com a próxima ação, fontes e estado verificável. Encerrar um recorte com evidência antes de trocar de contexto. Não reduzir um contrato importante a um resumo se o executor precisa de suas exceções e condições; indicar o documento completo e carregar as partes dependentes.

Marcar o que foi lido. Leitura integral de fontes aplicáveis à tarefa pode ser relatada como escopo da tarefa; só declarar leitura completa do método se todos os materiais correspondentes forem realmente consumidos. Se uma janela for insuficiente, dividir em recortes com checkpoints, sem inventar continuidade.

## Informações sensíveis e impedimentos

Transferir instruções de acesso e nomes de variáveis necessários, sem expor valores de segredos. Evitar dados pessoais ou registros sensíveis em comentários públicos. Para ação humana necessária, descrever o painel ou mecanismo, o que fazer e qual evidência segura permite continuar.

Se uma fonte essencial estiver ausente, indicar exatamente qual, o que ela impede e o que ainda pode ser feito. Não declarar conformidade, aprovação ou execução sem conseguir conferi-las.

[Governança](governanca.md) · [Modelos](modelos/README.md) · [Voltar ao guia](../README.md)
