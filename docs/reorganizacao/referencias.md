# Referências para a reorganização

> Histórico de fontes do planejamento e de R3. O [catálogo corrente de pesquisa e verificação](../fontes-de-referencia.md) e a [reconciliação R4](reconciliacao-r4.md) registram a aplicação preparada em R4. Nenhuma lista equivale a certificação ou conformidade integral.

| Fonte primária | Uso previsto | Limite de aplicação |
| --- | --- | --- |
| [GOV.UK — Como funciona a descoberta](https://www.gov.uk/service-manual/agile-delivery/how-the-discovery-phase-works) | Entender o problema antes de comprometer a construção | Adaptar ao porte e ao contexto do projeto |
| [GOV.UK — Aprender sobre usuários e necessidades](https://www.gov.uk/service-manual/user-research/start-by-learning-user-needs) | Aproveitar pesquisa e dados existentes; acompanhar necessidades ao longo do desenvolvimento | Material existente precisa ser avaliado, não aceito automaticamente |
| [GOV.UK — Planejar pesquisa com usuários](https://www.gov.uk/service-manual/user-research/plan-user-research-for-your-service) | Validar hipóteses e considerar usuários com necessidades de acesso | Referências visuais não substituem pesquisa com usuários |
| [W3C — WCAG 2.2](https://www.w3.org/TR/WCAG22/) | Critérios verificáveis de acessibilidade para UX, UI e validação | Conferir critérios aplicáveis e combinar verificação humana e automatizada |
| [AWS — Processo de registros de decisão arquitetural](https://docs.aws.amazon.com/prescriptive-guidance/latest/architectural-decision-records/adr-process.html) | Contexto, alternativas, decisão, consequências e histórico de substituições | Usar para decisões significativas, evitando um registro burocrático por escolha trivial |
| [Google Cloud — Well-Architected Framework](https://docs.cloud.google.com/architecture/framework) | Segurança, confiabilidade, operação, desempenho e custo | Referência de critérios; não torna Google Cloud a escolha do projeto |
| [AWS — Pilares do Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/the-pillars-of-the-framework.html) | Conferir preocupações técnicas e operacionais | Adaptar ao risco e aos recursos disponíveis; não prescrever fornecedor |
| [OWASP — Application Security Verification Standard](https://asvs.owasp.org/) | Requisitos e critérios de verificação de segurança de aplicações | Selecionar versão e requisitos aplicáveis; checklist isolado não comprova segurança |
| [NIST — Perfil de IA generativa, AI 600-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf) | Tratar respostas inventadas, confiança excessiva, proveniência e validação | Não fornece uma taxa universal de alucinação por etapa deste processo |
| [GitHub — Issues e sub-Issues](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/adding-sub-issues) | Hierarquia de trabalho e vínculos rastreáveis | Usar somente a profundidade necessária; conferir permissões e capacidades do ambiente |
| [GitHub — Campos de iteração](https://docs.github.com/en/issues/planning-and-tracking-with-projects/understanding-fields/about-iteration-fields) | Organizar trabalho em períodos recorrentes | Iteração é organização temporal, não aprovação nem prova de entrega |
| [GitHub — Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects) | Visões operacionais sobre Issues e PRs | Não duplicar regras de produto em campos de status |
| [Martin Fowler — Iterações com prazo definido](https://martinfowler.com/bliki/TimeboxedIterations.html) | Distinguir ciclo de trabalho, entrega e fluxo contínuo | Usar a cadência apropriada; não exigir iterações fixas para todo projeto |
| [Agile Alliance — Relato sobre incrementos verticais](https://agilealliance.org/resources/experience-reports/a-tale-of-slicing-and-imagination/) | Explicar entrega de valor que atravessa camadas da solução | É relato de experiência; não prescreve arquitetura nem distribuição de equipe |
| [Scrum Guide — versão oficial](https://scrumguides.org/scrum-guide.html) | Conferir significados de incremento, objetivo e ciclo no contexto Scrum | Usar ideias isoladas não autoriza declarar adoção completa de Scrum |

## Direção de pesquisa registrada no planejamento

Cada comparação relevante deve registrar pergunta, alternativas, critérios, fontes, data de consulta, diferenças de contexto e consequências da escolha. Especificações, versões, APIs, limites e preços devem ser conferidos em documentação oficial atual. Uma citação só sustenta o que a fonte realmente informa.

Benchmarking de produto e padrões é uma comparação de referências. Benchmark de desempenho é uma medição em condições declaradas. Ambos exigem contexto; números de um ambiente ou caso público não podem ser apresentados como medições do projeto.

Para validar necessidade de usuário, usar evidências e pesquisa adequadas. Para validar tecnologia, usar fontes oficiais e experimentos quando necessários. Para validar implementação, usar revisão e testes pertinentes. Para validar disponibilidade, custo real e operação, usar evidência do ambiente. A saída de uma IA ou uma lista de referências não substitui essas comprovações.

## Fontes conferidas na operação de R3

| Fonte primária | Aplicação | Limite |
| --- | --- | --- |
| [GitHub — Templates de Issue e PR](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/about-issue-and-pull-request-templates) | Destino dos templates e cabeçalhos Markdown | Arquivo preparado não comprova seletor renderizado no repositório de destino |
| [GitHub — Configurar templates](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository) | Campos name/about/title e adaptação | Labels, tipos e responsáveis dependem da configuração real; não são presumidos nos modelos |
| [GitHub — Vincular PR e Issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/linking-a-pull-request-to-an-issue) | Referências, palavras de fechamento e branch de destino | Conferir base e configuração; fechamento não equivale a aprovação ou liberação |
| [GitHub — Automação de Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects/automating-your-project/using-the-built-in-automations) | Auditar evento, filtro, ação e efeitos nos estados | Não habilitar Feito por fechamento sem verificar os critérios próprios do projeto |
| [GitHub — Fechamento automático](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/managing-repository-settings/managing-auto-closing-issues) | Conferir configuração de encerramento por merge | Não assumir que todos os repositórios usam os mesmos ajustes |
| [GitHub — Sub-Issues](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/adding-sub-issues) | Hierarquia nativa e sua conferência | Um link textual não cria automaticamente o vínculo de pai e filho |

As fontes sustentam capacidades e funcionamento do GitHub. Os significados de Pronto, Em revisão e Feito são convenções propostas pelo método e precisam ser adotados explicitamente pelo projeto.
