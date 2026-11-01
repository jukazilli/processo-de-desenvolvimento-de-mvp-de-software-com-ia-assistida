# Inventário de preservação

> Estado: origem inventariada e estrutura transferida em R2. Ver os destinos reais e mudanças justificadas na [reconciliação R2](reconciliacao-r2.md). A governança operacional está preparada na [reconciliação R3](reconciliacao-r3.md); benchmarking e verificação estão preparados na [reconciliação R4](reconciliacao-r4.md); exemplos e revisão final continuam em R5.

Origem fixada no commit [`12c87840bcb7779e3072eb717814a7bc28c623b8`](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/tree/12c87840bcb7779e3072eb717814a7bc28c623b8). O README tem 4.181 linhas lógicas, 28 grupos numerados e um grupo técnico principal sem número. Títulos dentro de blocos de exemplo não foram contados como seções reais.

## Como usar este inventário

Cada grupo tem um destino proposto e uma conferência de preservação. Antes de substituir o texto original, ler o trecho no commit fixado, revisar suas regras, condições e exemplos, e registrar o destino real na tabela de reconciliação. A lista de títulos auxilia a cobertura; não substitui a revisão do conteúdo.

## Mapa dos grupos principais

| Origem no README | Natureza | Destino proposto | Conferência necessária |
| --- | --- | --- | --- |
| [1. Propósito](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L7-L46) | Entrada do guia | README e etapa 01 | Reescrever propósito em termos genéricos, mantendo a separação entre apoio de IA e responsabilidade humana. |
| [2. Princípios gerais do processo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L47-L218) | Regras permanentes | Governança; etapa 01; guias de ferramentas | Preservar hipóteses identificadas, aprovação gradual, autorização, versionamento e limites de compatibilidade. Adaptar a autoridade do backlog para Issues. |
| [3. Arquitetura documental inicial](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L219-L245) | Mapa de materiais | Etapa 01 e índice de documentação | Separar número da etapa de nome do arquivo; aproveitar materiais existentes e retirar obrigação de pacote idêntico para todo projeto. |
| [4. Documento 01 — Pesquisa e Viabilidade](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L246-L284) | Etapa | 02 — Problema, usuários e evidências | Preservar viabilidade e distinção entre evidência, hipótese e decisão; permitir entrada por pesquisa já existente. |
| [5. Documento 02 — Briefing de Produto e Escopo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L285-L329) | Etapa | 03 — Objetivo, proposta e escopo | Preservar objetivo, limites, público, proposta, restrições e critérios macro de sucesso. |
| [6. Documento 03 — Visão de Product Owner](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L330-L363) | Etapa | 03 — Direção e prioridades do produto | Preservar princípios de decisão, prioridades e escolhas; esclarecer o responsável sem exigir cargo formal em toda equipe. |
| [7. Princípios de UX/UI](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L364-L522) | Etapa e regra permanente | 04 — UX; aplicação em 05 e 12 | Preservar carga cognitiva, densidade, linguagem do usuário, identidade e critérios avaliáveis. |
| [8. Documento 04 — Direção de UI e Design System](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L523-L599) | Etapa | 05 — Interface e sistema visual | Preservar contexto, hierarquia, tokens, componentes, estados e responsividade; conferir dependência das jornadas de UX. |
| [9. Documento 05 — Especificação de UX](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L600-L679) | Etapa | 04 — Jornadas e experiência | Preservar fluxos, estados, transições, erros, interrupções, acessibilidade e critérios comportamentais. |
| [10. Documento 06 — Técnicas de Desenvolvimento](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L680-L1313) | Regras de engenharia | 06 — Qualidade; aplicação em 08 e 12 | Conferir todos os 17 conjuntos de práticas de código, testes e revisão. Traduzir rótulos sem perder regras, exceções ou padrões técnicos. |
| [11. Documento 07 — Engenharia e Arquitetura](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1314-L1695) | Etapas técnicas | 06 — Qualidade e riscos; 07 — Arquitetura | Separar exigências e estrutura; preservar repositório, alternativas, limites verificáveis, decisões rejeitadas e entradas para tecnologia/infraestrutura. |
| [Visão do Tech Lead — Stack e Implementação Tecnológica](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1696-L2067) | Etapa técnica | 08 — Tecnologias e regras de uso | Numerar a seleção tecnológica; preservar pesquisa atual, compatibilidade, justificativas, alternativas, bibliotecas e contratos de uso. |
| [12. Infraestrutura e Plano de Fundação](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2068-L2491) | Etapa e preparação técnica | 09 — Infraestrutura; 11 — Fundação | Preservar entrevista, comparação, custos, ambientes, automações, credenciais e limites de autorização. Separar plano de execução comprovada. |
| [13. Documento 08 — Backlog Canônico, Rastreabilidade e Plano de Entrega](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2492-L2575) | Planejamento operacional | 10 — Trabalho no GitHub | Transferir a fila para Issues, mantendo objetivo, origem, aceite, dependências, risco, teste e evidência. Preservar IDs históricos quando existirem. |
| [14. Documento 09 — Matriz Operacional de Rastreabilidade](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2576-L2597) | Rastreabilidade | 10, 12 e 13; governança | Preservar vínculos de requisito, código, testes e entrega; evitar uma matriz manual que duplique o estado das Issues. |
| [15. Governança portátil por Skills e Agents](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2598-L2985) | Capacidades de ferramentas | Guia de agentes; governança; 11–14 | Preservar consistência, auditoria, arquitetura, preparação, aprendizado e revisão visual. Explicar capacidades sem exigir habilidades privadas ou instalação presumida. |
| [16. Documentação de segunda geração](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2986-L3022) | Regra documental | Governança; etapas 12–14 | Explicar documentação incremental; preservar criação sob demanda de APIs, dados, segurança, operação e decisões técnicas. |
| [17. Documentação deve se transformar em contrato executável quando possível](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3023-L3081) | Verificação executável | 06, 07, 12 e 13 | Preservar vínculo entre decisão, regra, teste, automação e evidência, incluindo exemplos de limites de acesso e dados. |
| [18. Três níveis de verdade](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3082-L3117) | Autoridade e evidência | Governança; critérios de conclusão | Distinguir produto esperado, solução técnica aprovada e execução observada; não normalizar divergências silenciosamente. |
| [19. Execução pelo Codex](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3118-L3207) | Execução | 11 — Fundação; 12 — Desenvolvimento; 13 — Validação | Preservar leitura das fontes, dependências, preparação, testes e rastreabilidade; usar papel genérico de executor no núcleo. |
| [20. Quality Gates](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3208-L3234) | Verificações | 06 — Estratégia; 12 e 13 — Execução | Preservar verificações aplicáveis de código, segurança, dados, infraestrutura, arquitetura, tecnologias e evidências. |
| [21. Staging como parte da definição de pronto](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3235-L3272) | Validação e liberação | 13 — Pré-produção e liberação | Preservar comprovação em ambiente representativo e identidade do artefato validado; declarar aplicabilidade e limitações. |
| [22. Identidade de produto e prevenção do "visual de IA"](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3273-L3316) | Experiência e identidade | 04 e 05; revisão em 12 | Preservar derivação da interface a partir de contexto, tarefa, jornada e marca, com conferência visual. |
| [23. Estrutura recomendada para documentos canônicos](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3317-L3367) | Modelo de documento | Governança e modelos | Preservar responsabilidade, dependências, estado e Git como histórico; metadados continuam proporcionais à necessidade. |
| [24. Critério de canonização](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3368-L3384) | Aprovação documental | Governança; saída das etapas | Preservar os dez critérios, responsabilidade humana, pendências explícitas e compreensão sem a conversa original. |
| [25. Regra de precedência](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3385-L3424) | Resolução de conflitos | Governança | Preservar resolução por assunto, proibição de alteração silenciosa e necessidade de reconciliação; esclarecer donos e fontes. |
| [26. Processo completo resumido](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3425-L3508) | Visão do fluxo | README e navegação das 14 etapas | Atualizar a visão geral com caminhos de entrada e ciclo de entrega; conferir todos os destinos antes de substituir. |
| [27. Resultado esperado](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3509-L3540) | Resultados esperados | README e etapa 14 | Preservar rastreabilidade, qualidade, identidade, aprendizado e documentação útil; não declarar resultados medidos sem evidências. |
| [28. Ativação da Engine no ChatGPT e handoff para o Codex](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3541-L4181) | Entrada e transferência | 01 — Entrada; guia de uso; guias de ferramentas | Preservar versão das fontes, aprovação gradual, autorização, retomada e contexto de execução; permitir materiais existentes e adaptar instruções à estrutura modular. |

## Títulos reais por grupo

Lista completa até o terceiro nível de títulos Markdown. Os links usam o arquivo de origem, cuja numeração permanece estável mesmo depois da reescrita.

### 1. Propósito

Sem subtítulos reais até o terceiro nível; conferir o texto, listas, tabelas e exemplos do grupo.

### 2. Princípios gerais do processo

- [2.1. A conversa de Discovery não é fonte canônica](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L49) — título de nível 3.
- [2.2. Markdown é o formato canônico](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L76) — título de nível 3.
- [2.3. Cada documento possui uma responsabilidade semântica](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L89) — título de nível 3.
- [2.4. A IA não deve completar lacunas silenciosamente](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L93) — título de nível 3.
- [2.5. Os documentos devem ser gerados e aprovados um por vez](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L104) — título de nível 3.
- [2.6. Onde salvar os documentos do projeto](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L156) — título de nível 3.
- [2.7. Compatibilidade atualmente homologada](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L180) — título de nível 3.

### 3. Arquitetura documental inicial

Sem subtítulos reais até o terceiro nível; conferir o texto, listas, tabelas e exemplos do grupo.

### 4. Documento 01 — Pesquisa e Viabilidade

- [Pergunta central](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L248) — título de nível 2.
- [Objetivo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L252) — título de nível 2.
- [Deve conter](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L256) — título de nível 2.
- [Regra de qualidade](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L271) — título de nível 2.
- [Saída](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L279) — título de nível 2.

### 5. Documento 02 — Briefing de Produto e Escopo

- [Pergunta central](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L287) — título de nível 2.
- [Objetivo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L291) — título de nível 2.
- [Deve conter](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L295) — título de nível 2.
- [Regra de qualidade](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L312) — título de nível 2.

### 6. Documento 03 — Visão de Product Owner

- [Pergunta central](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L332) — título de nível 2.
- [Objetivo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L336) — título de nível 2.
- [Deve conter](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L340) — título de nível 2.
- [Exemplo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L353) — título de nível 2.

### 7. Princípios de UX/UI

- [Pergunta central](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L366) — título de nível 2.
- [Natureza do documento](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L370) — título de nível 2.
- [Eixos obrigatórios](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L378) — título de nível 2.
- [7.1. Baixa carga cognitiva](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L380) — título de nível 3.
- [7.2. Baixa densidade](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L410) — título de nível 3.
- [7.3. Linguagem do usuário](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L423) — título de nível 3.
- [7.4. Comunicação e personalidade da marca](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L445) — título de nível 3.
- [Os princípios devem ser avaliáveis](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L477) — título de nível 2.
- [Papel no processo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L509) — título de nível 2.

### 8. Documento 04 — Direção de UI e Design System

- [Pergunta central](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L525) — título de nível 2.
- [Objetivo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L529) — título de nível 2.
- [Deve conter](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L535) — título de nível 2.
- [Exemplo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L556) — título de nível 2.
- [Relação com o Design System](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L584) — título de nível 2.

### 9. Documento 05 — Especificação de UX

- [Pergunta central](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L602) — título de nível 2.
- [Objetivo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L606) — título de nível 2.
- [Deve conter](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L610) — título de nível 2.
- [Exemplo de jornada](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L630) — título de nível 2.
- [Exemplo de User Story](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L654) — título de nível 2.
- [Distinção entre os três documentos de experiência](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L662) — título de nível 2.

### 10. Documento 06 — Técnicas de Desenvolvimento

- [Pergunta central](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L682) — título de nível 2.
- [Objetivo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L686) — título de nível 2.
- [Deve conter, quando aplicável](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L698) — título de nível 2.
- [10.1. Princípio de legibilidade universal](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L734) — título de nível 2.
- [10.2. Inglês como idioma técnico do código](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L764) — título de nível 2.
- [Exceções](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L806) — título de nível 3.
- [10.3. Naming deve revelar intenção](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L819) — título de nível 2.
- [Funções e métodos](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L823) — título de nível 3.
- [Booleanos](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L846) — título de nível 3.
- [Coleções](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L857) — título de nível 3.
- [Abreviações](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L878) — título de nível 3.
- [10.4. Clean Code é requisito, não preferência estética](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L884) — título de nível 2.
- [10.5. Comentários devem explicar o porquê](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L917) — título de nível 2.
- [10.6. Antes de criar código, procurar o que já existe](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L954) — título de nível 2.
- [Reutilizar não significa forçar abstração](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L988) — título de nível 3.
- [10.7. Duplicação deve ser analisada, não normalizada](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L998) — título de nível 2.
- [10.8. Dependências devem possuir justificativa](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1022) — título de nível 2.
- [10.9. Desempenho deve ser tratado com evidência e responsabilidade](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1038) — título de nível 2.
- [10.10. Tratamento de erros deve ser explícito](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1075) — título de nível 2.
- [10.11. Testes fazem parte da escrita do código](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1104) — título de nível 2.
- [10.12. A IA deve respeitar o estilo existente antes de introduzir um novo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1133) — título de nível 2.
- [10.13. Anti-padrões típicos de código gerado por IA](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1156) — título de nível 2.
- [10.14. Contrato operacional da IA antes de escrever código](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1183) — título de nível 2.
- [10.15. Auto-revisão obrigatória do diff](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1211) — título de nível 2.
- [10.16. Critério de qualidade humana](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1233) — título de nível 2.
- [10.17. Definition of Done mínima para qualidade de código](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1255) — título de nível 2.
- [Regra para agentes](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1275) — título de nível 2.
- [Separação entre Técnicas, Engenharia, Arquitetura e Visão do Tech Lead](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1281) — título de nível 2.

### 11. Documento 07 — Engenharia e Arquitetura

- [Pergunta central](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1316) — título de nível 2.
- [Objetivo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1320) — título de nível 2.
- [Ordem obrigatória de raciocínio](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1324) — título de nível 2.
- [11.1. O que deve ser avaliado primeiro — Engenharia](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1350) — título de nível 2.
- [Produto e escala](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1358) — título de nível 3.
- [Qualidade](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1371) — título de nível 3.
- [Segurança e privacidade](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1384) — título de nível 3.
- [Operação](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1398) — título de nível 3.
- [Evolução](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1409) — título de nível 3.
- [11.2. O que não deve ser escolhido antes dessa análise](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1427) — título de nível 2.
- [11.3. O que pertence à Arquitetura](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1450) — título de nível 2.
- [11.4. Estratégia do repositório é decisão arquitetural](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1478) — título de nível 2.
- [11.5. Escolha do modelo arquitetural](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1536) — título de nível 2.
- [11.6. Comparação antes da decisão](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1573) — título de nível 2.
- [11.7. Fronteiras devem ser verificáveis](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1590) — título de nível 2.
- [11.8. Decisões rejeitadas também devem ser registradas](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1622) — título de nível 2.
- [11.9. Saída obrigatória para a Visão do Tech Lead e para Infraestrutura](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1651) — título de nível 2.
- [Critério de qualidade do Documento 07](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1690) — título de nível 2.

### Visão do Tech Lead — Stack e Implementação Tecnológica

- [Pergunta central](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1698) — título de nível 2.
- [Objetivo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1702) — título de nível 2.
- [Inputs obrigatórios](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1723) — título de nível 2.
- [O que deve definir](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1737) — título de nível 2.
- [Linguagens e runtimes](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1741) — título de nível 3.
- [Frameworks](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1750) — título de nível 3.
- [Bibliotecas canônicas por responsabilidade](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1759) — título de nível 3.
- [Toolchain](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1790) — título de nível 3.
- [Compatibilidade e versões](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1807) — título de nível 3.
- [Pesquisa atual é obrigatória para escolhas materiais](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1823) — título de nível 2.
- [Critérios de seleção](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1852) — título de nível 2.
- [Uma biblioteca por responsabilidade, salvo justificativa](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1897) — título de nível 2.
- [Contratos de uso importam tanto quanto a escolha](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1923) — título de nível 2.
- [Dependências devem ser minimizadas](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1948) — título de nível 2.
- [Tecnologias rejeitadas também devem ser registradas quando a decisão for material](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1965) — título de nível 2.
- [Relação com Infraestrutura](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L1988) — título de nível 2.
- [Saída para Fundação e Backlog](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2020) — título de nível 2.
- [Critério de qualidade da Visão do Tech Lead](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2050) — título de nível 2.

### 12. Infraestrutura e Plano de Fundação

- [Pergunta central](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2070) — título de nível 2.
- [Objetivo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2074) — título de nível 2.
- [12.1. A IA deve entrevistar o humano](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2097) — título de nível 2.
- [Natureza do produto](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2103) — título de nível 3.
- [Estratégia de custo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2114) — título de nível 3.
- [Local versus cloud](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2125) — título de nível 3.
- [Operação](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2150) — título de nível 3.
- [Capacidades](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2158) — título de nível 3.
- [12.2. Pesquisa web atual é obrigatória](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2176) — título de nível 2.
- [12.3. A IA deve comparar alternativas](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2216) — título de nível 2.
- [12.4. Perfil de infraestrutura de referência](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2235) — título de nível 2.
- [12.5. O plano deve mapear a infraestrutura completa](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2251) — título de nível 2.
- [Repositório e entrega](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2255) — título de nível 3.
- [Ambientes](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2265) — título de nível 3.
- [Frontend](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2273) — título de nível 3.
- [Backend/API](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2283) — título de nível 3.
- [Banco de dados](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2293) — título de nível 3.
- [Autenticação](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2306) — título de nível 3.
- [Storage e mídia](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2316) — título de nível 3.
- [Workers, jobs, filas e eventos](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2324) — título de nível 3.
- [Observabilidade](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2334) — título de nível 3.
- [Segurança](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2343) — título de nível 3.
- [Custos](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2353) — título de nível 3.
- [12.6. O plano gera a Fundação — FND](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2361) — título de nível 2.
- [12.7. Automação do setup](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2410) — título de nível 2.
- [12.8. Login e credenciais — humano no circuito](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2435) — título de nível 2.
- [12.9. Custos exigem aprovação explícita](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2475) — título de nível 2.

### 13. Documento 08 — Backlog Canônico, Rastreabilidade e Plano de Entrega

- [Pergunta central](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2494) — título de nível 2.
- [Objetivo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2498) — título de nível 2.
- [Identificadores permanentes](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2502) — título de nível 2.
- [Cada item deve conter](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2514) — título de nível 2.
- [Exemplo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2529) — título de nível 2.
- [Fundação deve aparecer explicitamente no backlog](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2554) — título de nível 2.

### 14. Documento 09 — Matriz Operacional de Rastreabilidade

- [Pergunta central](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2578) — título de nível 2.
- [Objetivo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2582) — título de nível 2.
- [Exemplo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2586) — título de nível 2.

### 15. Governança portátil por Skills e Agents

- [15.1. Skill x Agent](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2616) — título de nível 2.
- [Skill](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2618) — título de nível 3.
- [Agent](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2629) — título de nível 3.
- [15.2. Skill recomendada — `document-consistency`](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2641) — título de nível 2.
- [Objetivo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2643) — título de nível 3.
- [15.3. Skill recomendada — `backlog-evidence-audit`](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2679) — título de nível 2.
- [Objetivo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2681) — título de nível 3.
- [15.4. Skill recomendada — `architecture-conformance`](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2713) — título de nível 2.
- [Objetivo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2715) — título de nível 3.
- [15.5. Skill recomendada — `foundation-readiness`](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2741) — título de nível 2.
- [Objetivo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2743) — título de nível 3.
- [15.6. Skill de aprendizado — `discover-to-skill`](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2772) — título de nível 2.
- [Objetivo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2774) — título de nível 3.
- [Issue como memória operacional](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2840) — título de nível 3.
- [15.7. Skill visual — `visual-reference-to-spec`](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2864) — título de nível 2.
- [Objetivo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2866) — título de nível 3.
- [15.8. Skills complementares](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2917) — título de nível 2.
- [`issue-to-knowledge`](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2919) — título de nível 3.
- [`ui-principles-audit`](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2934) — título de nível 3.
- [15.9. Agents recomendados](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2950) — título de nível 2.
- [`document-steward-agent`](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2952) — título de nível 3.
- [`architecture-review-agent`](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2958) — título de nível 3.
- [`foundation-orchestrator-agent`](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2962) — título de nível 3.
- [`backlog-implementation-agent`](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2966) — título de nível 3.
- [`visual-quality-agent`](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2970) — título de nível 3.
- [`release-audit-agent`](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2974) — título de nível 3.
- [15.10. Regra de portabilidade](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L2978) — título de nível 2.

### 16. Documentação de segunda geração

Sem subtítulos reais até o terceiro nível; conferir o texto, listas, tabelas e exemplos do grupo.

### 17. Documentação deve se transformar em contrato executável quando possível

Sem subtítulos reais até o terceiro nível; conferir o texto, listas, tabelas e exemplos do grupo.

### 18. Três níveis de verdade

Sem subtítulos reais até o terceiro nível; conferir o texto, listas, tabelas e exemplos do grupo.

### 19. Execução pelo Codex

- [Fundação antes das funcionalidades](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3140) — título de nível 2.
- [Fluxo esperado de cada fatia](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3178) — título de nível 2.

### 20. Quality Gates

Sem subtítulos reais até o terceiro nível; conferir o texto, listas, tabelas e exemplos do grupo.

### 21. Staging como parte da definição de pronto

Sem subtítulos reais até o terceiro nível; conferir o texto, listas, tabelas e exemplos do grupo.

### 22. Identidade de produto e prevenção do "visual de IA"

Sem subtítulos reais até o terceiro nível; conferir o texto, listas, tabelas e exemplos do grupo.

### 23. Estrutura recomendada para documentos canônicos

Sem subtítulos reais até o terceiro nível; conferir o texto, listas, tabelas e exemplos do grupo.

### 24. Critério de canonização

Sem subtítulos reais até o terceiro nível; conferir o texto, listas, tabelas e exemplos do grupo.

### 25. Regra de precedência

Sem subtítulos reais até o terceiro nível; conferir o texto, listas, tabelas e exemplos do grupo.

### 26. Processo completo resumido

Sem subtítulos reais até o terceiro nível; conferir o texto, listas, tabelas e exemplos do grupo.

### 27. Resultado esperado

Sem subtítulos reais até o terceiro nível; conferir o texto, listas, tabelas e exemplos do grupo.

### 28. Ativação da Engine no ChatGPT e handoff para o Codex

- [Pergunta central](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3543) — título de nível 2.
- [Objetivo](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3547) — título de nível 2.
- [28.1. Requisito mínimo para ativação](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3555) — título de nível 2.
- [28.2. Fonte canônica da Engine](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3590) — título de nível 2.
- [28.3. Leitura integral antes de qualquer execução](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3618) — título de nível 2.
- [28.4. Fixação da versão durante a sessão](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3640) — título de nível 2.
- [28.5. A ativação não cria documentos](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3665) — título de nível 2.
- [28.6. Handshake de ativação](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3687) — título de nível 2.
- [28.7. Chave de ativação para o ChatGPT](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3714) — título de nível 2.
- [28.8. Primeiro acionamento — Pesquisa e Viabilidade](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3769) — título de nível 2.
- [28.9. Aprovação possui duas fases distintas](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3811) — título de nível 2.
- [28.10. Ciclo obrigatório para os documentos seguintes](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3839) — título de nível 2.
- [28.11. Destino dos documentos do projeto](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3875) — título de nível 2.
- [28.12. Continuidade de sessão](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3906) — título de nível 2.
- [28.13. Atualização ou rotação da chave](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3923) — título de nível 2.
- [28.14. Transição do ChatGPT para o Codex](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3942) — título de nível 2.
- [28.15. Pré-condição local do Codex](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3961) — título de nível 2.
- [28.16. Prompt de bootstrap para o Codex](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L3981) — título de nível 2.
- [28.17. Comando curto para uso recorrente no Codex](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L4027) — título de nível 2.
- [28.18. O Codex deve provar que consumiu antes de executar](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L4045) — título de nível 2.
- [28.19. Quando devolver a decisão para o ChatGPT/humano](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L4066) — título de nível 2.
- [28.20. Integridade entre ChatGPT e Codex](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L4103) — título de nível 2.
- [28.21. Regra para exemplos práticos desta metodologia](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L4137) — título de nível 2.
- [28.22. Resultado esperado da ativação](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md#L4153) — título de nível 2.

## Arquivos existentes

O repositório contém 16 arquivos Markdown no commit de origem. O único exemplo é declarado fictício na sua apresentação. A revisão dos exemplos em R5 precisa atualizar os nomes, links, sequência, critérios de entrada e fonte do backlog; uma cópia das regras antigas em um exemplo também precisa de reconciliação.

| Arquivo de origem | Blob Git | Tratamento previsto |
| --- | --- | --- |
| [README.md](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/README.md) | `a5ac6dc11df6e9f4e5ecacd28173e536d2c476e9` | Entrada acessível e índice das etapas; regras detalhadas com destinos explícitos. |
| [examples/ava-omem/00_Conversa_Simulada_Discovery_ate_Handoff.md](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/examples/ava-omem/00_Conversa_Simulada_Discovery_ate_Handoff.md) | `8a1552c0f44e3846fcbf284896b2cf7154bc2899` | Revisar a conversa fictícia, atualização de fonte, aprovações e entrada por materiais existentes. |
| [examples/ava-omem/10_Handoff_para_Codex.md](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/examples/ava-omem/10_Handoff_para_Codex.md) | `891f21e14b5a32c20a42718feb176dc9f2ea2a55` | Revisar transferência de contexto, ferramentas, permissões, Issues e evidências reais esperadas. |
| [examples/ava-omem/README.md](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/examples/ava-omem/README.md) | `dea93bf37067c65f5a1aea88aeb2ec00d62b9a09` | Atualizar apresentação, navegação e sequência do estudo fictício. |
| [examples/ava-omem/documentos/01_Pesquisa_e_Viabilidade.md](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/examples/ava-omem/documentos/01_Pesquisa_e_Viabilidade.md) | `9b028a2ce16b68f6ca7392b5cc64f2ac68c1dee2` | Conferir regras do documento, renomear e atualizar números e vínculos conforme a etapa correspondente. |
| [examples/ava-omem/documentos/02_Briefing_de_Produto_e_Escopo.md](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/examples/ava-omem/documentos/02_Briefing_de_Produto_e_Escopo.md) | `8996b254fe949a503992546aa7a02ee8f06e1ec0` | Conferir regras do documento, renomear e atualizar números e vínculos conforme a etapa correspondente. |
| [examples/ava-omem/documentos/03_Visao_de_Product_Owner.md](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/examples/ava-omem/documentos/03_Visao_de_Product_Owner.md) | `08c18d08d6807cbd6e864fed632593cd52608198` | Conferir regras do documento, renomear e atualizar números e vínculos conforme a etapa correspondente. |
| [examples/ava-omem/documentos/04_Direcao_de_UI_e_Design_System.md](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/examples/ava-omem/documentos/04_Direcao_de_UI_e_Design_System.md) | `1888ee89bf01740f5d4ac8e453311ad44704141f` | Conferir regras do documento, renomear e atualizar números e vínculos conforme a etapa correspondente. |
| [examples/ava-omem/documentos/05_Especificacao_de_UX.md](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/examples/ava-omem/documentos/05_Especificacao_de_UX.md) | `7200dd56e9f681539b47c9061a8b6a2633989dbd` | Conferir regras do documento, renomear e atualizar números e vínculos conforme a etapa correspondente. |
| [examples/ava-omem/documentos/06_Tecnicas_de_Desenvolvimento.md](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/examples/ava-omem/documentos/06_Tecnicas_de_Desenvolvimento.md) | `2d9cd6d77d42ae73938f9f1cf02d970cdc35634d` | Conferir regras do documento, renomear e atualizar números e vínculos conforme a etapa correspondente. |
| [examples/ava-omem/documentos/07_Engenharia_e_Arquitetura.md](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/examples/ava-omem/documentos/07_Engenharia_e_Arquitetura.md) | `05bb2e9d214242ff0dc406806e528f1bd85afbb4` | Conferir regras do documento, renomear e atualizar números e vínculos conforme a etapa correspondente. |
| [examples/ava-omem/documentos/08_Backlog_Canonico_Rastreabilidade_e_Plano_de_Entrega.md](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/examples/ava-omem/documentos/08_Backlog_Canonico_Rastreabilidade_e_Plano_de_Entrega.md) | `14af8f1d802b534223351fb04c18325d2ff4cfd4` | Reformular como demonstração de Issues, hierarquia, dependências e acompanhamento; retirar fila local concorrente. |
| [examples/ava-omem/documentos/09_Matriz_Operacional_de_Rastreabilidade.md](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/examples/ava-omem/documentos/09_Matriz_Operacional_de_Rastreabilidade.md) | `83b54df733aec9d4b1de196dfb3ba2a5fa0aabfe` | Demonstrar vínculos de rastreabilidade; relatório adicional apenas quando justificado. |
| [examples/ava-omem/documentos/Infraestrutura_e_Plano_de_Fundacao.md](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/examples/ava-omem/documentos/Infraestrutura_e_Plano_de_Fundacao.md) | `433b5c1c016d35e024de865c34b0b5c2cda04bf0` | Conferir regras do documento, renomear e atualizar números e vínculos conforme a etapa correspondente. |
| [examples/ava-omem/documentos/Principios_de_UX_UI.md](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/examples/ava-omem/documentos/Principios_de_UX_UI.md) | `aefd89cb65665a866890b8091d0bac4d6a73d257` | Conferir regras do documento, renomear e atualizar números e vínculos conforme a etapa correspondente. |
| [examples/ava-omem/documentos/Visao_do_Tech_Lead.md](https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida/blob/12c87840bcb7779e3072eb717814a7bc28c623b8/examples/ava-omem/documentos/Visao_do_Tech_Lead.md) | `a4297b54b5632aeb173413c0503c30151e4c67ab` | Conferir regras do documento, renomear e atualizar números e vínculos conforme a etapa correspondente. |

## Pontos que exigem reconciliação explícita

1. Sequência UI/UX e etapas técnicas sem número: atualizar também listas, diagramas, exemplos, dependências e instruções de ativação.
2. Backlog e matriz locais: preservar conteúdo e IDs necessários, transferindo autoridade para Issues e vínculos; não apagar critérios de aceite, dependências, testes ou evidências.
3. Origem ligada a projeto particular: retirar atribuição específica e usar propósito genérico. O histórico Git preserva a proveniência.
4. Fontes de ativação: corrigir endereço do repositório e identificadores exibidos pelo protocolo. Conferir o README e a conversa fictícia.
5. Uso universal da pesquisa inicial: permitir partir de materiais suficientes, verificando apenas lacunas relevantes.
6. Configurações locais e ferramentas: preservar as capacidades necessárias, documentar como confirmar sua disponibilidade e distinguir exemplo de compatibilidade comprovada.
7. Aprovação e entrega: preservar a distinção entre decisão aprovada, trabalho concluído no seu escopo, software testado e versão liberada.
8. Atualização documental: preservar criação sob demanda, histórico de decisões e responsabilidade de cada fonte; evitar novos documentos que dupliquem Issues.

## Registro de reconciliação

Acrescentar uma linha por unidade revisada nas entregas seguintes. A PR deve apontar o commit que contém o destino real e a justificativa de qualquer mudança.

| Unidade | Estado nesta entrega | Evidência ou próximo passo |
| --- | --- | --- |
| Título e propósito inicial | Redação editorial preparada em R1 | Título explícito e propósito genérico; conferir diff da PR |
| Endereço de ativação no README e conversa fictícia | Correção preparada em R1 | Usar o endereço do repositório acessado; conferir ocorrências nas duas fontes |
| Grupos principais e subtítulos | Estrutura transferida e regras reconciliadas em R2 | [Destinos reais e justificativas](reconciliacao-r2.md); governança aprofundada em R3; comparação detalhada preparada em R4 |
| Exemplo fictício e seus documentos | Arquivos e blobs inventariados; revisão de conteúdo pendente | R5; atualização de nomes, sequência e operação do backlog |
| Validação com leitores externos | Pendente | Registrar participantes, critérios e resultados apenas se ocorrer |
