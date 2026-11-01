# Reconciliação da estrutura em R2

> Estado: nova estrutura preparada e conferida editorialmente. Integração e revisão externa pendentes. A Issue #1 controla o andamento da reorganização.

Esta entrega parte do commit de R1 `667a7668ea1761879ae6e05bb7d4716d7ff74f79`. A origem histórica continua sendo `12c87840bcb7779e3072eb717814a7bc28c623b8`. A PR de R2 usa como base a branch de R1 enquanto ela não estiver integrada; isso preserva o inventário e evita repetir suas alterações no diff da nova entrega.

## Como o conteúdo foi transferido

O README passou a apresentar os caminhos de entrada e o índice de 14 etapas. Cada etapa possui objetivo, entradas, atividades, registros, critério de conclusão, regras de reaproveitamento e transferência para a próxima atividade. A numeração das etapas não obriga renomear documentos ou IDs de projetos existentes.

Os capítulos de experiência, desenvolvimento, arquitetura, tecnologias, infraestrutura e capacidades de ferramentas preservam o detalhamento original, com atualização de termos e referências. Eles aprofundam as etapas e não representam etapas adicionais. As regras gerais foram consolidadas em um capítulo comum. A ativação e a continuidade foram reescritas para funcionar com essa navegação e com materiais já disponíveis.

## Destinos dos 29 grupos principais

O [inventário](inventario.md) mantém os links exatos para a origem e seus títulos. Esta tabela aponta para os arquivos reais desta entrega.

| Grupo de origem | Destino em R2 | Conferência e tratamento |
| --- | --- | --- |
| 1 — Propósito | [README](../../README.md) | Propósito genérico e responsabilidade humana; apoio de IA no processo explicitado |
| 2 — Princípios gerais | [Regras](../regras-do-processo.md), [uso com IA](../ferramentas/uso-com-ia.md), [etapa 01](../etapas/01-ponto-de-partida.md) | Aprovação gradual, hipóteses, autorização, fontes, versão e limitações preservadas; escolhas de entrada e formato adaptadas |
| 3 — Arquitetura documental inicial | [README](../../README.md), [etapa 01](../etapas/01-ponto-de-partida.md) | Substitui o pacote obrigatório de nomes por responsabilidades e materiais suficientes; IDs existentes permanecem válidos |
| 4 — Pesquisa e viabilidade | [Etapa 02](../etapas/02-problema-e-evidencias.md) | Problema, público, alternativas, evidências, viabilidade, riscos e decisão de seguir ou não |
| 5 — Briefing e escopo | [Etapa 03](../etapas/03-objetivo-e-escopo.md) | Objetivo, público, valor, escopo, exclusões, restrições e sucesso; aceita requisitos existentes |
| 6 — Direção do produto | [Etapa 03](../etapas/03-objetivo-e-escopo.md) | Prioridades e princípios de decisão integrados à definição do produto |
| 7 — Princípios de UX/UI | [Etapa 04](../etapas/04-experiencia-ux.md), [experiência](../praticas/experiencia.md) | Detalhes de carga cognitiva, densidade, linguagem e personalidade preservados |
| 8 — Direção de UI | [Etapa 05](../etapas/05-interface-ui.md), [experiência](../praticas/experiencia.md) | Contexto, tarefa, informações, ações, hierarquia, padrões visuais e estados preservados |
| 9 — Especificação de UX | [Etapa 04](../etapas/04-experiencia-ux.md), [experiência](../praticas/experiencia.md) | Jornadas, estados, validações, falhas, interrupções e acessibilidade; sequência ajustada para UX antes do detalhe de UI |
| 10 — Técnicas de desenvolvimento | [Etapa 06](../etapas/06-qualidade-e-riscos.md), [etapa 12](../etapas/12-desenvolvimento-incremental.md), [desenvolvimento](../praticas/desenvolvimento.md) | Os 17 tópicos de práticas foram preservados, com suas listas, exemplos e exceções; não reduzidos a um checklist curto |
| 11 — Engenharia e arquitetura | [Etapa 06](../etapas/06-qualidade-e-riscos.md), [etapa 07](../etapas/07-arquitetura.md), [arquitetura](../praticas/arquitetura.md) | Engenharia separada da escolha estrutural; nove conjuntos de orientações e suas condições preservados |
| Escolha tecnológica sem número | [Etapa 08](../etapas/08-tecnologias.md), [tecnologias](../praticas/tecnologias.md) | Etapa numerada; linguagens, bibliotecas, ferramentas, pesquisa, compatibilidade, alternativas e contratos de uso |
| 12 — Infraestrutura e fundação | [Etapa 09](../etapas/09-infraestrutura.md), [etapa 11](../etapas/11-fundacao.md), [infraestrutura](../praticas/infraestrutura.md) | Plano separado da execução; entrevista, serviços, custos, automação, credenciais e nove conjuntos de orientações preservados |
| 13 — Backlog | [Etapa 10](../etapas/10-trabalho-no-github.md), [regras](../regras-do-processo.md) | Fila passa a Issues; origem, objetivo, aceite, dependências, risco, testes, evidência e status preservados por responsabilidade |
| 14 — Matriz de rastreabilidade | [Etapa 10](../etapas/10-trabalho-no-github.md), [etapa 13](../etapas/13-validacao-e-liberacao.md), [regras](../regras-do-processo.md) | Vínculos de requisito, implementação, teste e evidência; relatório adicional só quando necessário, sem estado duplicado |
| 15 — Habilidades e agentes | [Capacidades](../ferramentas/capacidades.md), [uso com IA](../ferramentas/uso-com-ia.md) | Preserva descrições de capacidades, aprendizado recorrente e revisão visual; não presume instalação local |
| 16 — Documentação de segunda geração | [Regras](../regras-do-processo.md), [etapa 14](../etapas/14-operacao-e-aprendizado.md) | Documentação incremental, criação sob demanda e assuntos técnicos preservados |
| 17 — Contrato executável | [Regras](../regras-do-processo.md), [etapa 06](../etapas/06-qualidade-e-riscos.md), [etapa 13](../etapas/13-validacao-e-liberacao.md) | Decisão traduzida em regra verificável, teste e evidência; exemplos técnicos também preservados nos capítulos de arquitetura e tecnologia |
| 18 — Níveis de verdade | [Regras](../regras-do-processo.md) | Expectativa de produto, solução aprovada e comportamento comprovado continuam distintos |
| 19 — Execução | [Etapa 11](../etapas/11-fundacao.md), [etapa 12](../etapas/12-desenvolvimento-incremental.md), [etapa 13](../etapas/13-validacao-e-liberacao.md) | Preparação, leitura, menor mudança coerente, testes, revisão, evidência e liberação; executor genérico no núcleo |
| 20 — Verificações obrigatórias | [Etapa 06](../etapas/06-qualidade-e-riscos.md), [etapa 13](../etapas/13-validacao-e-liberacao.md), [regras](../regras-do-processo.md) | Verificações de código, segurança, dados, infraestrutura, arquitetura, tecnologias e documentos conforme aplicabilidade |
| 21 — Pré-produção | [Etapa 13](../etapas/13-validacao-e-liberacao.md) | Candidato validado, evidência de ambiente e promoção do mesmo artefato; ausência de pré-produção exige condição substituta explícita |
| 22 — Identidade de produto | [Etapa 05](../etapas/05-interface-ui.md), [regras](../regras-do-processo.md), [capacidades](../ferramentas/capacidades.md) | Interface derivada de contexto, jornada, tarefa e marca; referências não aprovam implementação automaticamente |
| 23 — Estrutura de documentos | [Regras](../regras-do-processo.md) | Metadados úteis e opcionais preservados por função; o exemplo YAML foi consolidado na descrição de campos, sem impor um modelo único |
| 24 — Aprovação oficial | [Regras](../regras-do-processo.md), [uso com IA](../ferramentas/uso-com-ia.md) | Responsabilidade, hipóteses, limites, coerência, independência da conversa, pendências, versão e aprovação humana |
| 25 — Precedência | [Regras](../regras-do-processo.md) | Autoridade por assunto e revisão explícita de conflitos; comportamento em execução não reescreve intenção silenciosamente |
| 26 — Fluxo resumido | [README](../../README.md) | Índice de 14 etapas, caminhos de entrada e ciclo recorrente; etapas e documentos distinguidos |
| 27 — Resultado esperado | [README](../../README.md), [etapa 14](../etapas/14-operacao-e-aprendizado.md) | Software compreensível, verificável e operável; aprendizado e evolução documental |
| 28 — Ativação e transferência | [Uso com IA](../ferramentas/uso-com-ia.md), [etapa 01](../etapas/01-ponto-de-partida.md) | Versão, leitura comprovada, entrada por materiais, autorização, destino, sincronização, impedimentos e checkpoint; rótulos antigos de relatório preservados para compatibilidade |

## Mudanças de regra justificadas

| Regra ou formato anterior | Tratamento novo | Motivo e limite |
| --- | --- | --- |
| Pesquisa inicial como partida universal | Avaliação de materiais e lacunas | Reaproveitar fontes suficientes sem inventar sua aprovação; etapa 01 permanece a entrada comum |
| Sequência numerada de documentos com complementos | Sequência única de 14 etapas; documentos por responsabilidade | Tornar tecnologia e infraestrutura visíveis; evitar exigir renomeação de arquivos já consumidos por ferramentas |
| UI detalhada antes da UX | Jornadas na etapa 04, interface na 05, com revisões possíveis | Esclarecer o comportamento que a tela suporta; não impedir trabalho conjunto ou revisão de hipóteses |
| Backlog oficial e matriz editável em Markdown | Issues como fila; vínculos rastreáveis; Projects opcional | Evitar duas filas e status conflitantes. Templates e operação serão detalhados em R3; exemplos antigos ficam identificados até R5 |
| Uma leitura monolítica obrigatória do README inteiro | README, regras e conjunto completo dos capítulos relevantes à tarefa | Controlar volume de contexto preservando leitura integral das fontes aplicáveis. Informar o escopo real; não alegar leitura completa do método após ler apenas partes |
| Dependência do fluxo específico de duas ferramentas e planos pagos | Núcleo por capacidades, com conferência de acesso e limites | Permitir uso por outras equipes sem alegar homologação geral. A integração com ferramentas e habilidades existentes será revisada em R3 |
| Ativação em uma conversa de descoberta como único caminho | Carregamento por tarefa e fontes existentes | Manter o vínculo com decisões e evidências quando a entrada for requisito, protótipo ou código |
| Dois comandos de aprovação quando o significado já era explícito | Conteúdo e registro podem ser autorizados na mesma instrução | Preservar decisão humana e respeitar autorização já concedida, com novos limites decididos quando necessário |
| Protocolo com rótulos em inglês | Registro simples em português, com rótulos anteriores documentados | Preservar compatibilidade de prompts e habilidades sem obrigar novos leitores a aprendê-los |

## Exemplos e limites desta entrega

Os 15 arquivos do estudo fictício continuam preservados. Apenas sua apresentação recebeu um aviso da estrutura anterior e um link para a entrada nova. Eles ainda usam números, documentos e backlog antigos, que serão tratados em R5. Não apresentá-los como demonstração já atualizada.

R2 cria etapas e preserva orientações técnicas; não instala habilidades nem atualiza instruções externas de máquinas ou ferramentas. R3 detalhará governança, templates e integração. R4 aprofundará referências e comparação por etapa. R5 verificará a consistência final e atualizará os exemplos.

As verificações desta entrega são documentais. Navegação válida e preservação de conteúdo não comprovam validação por leitores externos ou uso de ponta a ponta em outro ambiente. Registrar essas validações apenas quando ocorrerem.

[Continuidade](README.md) · [Plano](plano.md)
