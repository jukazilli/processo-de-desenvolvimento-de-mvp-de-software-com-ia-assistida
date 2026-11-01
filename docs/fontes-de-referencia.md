# Fontes para pesquisa, comparação e verificação

Este catálogo registra a base consultada em R4 em 31/10/2026. As fontes ajudam a escolher perguntas e critérios; o uso de uma referência não declara conformidade ou certificação do método ou do produto. Os procedimentos operacionais são adaptações propostas para desenvolvimento com apoio de IA.

| Fonte primária | Tipo e versão de referência | O que sustenta | Limite de uso |
| --- | --- | --- | --- |
| [NIST AI 600-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf) | Perfil de risco de IA generativa, julho de 2024 | Confabulação, confiança excessiva, integridade e verificação de fontes | Não mede este processo nem fornece ranking universal de alucinação por etapa |
| [GOV.UK — Usuários e necessidades](https://www.gov.uk/service-manual/user-research/start-by-learning-user-needs) | Guia contínuo de pesquisa | Evidências existentes, pesquisa com usuários e necessidades ao longo do desenvolvimento | Contexto de serviço público; adaptar ao projeto e não inventar pesquisa realizada |
| [GOV.UK Design System — Patterns](https://design-system.service.gov.uk/patterns/) | Padrões documentados por tarefa e página | Referências de solução de interação e adaptação ao contexto | Não prova demanda ou desempenho do produto que consulta o padrão |
| [IBM Carbon — Componentes](https://www.carbondesignsystem.com/building-blocks/core/components/overview/components) | Documentação contínua de design system | Referências de componentes e consistência de interface | Não obriga usar seus componentes, identidade ou densidade |
| [W3C — WCAG 2.2](https://www.w3.org/TR/WCAG22/) | Critérios de acessibilidade, edição 2.2 | Critérios verificáveis de acessibilidade | Selecionar escopo e avaliação apropriados; citar não comprova conformidade |
| [W3C/WAI — Avaliação](https://www.w3.org/WAI/test-evaluate/) | Guia contínuo de avaliação | Combinação de ferramentas e avaliação humana | Ferramenta isolada não determina acessibilidade integral |
| [OWASP ASVS](https://asvs.owasp.org/) | Padrão comunitário; versão 5.0.0 apresentada na consulta | Requisitos e base para verificação de segurança de aplicações | Fixar versão e requisitos usados; identificadores podem mudar entre edições |
| [NIST SP 800-218](https://csrc.nist.gov/pubs/sp/800/218/final) | SSDF versão 1.1, fevereiro de 2022 | Práticas de desenvolvimento seguro integráveis ao ciclo de vida | Não é prova de segurança do produto nem uma prescrição única de arquitetura |
| [AWS — Processo de ADR](https://docs.aws.amazon.com/prescriptive-guidance/latest/architectural-decision-records/adr-process.html) | Guia contínuo de decisões arquiteturais | Contexto, alternativas, consequências e histórico de substituições | Adaptar às decisões significativas; não escolher fornecedor por causa da fonte |
| [C4 — Fonte oficial](https://c4model.com/) | Modelo de comunicação de arquitetura | Abstrações e diagramas para explicar a estrutura | Não escolhe uma arquitetura de implementação nem exige todos os diagramas |
| [Google Cloud Well-Architected](https://docs.cloud.google.com/architecture/framework) | Framework contínuo de arquitetura e operação em nuvem | Critérios como segurança, confiabilidade, custo, desempenho e operação | Adaptar ao contexto; não comprova preços, limites ou configuração de uma conta |
| [Spracklen et al. — USENIX Security 2025](https://www.usenix.org/conference/usenixsecurity25/presentation/spracklen) | Pesquisa empírica sobre pacotes inventados em geração de código | Evidência do fenômeno nos modelos, linguagens e cenários avaliados | Não extrapolar seus percentuais para este método ou para todos os modelos atuais |

## Como manter uma referência útil

Na decisão do projeto, registrar a página ou edição realmente consultada e a afirmação que ela sustenta. Páginas contínuas podem mudar; usar versões, releases, commits ou trechos identificáveis quando necessários à reprodução da decisão. Uma versão adotada não deve ser confundida com a versão mais recente em qualquer data futura.

Revalidar informação mutável quando apoiar contratação, instalação, migração ou outra ação relevante. Para preços e limites, consultar o serviço, plano e região concretos; este catálogo não substitui essa pesquisa. Para implementação, consultar a documentação correspondente à versão instalada.

Uma fonte pode estar inacessível ou insuficiente. Registrar isso e buscar outra fonte primária apropriada ou planejar validação; não declarar o conteúdo conferido apenas porque seu título ou link foi encontrado. Preferir links originais e respeitar condições de uso de textos, marcas e assets.

As referências de operação do GitHub ficam no [guia correspondente](trabalho-no-github.md); o [registro histórico da reorganização](reorganizacao/referencias.md) preserva as fontes das entregas anteriores.

[Pesquisa e benchmarking](pesquisa-e-benchmarking.md) · [Verificação com IA](verificacao-com-ia.md) · [Voltar ao guia](../README.md)
