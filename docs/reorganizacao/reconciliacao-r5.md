# Reconciliação R5: exemplos e auditoria final

> Estado: preparação documental concluída para revisão. Integração das PRs e validação com leitores externos pendentes. A Issue #1 guarda o estado corrente.

## Base e preservação

R5 parte de R4, commit `3032dec85b7ee4ddd3a68e7b5769b931703c732f`, e usa branch `docs/reorganizacao-r5-exemplos`, com base na branch de R4. No início desta entrega, PRs #2–#5 estavam abertas, em rascunho, sem merge; main no commit de origem `12c87840bcb7779e3072eb717814a7bc28c623b8`. Conferir estado e dependências antes de integrar.

Os 29 grupos e os 223 títulos reais de origem continuam inventariados. A [reconciliação R2](reconciliacao-r2.md) associa os grupos aos destinos e justifica alterações de regra; R3 detalha governança e R4 pesquisa. Nesta entrega, as 14 etapas, os cinco capítulos técnicos, regras, governança, modelos e guias de ferramentas permanecem idênticos a R4. Os 18 campos legados de relatório continuam disponíveis. A conferência de estrutura não constitui prova automática de equivalência semântica de cada frase; as mudanças editoriais e operacionais estão registradas nas reconciliações.

## Destino dos 15 arquivos do exemplo

A pasta anterior era um estudo fictício, mas dependia de nomes e integrações particulares. O exemplo atual é uma plataforma de cursos genérica. Os caminhos antigos continuam como encaminhamentos, com link à origem por commit; não há dois contratos atuais concorrentes. Nenhum link existente foi deliberadamente removido.

| Arquivo anterior | Fonte atual | Tratamento |
| --- | --- | --- |
| `README.md` | [README.md](../../examples/plataforma-de-cursos/README.md) | Índice e responsabilidades ligados às 14 etapas; limites declarados. |
| `00_Conversa_Simulada_Discovery_ate_Handoff.md` | [conversa-e-decisoes.md](../../examples/plataforma-de-cursos/conversa-e-decisoes.md) | Diálogo reescrito: entrada flexível, aprovação no escopo e verificação proporcional. |
| `10_Handoff_para_Codex.md` | [handoff-de-execucao.md](../../examples/plataforma-de-cursos/handoff-de-execucao.md) | Transferência portátil: versões, escopo, quatro dimensões e campos não disponíveis. |
| `01_Pesquisa_e_Viabilidade.md` | [problema-e-viabilidade.md](../../examples/plataforma-de-cursos/problema-e-viabilidade.md) | Necessidades, riscos e hipóteses mantidos; conclusão sem pesquisa substituída por recomendação pendente. |
| `02_Briefing_de_Produto_e_Escopo.md` | [objetivo-e-escopo.md](../../examples/plataforma-de-cursos/objetivo-e-escopo.md) | Conteúdo detalhado adaptado para cenário genérico e termos diretos; IDs preservados. |
| `03_Visao_de_Product_Owner.md` | [prioridades-do-produto.md](../../examples/plataforma-de-cursos/prioridades-do-produto.md) | Conteúdo detalhado adaptado para cenário genérico e termos diretos; IDs preservados. |
| `04_Direcao_de_UI_e_Design_System.md` | [interface-e-componentes.md](../../examples/plataforma-de-cursos/interface-e-componentes.md) | Conteúdo detalhado adaptado para cenário genérico e termos diretos; IDs preservados. |
| `05_Especificacao_de_UX.md` | [jornadas-e-comportamento.md](../../examples/plataforma-de-cursos/jornadas-e-comportamento.md) | Conteúdo detalhado adaptado para cenário genérico e termos diretos; IDs preservados. |
| `06_Tecnicas_de_Desenvolvimento.md` | [qualidade-do-codigo.md](../../examples/plataforma-de-cursos/qualidade-do-codigo.md) | Conteúdo detalhado adaptado para cenário genérico e termos diretos; IDs preservados. |
| `07_Engenharia_e_Arquitetura.md` | [arquitetura.md](../../examples/plataforma-de-cursos/arquitetura.md) | Conteúdo detalhado adaptado para cenário genérico e termos diretos; IDs preservados. |
| `08_Backlog_Canonico_Rastreabilidade_e_Plano_de_Entrega.md` | [issues-e-criterios.md](../../examples/plataforma-de-cursos/issues-e-criterios.md) | 29 IDs e critérios mantidos como conteúdo didático para Issues; fila local e cronograma substituídos. |
| `09_Matriz_Operacional_de_Rastreabilidade.md` | [rastreabilidade.md](../../examples/plataforma-de-cursos/rastreabilidade.md) | Matriz manual substituída por vínculos em Issues; estados, aprovações e evidências separados. |
| `Infraestrutura_e_Plano_de_Fundacao.md` | [infraestrutura-e-fundacao.md](../../examples/plataforma-de-cursos/infraestrutura-e-fundacao.md) | Necessidades e critérios preservados; números de preço/cotas e compatibilidade sem execução retirados. |
| `Principios_de_UX_UI.md` | [principios-de-experiencia.md](../../examples/plataforma-de-cursos/principios-de-experiencia.md) | Conteúdo detalhado adaptado para cenário genérico e termos diretos; IDs preservados. |
| `Visao_do_Tech_Lead.md` | [tecnologias.md](../../examples/plataforma-de-cursos/tecnologias.md) | Restrições e IDs preservados; pesquisa de versões não comprovada retirada e substituída por verificações. |

Os IDs DOC-01–DOC-09, TECH-LEAD-VISION, Princípios e Infraestrutura continuam declarados. DOC-05 passa a depender de objetivo e princípios; DOC-04 referencia jornadas antes do detalhe visual, alinhando UX e UI sem renumerar contratos. Chaves técnicas de escopo e nomes de pacotes/comandos permanecem preservados.

## Mudanças e adições justificadas

- **Contexto genérico:** retirada a associação com software ou integração particular. Cursos, empresas, turmas, matrículas, materiais, avaliações, progresso, permissões e certificados continuam no estudo.
- **Critérios preservados:** os 29 IDs FND, AUTH, TEN, CNT, TRL, CLS, LRN, ASM, OBS e CERT mantêm os critérios e dependências de trabalho. Versões específicas deixam de ser apresentadas como atuais; compatibilidade e custos dependem de conferência no projeto adotante.
- **Fila no GitHub:** DOC-08 torna-se catálogo didático de conteúdo para Issues. Ao adotar, publicar e conferir paridade antes de retirar fila anterior; depois manter status somente na fonte operacional. O catálogo não é um backlog ativo deste repositório.
- **Rastreabilidade:** DOC-09 deixa de duplicar status de 29 linhas; demonstra vínculos e as quatro dimensões. Regra, Issue, PR/commit e evidência continuam identificáveis. O cronograma por áreas cede lugar à seleção de incremento verificável nas Issues.
- **Aprovação humana:** preservada com escopo e vigência; retirada exigência de dois comandos quando uma instrução já aprova e autoriza registrar. Campos fictícios nunca representam uma aprovação real.
- **Pesquisa e implantação:** retiradas afirmações de versões, preços, cotas, demanda e compatibilidade não comprovadas neste estudo. Os nomes de tecnologias e fornecedores são exemplos, com verificação pendente. Resultados simulados de execução não são apresentados como evidência.
- **Quatro materiais adicionados:** pontos de partida, governança do exemplo, comparação e decisão, validação e operação. Com os 15 destinos, o estudo possui 19 documentos; as 14 etapas são responsabilidades, não um pacote obrigatório de 14 arquivos.

## Percursos conferidos documentalmente

| Cenário | Caminho nos arquivos | Resultado da revisão |
| --- | --- | --- |
| Ideia inicial | Índice → conversa → problema → objetivo | Hipóteses ficam visíveis; pesquisa pendente não vira viabilidade comprovada |
| Ana tem requisitos sem briefing | Índice → pontos de partida → objetivo/jornadas | Aproveita fontes; complementa lacunas e não exige descoberta do zero |
| Telas ou assets existentes | Pontos de partida → jornadas/interface | Aprovação, direitos e comportamento ausente são conferidos separadamente |
| Produto em operação | Pontos de partida → governança → Issues | Distingue comportamento e decisão; reaproveita fundação suficiente |
| Bug pequeno | Pontos de partida → qualidade → validação | Recorte e verificação proporcionais, sem pesquisa de mercado obrigatória |
| Outra ferramenta ou pessoa assume | Handoff → fontes/aceite → retorno | Versões e acesso não são presumidos; resultados ausentes permanecem ausentes |
| Comparação incompleta | Comparação → tecnologias/infraestrutura | Desconhecido não vira nota, gratuidade, compatibilidade ou autorização |

Esses percursos são leitura e inspeção dos documentos; não houve estudo de usabilidade, leitor externo, execução da aplicação, teste de integração com ferramentas ou configuração de Projects. O cenário de Ana é fictício, sem arquivos pessoais recebidos.

## Resultado das verificações locais

Conferidos 86 arquivos Markdown, 494 links relativos e 15 cabeçalhos YAML (incluindo os três modelos de Issue). As 14 etapas e outros 33 documentos do núcleo coincidem com R4: 47 arquivos inalterados. Há 29 destinos de grupos, 18 campos legados, 29 IDs de atividades com suas listas de aceite e 77 IDs de contratos do exemplo preservados. Os 15 caminhos anteriores apontam para os destinos atuais. A contagem de itens auxilia a revisão e não substitui avaliação semântica ou teste de execução.

## Validação e próximo passo

A conferência cobre links locais, numeração e campos das etapas, cabeçalhos YAML, IDs e critérios dos exemplos, ausência de referências pessoais na apresentação, preservação do núcleo frente a R4 e existência dos destinos dos 29 grupos. O inventário histórico mantém os títulos de origem para rastreabilidade; não os apresenta como nova terminologia.

Revisar as PRs na ordem R1 → R2 → R3 → R4 → R5. Após cada integração, conferir base e diff da dependente. Preparação, revisão, merge e publicação são estados distintos. A integração não foi executada nesta entrega. Depois, colher retorno de leitores técnicos e abrir Issues para dúvidas concretas; somente essa evidência permitirá afirmar validação externa.

[Continuidade](README.md) · [Inventário](inventario.md) · [Plano](plano.md) · [Exemplo atual](../../examples/plataforma-de-cursos/README.md)
