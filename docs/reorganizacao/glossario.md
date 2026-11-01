# Glossário para a revisão editorial

> Estado: propostas de vocabulário para R2–R5. Os termos abaixo orientam a redação; nomes de arquivos, identificadores técnicos e comandos precisam ser adaptados com seus consumidores.

Usar a expressão mais direta no texto principal. Quando um termo técnico ajuda a pesquisar ou conversar com a área, apresentá-lo entre parênteses na primeira ocorrência. Evitar traduzir de modo que se perca uma distinção técnica importante.

| Expressão atual | Redação preferida ou explicação | Cuidado na revisão |
| --- | --- | --- |
| Engenharia de IA | Desenvolvimento de software com apoio de IA | O método trata do uso de IA no processo de desenvolvimento; o produto pode ter ou não recursos de IA |
| Engine | Protocolo de uso do processo, ou simplesmente processo | Reservar nomes de configuração a instruções específicas de ferramenta |
| Bootstrap / chave de ativação | Instrução inicial para carregar o processo | É uma instrução de texto, não uma credencial |
| Discovery | Entendimento do problema e pesquisa inicial | Pode aproveitar evidências existentes; não pressupõe começar do zero |
| Discovery Freeze | Aprovação das decisões de uma etapa | Decisões podem ser revistas com registro explícito |
| Canônico / fonte da verdade | Oficial ou fonte oficial, após explicar quem aprova | Não transformar uma proposta em decisão só por salvar um arquivo |
| Canonizar | Aprovar e registrar como decisão oficial | Aprovação e autorização de registro podem ocorrer na mesma instrução explícita |
| Baseline | Base de decisões e materiais aprovados | Informar a versão e o escopo; não exigir pacote completo para toda mudança |
| Briefing | Visão resumida do produto | Explicar problema, público, proposta, objetivo e escopo |
| Visão do Product Owner | Direção e prioridades do produto | Preservar princípios de decisão e responsabilidades do responsável pelo produto |
| Princípios de UX/UI | Princípios de experiência | Manter regras avaliáveis e seus efeitos sobre escolhas de interface |
| UX | Experiência de uso | Inclui necessidades, jornadas, estados, erros e acessibilidade |
| UI | Interface e sistema visual | Inclui elementos, hierarquia, componentes e estados visuais |
| Design System | Sistema de padrões visuais e componentes | Não determina sozinho a tarefa e o contexto de uma tela |
| Tarefa mental | Objetivo principal do usuário naquele momento | Descrever a tarefa concreta no exemplo |
| Técnicas de Desenvolvimento | Práticas e padrões de desenvolvimento | Preservar regras de legibilidade, testes, segurança e manutenção |
| Visão do Tech Lead | Escolha das tecnologias e regras de uso | A liderança técnica é o papel responsável; o documento descreve decisões |
| Stack | Conjunto de tecnologias | Diferenciar arquitetura, ferramentas e ambiente de execução |
| Toolchain | Ferramentas de desenvolvimento e automação | Versões e compatibilidade precisam de fonte e verificação |
| Boundary | Limite entre módulos, sistemas ou áreas de confiança | Dizer qual limite e como ele é verificado |
| Setup / Fundação / FND | Preparação inicial do projeto | Se `FND-*` já for identificador de trabalho, preservar histórico e vínculos |
| Fatia / slice | Entrega pequena e verificável | Se incluir capacidade de ponta a ponta, explicar incremento vertical |
| Incremento vertical | Entrega funcional de ponta a ponta | Pode envolver interface, lógica e dados; não confundir com arquitetura vertical |
| Iteração | Ciclo de trabalho com prazo definido | É um período de organização; não é sinônimo de incremento |
| Fluxo contínuo | Execução ordenada sem ciclos com prazo fixo | Pode ser usado quando adequado, com revisão frequente do trabalho |
| Iteration-driven / driven development | Evitar como rótulo novo para este método | Não trocar uma expressão informal por outra ambígua |
| Backlog canônico em Markdown | Fila de trabalho em GitHub Issues | Documento de escopo e fila operacional têm funções distintas |
| Matriz operacional de rastreabilidade | Vínculos de requisito, trabalho, implementação e evidência | Relatório adicional apenas se houver necessidade; evitar atualização duplicada |
| Handoff | Transferência de contexto e responsabilidade | Informar entradas, versões, pendências, resultado esperado e critério de conclusão |
| Pick-up / Ready | Pronto para alguém assumir | Depende de fontes acessíveis, escopo, dependências e aceite suficientes |
| Quality gate | Verificação obrigatória para avançar | Explicar o critério e a evidência, além do nome da ferramenta |
| Definition of Done | Critérios de conclusão | Distinguir conclusão de pesquisa, design, implementação e liberação |
| Staging | Ambiente de pré-produção | Explicar o quanto representa o ambiente real e suas limitações |
| Promoção | Liberação da versão validada no ambiente seguinte | Registrar artefato ou commit; evitar recriar um candidato diferente sem validar |
| Rollback | Retorno a uma versão anterior | Mudanças em dados podem exigir recuperação própria, não só retorno do código |
| Runtime | Comportamento e ambiente de execução | Distinguir o que é esperado do que foi observado |
| ADR | Registro de decisão arquitetural | Contexto, alternativas, decisão, consequências, responsável e estado |
| Runbook | Guia operacional de uma tarefa ou incidente | Precisa de instruções executáveis no contexto e limites de autorização |
| Skill | Habilidade reutilizável de uma ferramenta de IA | Não presumir presença, execução ou portabilidade automática |
| Agent | Agente de IA responsável por uma tarefa | Descrever capacidades necessárias e limites de ação |
| Checkpoint | Registro de continuidade | Gravar estado real, fontes, pendências e próximo passo no repositório |
| Benchmarking | Comparação estruturada de referências e alternativas | Diferenciar comparação de produto/padrões de medição de desempenho |

## Exemplo da distinção entre ciclo e entrega

Uma equipe usa ciclos de uma semana. No ciclo atual, pretende permitir que o usuário salve um endereço de entrega e o consulte depois. Essa capacidade é um incremento funcional, envolvendo formulário, regras de validação e persistência. O ciclo é o período; o incremento é o resultado. Tarefas técnicas de preparação e pesquisa também podem existir, com seus próprios critérios de conclusão.

## Como aplicar o glossário

Revisar a frase inteira em vez de fazer substituições cegas. Um `gate` pode ser um critério de aprovação ou uma automação; um `boundary` pode envolver arquitetura ou segurança. Manter nomes de APIs, bibliotecas, identificadores e termos de código quando a tradução quebraria o contrato técnico. Explicar o contexto em português e conferir exemplos e links após renomear arquivos.
