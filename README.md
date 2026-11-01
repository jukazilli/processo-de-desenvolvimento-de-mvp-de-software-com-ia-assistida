# Processo de desenvolvimento de software com apoio de IA

Um guia para transformar ideias ou materiais existentes em software compreensível, verificável e documentado. A IA apoia pesquisa, planejamento, implementação e revisão. As decisões relevantes e a responsabilidade pelo produto pertencem às pessoas que conduzem o projeto.

O processo atende profissionais técnicos que precisam de um caminho claro entre objetivo, requisitos, experiência, arquitetura, tecnologias, infraestrutura e entrega. O produto construído pode ter ou não funcionalidades de IA.

> **Revisão R3:** esta branch contém a entrada, as etapas, a governança incremental e os modelos operacionais. A comparação de referências será aprofundada em R4 e os exemplos completos em R5. [Acompanhar a reorganização](docs/reorganizacao/README.md).

## Comece pelo que você já tem

Leia as [regras do processo](docs/regras-do-processo.md) e faça a [etapa 01](docs/etapas/01-ponto-de-partida.md). Ela avalia as fontes existentes e seleciona o trabalho necessário. Você não precisa refazer decisões suficientes nem pesquisar tudo desde o início.

| Sua situação | Como começar |
| --- | --- |
| Só existe uma ideia | Entenda o problema e reúna evidências na etapa 02 antes de delimitar a proposta |
| Há requisitos, mas falta briefing | Analise os requisitos e suas fontes; use-os na etapa 03 para consolidar objetivo e escopo, esclarecendo as lacunas |
| Há telas, assets ou protótipo | Inventarie os materiais e confira comportamento, identidade e aprovação nas etapas 04–05 |
| Já existe código ou aplicação em operação | Confira o estado atual e as decisões; avance nas etapas afetadas pela mudança |
| Há uma correção pequena em produto documentado | Use a Issue e as fontes afetadas; reaproveite critérios suficientes e execute revisão e validação proporcionais |

Para cada área, registre **suficiente e verificada**, **parcial**, **ausente** ou **não aplicável com justificativa**. Uma etapa pode ser atendida por material existente. O importante é localizar a evidência, identificar o responsável e tornar as lacunas visíveis.

## As 14 etapas

| Etapa | Para que serve |
| --- | --- |
| [01. Escolher o ponto de partida e organizar o projeto](docs/etapas/01-ponto-de-partida.md) | Saber o que já existe, qual resultado se deseja e quais lacunas realmente precisam de trabalho. |
| [02. Entender o problema, os usuários e as evidências](docs/etapas/02-problema-e-evidencias.md) | Entender se vale construir ou alterar a solução e quais necessidades ela deve atender. |
| [03. Definir objetivo, proposta e escopo do produto](docs/etapas/03-objetivo-e-escopo.md) | Explicar o que o produto deve alcançar, para quem e até onde vai a primeira entrega. |
| [04. Mapear jornadas e validar a experiência — UX](docs/etapas/04-experiencia-ux.md) | Explicar como a pessoa realiza uma tarefa, recebe retorno e se recupera de erros ao usar a solução. |
| [05. Definir interface e sistema visual — UI](docs/etapas/05-interface-ui.md) | Transformar contexto e comportamento em uma interface coerente com a identidade e os objetivos do produto. |
| [06. Definir requisitos de qualidade e riscos](docs/etapas/06-qualidade-e-riscos.md) | Tornar explícito o que o sistema precisa suportar e como sua qualidade será verificada. |
| [07. Desenhar a arquitetura da solução](docs/etapas/07-arquitetura.md) | Escolher uma estrutura que atenda às necessidades técnicas com complexidade justificável. |
| [08. Escolher e validar as tecnologias](docs/etapas/08-tecnologias.md) | Definir com quais tecnologias a arquitetura será implementada e quais regras orientam seu uso. |
| [09. Planejar infraestrutura, custos e segurança](docs/etapas/09-infraestrutura.md) | Planejar onde a solução roda, como é operada e quais condições de custo e acesso se aplicam. |
| [10. Organizar o trabalho no GitHub](docs/etapas/10-trabalho-no-github.md) | Transformar decisões em uma fila de trabalho que pessoas e agentes consigam assumir e verificar. |
| [11. Preparar a fundação do projeto](docs/etapas/11-fundacao.md) | Criar ou conferir uma base técnica utilizável para desenvolver, testar e implantar o que foi planejado. |
| [12. Desenvolver por ciclos e entregas pequenas](docs/etapas/12-desenvolvimento-incremental.md) | Implementar mudanças pequenas, verificáveis e coerentes com os objetivos do produto. |
| [13. Validar em pré-produção e liberar](docs/etapas/13-validacao-e-liberacao.md) | Conferir o candidato em condições representativas e liberar uma versão cuja qualidade e limites sejam conhecidos. |
| [14. Operar, aprender e atualizar o produto](docs/etapas/14-operacao-e-aprendizado.md) | Usar evidências de operação e feedback para orientar a evolução do software e do processo. |

As etapas orientam decisões e dependências. Não exigem uma passagem única por todos os documentos. A equipe pode aprender, revisar uma decisão e voltar à etapa correspondente. As etapas 12–14 se repetem conforme a evolução do produto; testes e riscos são planejados desde a etapa 06 e verificados durante o desenvolvimento.

## Como usar com pessoas e ferramentas de IA

Cada atividade identifica objetivo, entradas, trabalho esperado, resultado e critério de conclusão. A transferência para outra pessoa ou ferramenta inclui fontes, versões, decisões, autorizações, evidências, pendências e próximo passo. Veja [como carregar e retomar o processo](docs/ferramentas/uso-com-ia.md) e [as capacidades de apoio](docs/ferramentas/capacidades.md).

O núcleo descreve responsabilidades e resultados. Cada ferramenta confirma suas capacidades, acesso e instruções disponíveis. Habilidades instaladas em uma máquina não são presumidas em outra; compatibilidade efetivamente testada deve ter evidência própria.

## Documentação e trabalho no GitHub

Use documentos para decisões e especificações aprovadas, Issues para o trabalho, PRs para mudanças revisáveis e Projects para acompanhar o andamento quando útil. A documentação é atualizada junto com decisões e entregas; cada informação possui uma fonte oficial indicada pelo projeto.

O backlog principal vive em Issues. Evite uma fila local concorrente em Markdown. Mantenha os vínculos entre requisito, Issue, PR, código, testes e evidência. Um item concluído em pesquisa ou design não comprova implementação nem liberação de software.

Os procedimentos estão nos guias de [governança incremental](docs/governanca.md), [trabalho no GitHub](docs/trabalho-no-github.md) e [handoffs](docs/handoffs.md). Os [modelos reutilizáveis](docs/modelos/README.md) ajudam a registrar o necessário sem criar uma segunda fila.

## Para consultar durante o trabalho

- [Glossário](docs/glossario.md): definições diretas e termos técnicos necessários.
- [Experiência e interface](docs/praticas/experiencia.md): princípios, jornadas e decisões visuais.
- [Padrões de desenvolvimento](docs/praticas/desenvolvimento.md): código, testes e revisão.
- [Engenharia e arquitetura](docs/praticas/arquitetura.md): propriedades, estrutura e limites.
- [Tecnologias](docs/praticas/tecnologias.md): alternativas, compatibilidade e regras de uso.
- [Infraestrutura](docs/praticas/infraestrutura.md): serviços, custo, acesso e preparação.
- [Fontes de referência](docs/reorganizacao/referencias.md): base da revisão; adaptação detalhada por etapa em R4.
- [Exemplo da estrutura anterior](examples/ava-omem/README.md): estudo fictício em atualização para R5, com numeração e operação ainda antigas.

## Como avaliar uma entrega

A entrega deve permitir que outra pessoa entenda o resultado, encontre a decisão que o sustenta e confira a evidência. Qualidade de código, identidade de produto, segurança, custo e operação são avaliados conforme o contexto. O método não transforma uma proposta em decisão, uma imagem em teste ou código existente em liberação comprovada.

Uma equipe pode encerrar em pesquisa ou protótipo se esse for o objetivo. Para software liberado, registrar o que foi implementado, testado, validado no ambiente e efetivamente colocado em operação.
