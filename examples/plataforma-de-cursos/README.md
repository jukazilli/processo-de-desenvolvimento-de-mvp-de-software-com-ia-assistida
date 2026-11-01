# Exemplo: plataforma de cursos

> **Estudo fictício, versão 2.0.** Demonstra o método, sem aplicação implementada, entrevistas, aprovações de terceiros, Issues do produto, testes ou serviços implantados. “Aprovado” nos diálogos significa apenas uma decisão dentro da narrativa. O [guia e suas regras](../../README.md) orientam o método.

Uma consultoria quer organizar cursos, turmas, materiais, avaliações, progresso e certificados para empresas que treinam seus funcionários. Os cursos podem ensinar um software corporativo; não dependem de marca ou integração específica. Há administrador, instrutor, gestor restrito à própria empresa e aluno.

## Relação com a saída incremental

Este estudo anterior mantém documentos separados para preservar seus IDs e demonstrar aproveitamento de materiais existentes. Para uma adoção nova, o padrão é um único `docs/PROJETO.md` do produto. O índice pode referenciar estes materiais sem duplicar suas regras até uma migração explícita. O [exemplo de ativação e saída única](../ativacao/README.md) demonstra o contrato atual.

## Escolha um percurso

- **Projeto novo:** [conversa e decisões](conversa-e-decisoes.md), análise do problema e definição do primeiro resultado.
- **Ana já tem requisitos, telas e materiais:** [entrada por materiais existentes](pontos-de-partida.md). Consolidar o objetivo a partir deles e pesquisar somente lacunas.
- **Já há código em operação ou um bug pequeno:** [percursos proporcionais](pontos-de-partida.md), sem reconstruir toda a fundação.
- **Outra pessoa ou IA vai assumir:** [handoff de execução](handoff-de-execucao.md), com entradas, limites e próximo passo conferíveis.

## Fontes e relação com as etapas

Os arquivos são exemplos de fontes por assunto. Seus nomes e IDs de documentos não são números de etapas. DOC-01 a DOC-09, TECH-LEAD-VISION e os IDs de requisitos foram preservados como demonstração de compatibilidade; não é necessário renomear documentos existentes para adotar o método.

| Etapa do método | Fonte didática responsável pelo assunto |
| --- | --- |
| 01 — Ponto de partida | [Materiais e percursos](pontos-de-partida.md), [governança](governanca-do-exemplo.md) |
| 02 — Problema e evidências | [Problema e viabilidade — DOC-01](problema-e-viabilidade.md) |
| 03 — Objetivo e escopo | [Objetivo — DOC-02](objetivo-e-escopo.md), [prioridades — DOC-03](prioridades-do-produto.md) |
| 04 — UX | [Jornadas — DOC-05](jornadas-e-comportamento.md), [princípios](principios-de-experiencia.md) |
| 05 — UI | [Interface — DOC-04](interface-e-componentes.md) |
| 06 — Qualidade e riscos | [Qualidade — DOC-06](qualidade-do-codigo.md), requisitos ENG da arquitetura |
| 07 — Arquitetura | [Arquitetura — DOC-07](arquitetura.md) |
| 08 — Tecnologias | [Tecnologias — TECH-LEAD-VISION](tecnologias.md) |
| 09 — Infraestrutura | [Infraestrutura e fundação](infraestrutura-e-fundacao.md), parte de planejamento |
| 10 — Trabalho no GitHub | [Issues e aceite — DOC-08](issues-e-criterios.md), [vínculos — DOC-09](rastreabilidade.md) |
| 11 — Fundação | [Critérios FND das Issues](issues-e-criterios.md), [handoff](handoff-de-execucao.md) |
| 12 — Desenvolvimento incremental | [Seleção do incremento](issues-e-criterios.md), [qualidade](qualidade-do-codigo.md) |
| 13 — Validação e liberação | [Verificação, liberação e operação](validacao-e-operacao.md) |
| 14 — Operação e aprendizado | [Verificação, liberação e operação](validacao-e-operacao.md), retorno de evidências à Issue |

A [comparação e decisão](comparacao-e-decisao.md) atravessa as áreas conforme o impacto da escolha. A [governança](governanca-do-exemplo.md) define autoridade e atualização incremental; o [handoff](handoff-de-execucao.md) transfere uma atividade, sem depender de uma máquina específica.

## O que permanece pendente

Necessidade e viabilidade comercial, fornecedores, versões, custos, acessibilidade e segurança efetivamente verificadas, implementação e liberação. As tabelas descrevem o que conferir, sem substituir a execução. Use os [modelos do método](../../docs/modelos/README.md) para adaptar o registro ao projeto real.

## Termos usados nos documentos técnicos

**Tenant** é a empresa cujo acesso precisa ficar isolado; **adaptador** conecta a regra de negócio a um serviço externo; **port** é o contrato dessa conexão; **runtime** executa o programa; **lockfile** fixa dependências; **CI** executa verificações automatizadas; **E2E** testa a jornada completa; **staging** é pré-produção. Termos em código e IDs continuam iguais para não quebrar exemplos e consumidores. Veja também o [glossário do método](../../docs/glossario.md).

**AVA/LMS** significa plataforma de aprendizagem. **Beta** é a versão inicial de avaliação. O exemplo usa esses termos para contextualizar o produto; não exige uma fase Beta em toda adoção.
