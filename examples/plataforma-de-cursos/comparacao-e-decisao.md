# Comparação contextual e decisão ilustrativa

> Exercício de preenchimento, sem benchmark executado ou pesquisa do produto. Fontes do método orientam a verificação; não comprovam os resultados deste exemplo.

## Pergunta e contexto

Como estruturar o primeiro Beta para uma equipe pequena, preservando isolamento entre empresas e implantação independente de web e API? A demanda, o volume inferior a 500 usuários e a capacidade da equipe são hipóteses da narrativa. Não usar esses números como medição.

## Alternativas e critérios

| Alternativa | O que avaliar | Evidência disponível neste exemplo |
| --- | --- | --- |
| Adaptar solução existente | Fluxos, permissões, exportação, limites, custo e manutenção | Nenhum produto avaliado; lacuna de pesquisa |
| Aplicação única com módulos definidos | Simplicidade, dependências, isolamento e implantação | Análise conceitual; sem protótipo |
| Monólito modular com web e API separadas | Contratos, operação, autenticação, implantação e esforço de manter duas superfícies | Proposta do exemplo; sem execução |
| Microsserviços | Justificativa de escala, operação, contratos e observabilidade | Necessidade não demonstrada |

Não pontuar desconhecido como zero. Não atribuir pesos ou nota sem critério definido. “Empresa conhecida usa” não comprova adequação. Identificar contexto, direitos e limites da referência; adaptar ao requisito em vez de copiar a solução.

## Referências que orientam o trabalho

- [C4](https://c4model.com/): comunicar estrutura por níveis; diagramas não comprovam segurança ou desempenho.
- [Processo de ADR da AWS](https://docs.aws.amazon.com/prescriptive-guidance/latest/architectural-decision-records/adr-process.html): registrar decisão e consequências; não escolhe a arquitetura do produto.
- [GOV.UK — necessidades](https://www.gov.uk/service-manual/user-research/start-by-learning-user-needs) e [padrões](https://design-system.service.gov.uk/patterns/): orientar perguntas e padrões de interação; adequação à tarefa precisa de avaliação própria.
- [WCAG 2.2](https://www.w3.org/TR/WCAG22/) e [avaliação WAI](https://www.w3.org/WAI/test-evaluate/): definir verificação de acessibilidade; copiar um componente não comprova conformidade.
- [OWASP ASVS](https://asvs.owasp.org/): selecionar requisitos verificáveis de segurança conforme escopo e versão; não é certificado do exemplo.

As fontes foram reunidas no [catálogo do método](../../docs/fontes-de-referencia.md), com seu escopo e limites. Na adoção, registrar data e versão efetivamente consultadas para cada afirmação e artefato; este registro não finge uma nova consulta de versões, preços ou produtos.

## Decisão dentro da narrativa

**ID:** ADR-002. **Responsável:** Ana, com revisão da pessoa responsável pela engenharia. **Estado ilustrativo:** proposta aprovada somente para explorar o desenho do Beta. **Vigência:** planejamento; não autoriza contratar ou publicar. **Evidência:** diálogo fictício em [conversa](conversa-e-decisoes.md), seção 4; nenhuma aprovação externa real.

Explorar monólito modular com web e API separadas. Consequências: contratos e implantação de duas superfícies precisam de manutenção; autorização e isolamento continuam exigindo prova. Microsserviços não têm justificativa demonstrada. A decisão não dispensa comparar uma solução existente antes de comprometer investimento.

## Verificações e condição de revisão

Ainda pendentes: necessidade com usuários, custo total, compatibilidade de versões, comportamento de autorização e prova pequena de implantação. Para UX/UI, avaliar a tarefa com pessoas e teclado; para tecnologias, conferir documentação e executar contrato mínimo; para infraestrutura, verificar conta, região, cotas, dados, recuperação e custos antes da criação.

Rever a decisão se solução existente atender ao recorte, se a equipe não sustentar a operação ou se requisitos novos alterarem os limites. Atualizar a fonte responsável e as Issues; nenhuma referência transforma hipótese em execução.

[Índice](README.md) · [Pesquisa e benchmarking](../../docs/pesquisa-e-benchmarking.md)
