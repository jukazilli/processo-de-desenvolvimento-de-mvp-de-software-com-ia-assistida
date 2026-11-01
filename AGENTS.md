# Instruções para manter este repositório

Este repositório contém um método de desenvolvimento de software e seus exemplos. As instruções abaixo orientam sua manutenção; os modelos em `framework/modelos/` são materiais para adaptação em outros projetos.

## Antes de editar

Ler `README.md`, `framework/regras-do-processo.md`, `framework/governanca.md` e os capítulos afetados. Durante a reorganização, ler também a Issue #1, `docs/reorganizacao/README.md`, o plano, inventário e reconciliações pertinentes. Conferir branch, commit, PRs e dependências ainda não integradas. Não presumir que a `main` contém os rascunhos.

Identificar o escopo solicitado e as autorizações já concedidas. Executar o trabalho autorizado sem repetir confirmações; encaminhar escolhas novas que alterem produto, custo, risco ou escopo além dessa autorização. Não mesclar, publicar ou mudar configurações externas sem autorização aplicável.

## Preservação e clareza

Manter linguagem direta para leitores técnicos sem contexto prévio. Separar etapas, documentos, regras e instruções de ferramentas. Preservar IDs e contratos usados por consumidores; registrar origem, destino e justificativa ao alterar uma regra. Exemplos devem ser explicitamente fictícios; não atribuir o método a projetos particulares.

Manter uma fonte oficial por assunto e Issues como fila. Documentação, estado operacional, aprovação e evidência de execução são informações diferentes. Não alegar validação por usuários, instalação de habilidades, configuração de Projects ou execução de software sem prova correspondente.

Ao acrescentar afirmação técnica material, consultar fonte primária apropriada, identificar versão/condições e registrar o limite do que foi conferido. Seguir `framework/pesquisa-e-benchmarking.md` e `framework/verificacao-com-ia.md`. Comparação e revisão documental não devem ser apresentadas como experimento ou validação externa.

## Verificar e transferir

Conferir coerência com as regras existentes, navegação e links relativos, numeração, termos, modelos e exemplos afetados. Para templates, verificar formato e instruções de adaptação. A verificação documental não comprova funcionamento da interface do GitHub ou adoção em outras ferramentas.

Ao terminar um recorte, registrar arquivos/commits, evidências, verificações realizadas e pendentes, conflitos e próximo passo na Issue e no checkpoint pertinente. Preservar trabalho local e branches não integradas; conferir a base de uma PR dependente antes de integrá-la.

## Separação entre framework, explicação e produto

Manter o README como entrada operacional única para a IA, com ativação e contratos das 14 etapas. Regras e modelos complementares ficam em `framework/`; `docs/` explica propósito, adoção, revisão e histórico. Páginas de etapas em docs apontam para o contrato do README, sem segunda lista de execução. Não inserir inventário de migração ou estado de PR no ponto de ativação.

O padrão de saída é `docs/PROJETO.md` no repositório do produto, com seções revisáveis, fontes e continuidade. Este repositório fornece apenas o modelo e exemplos fictícios. Conferir que entradas curtas iniciam análise, que materiais existentes são aproveitados e que nenhuma etapa promete persistência, aprovação ou execução inexistentes. Preservar caminhos antigos como referências aos destinos e conferir links, anchors, campos e compatibilidade ao alterá-los.
