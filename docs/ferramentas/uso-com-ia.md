# Carregar, executar e retomar o processo com IA

Este guia permite transferir contexto entre pessoas, conversas, máquinas e ferramentas. Consultar os procedimentos de [handoff](../handoffs.md), a [governança](../governanca.md) e os [modelos reutilizáveis](../modelos/README.md). Uma habilidade local só pode ser usada quando a ferramenta confirmar sua disponibilidade e instruções.

## Identificar fontes e versão

A fonte do método é este repositório. Identificar repositório, branch e commit carregados quando o acesso permitir. O README é a entrada; as regras gerais e etapas aplicáveis contêm instruções adicionais. Ler integralmente os materiais necessários à tarefa, seguindo seus vínculos e condições. Se uma fonte essencial não estiver acessível, informar a limitação antes de alegar conformidade.

A seleção dos capítulos depende do estado do projeto: não basta ler só o índice ou presumir que um resumo contém todas as regras. Identificar e carregar o conjunto completo relevante à tarefa, incluindo práticas técnicas, decisões e Issues afetadas. Declarar quais fontes foram realmente lidas. Não alegar leitura integral de arquivos que não foram consumidos.

Manter a versão do método durante uma atividade. Se o responsável solicitar atualização, carregar a nova versão e reconciliar diferenças antes de continuar. Para decisões do produto, consultar também o estado atual de suas fontes oficiais e registrar os commits efetivamente usados.

## Entrada pelo que já existe

Aceitar ideia, conversa, requisitos, pesquisa, telas, assets, protótipo ou código como entrada. Aplicar a etapa 01 para identificar materiais suficientes e lacunas. A conversa anterior pode fornecer contexto, mas hipóteses não se tornam requisitos sem aprovação.

Carregar o processo, sozinho, não autoriza produzir todos os documentos, implementar o produto ou publicar alterações. Identificar a tarefa solicitada, escopo autorizado e próximo passo. Quando o responsável já aprovou e autorizou uma ação, executar dentro desse escopo sem pedir a mesma confirmação de novo.

## Instrução inicial adaptável

```text
Use o processo em:
https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida

Leia o README, as regras gerais e todas as etapas e práticas necessárias à tarefa.
Identifique branch e commit da versão do método quando possível.
Comece avaliando os materiais existentes do projeto e as lacunas relevantes.
Separe evidência, hipótese, proposta, decisão aprovada, pendência e substituição.
Confira as decisões oficiais, Issues e autorizações da tarefa antes de atuar.
Não preencha lacunas relevantes silenciosamente nem afirme ações sem evidência.
Ao trocar de tarefa, escopo ou ferramenta, atualize a transferência de contexto.

Tarefa autorizada: <descrever objetivo, limites e ações autorizadas>.
Fontes do projeto: <repositório, branch, documentos, Issues e assets>.
```

Na primeira resposta, confirmar: fontes e versões realmente lidas; objetivo e estado do trabalho; materiais aproveitáveis; lacunas; decisões vigentes; próximo passo elegível; limitações de acesso e capacidade. Pode ser um registro curto em português. Não declarar compatibilidade ou execução integral em uma ferramenta sem comprovação.

## Produzir e aprovar decisões

Trabalhar em unidades revisáveis: analisar a necessidade, apresentar proposta, obter decisão do responsável e registrar a versão aprovada. Ajustar o mesmo material. A aprovação do conteúdo e a autorização para registrá-lo podem vir na mesma instrução explícita.

Antes de gravar, confirmar o destino autorizado. A metodologia pertence a este repositório; os documentos e o código do produto pertencem ao repositório do produto. Não salvar artefatos de um projeto na documentação do método por engano.

Se não houver acesso de escrita ao destino, preparar material para importação ou registrar o impedimento. Sem acesso ao GitHub, não alegar que Issues ou Projects foram atualizados. Não criar uma segunda fila local editável para substituir silenciosamente o backlog oficial.

## Transferência para execução local

O executor local, seja uma pessoa ou agente de codificação, recebe os documentos aprovados acessíveis, a Issue, critérios de aceite, decisões de arquitetura/tecnologia/infraestrutura, dependências, evidências e ações autorizadas. Conferir instruções locais de agentes e habilidades existentes, sem presumir que foram carregadas.

Conferir remote, branch, commits disponíveis, alterações locais e trabalho não integrado. Atualizar fontes quando necessário sem sobrescrever alterações de outras pessoas. Uma versão de documento não sincronizada deve ser identificada explicitamente.

Confirmar antes de implementar: estado da preparação técnica; próximo item pronto; decisões e padrões aplicáveis; verificações; permissões; impedimentos. Começar pelos itens necessários à entrega, preservando preparação e exceções aprovadas. Não escolher funcionalidades aleatoriamente.

Para comandos curtos recorrentes, usar o contexto persistido: “Consulte a Issue e as fontes oficiais e execute o próximo item pronto dentro das autorizações, critérios e padrões do projeto.” O executor continua responsável por conferir as fontes e o estado real.

## Quando retornar uma decisão ao responsável

Apontar conflito ou lacuna que ultrapasse a autorização: requisito ambíguo; nova regra de produto; mudança de experiência, arquitetura ou tecnologia; infraestrutura não prevista; custo; risco novo; ampliação de escopo. Apresentar contexto, alternativas e impacto. Registrar a resolução e atualizar fontes antes de tratar a escolha como regra vigente.

Continuar partes independentes que já tenham escopo e autorização suficientes. Não inventar aprovação nem usar um problema localizado para interromper trabalho independente sem necessidade.

## Conferir fontes e resultados

Aplicar [pesquisa e benchmarking](../pesquisa-e-benchmarking.md) nas escolhas materiais e [verificação com IA](../verificacao-com-ia.md) para conferir afirmações e execução. Distinguir fonte, observação, inferência, estimativa e proposta. Uma resposta convincente ou concordância entre agentes não substitui fonte verificada, decisão ou teste.

## Registro de continuidade

Persistir na Issue e/ou documento de continuidade definido pelo projeto:

- Tarefa, responsável, etapa e estado real.
- Repositório, branch, commit e materiais oficiais utilizados.
- Decisões aprovadas, propostas abertas, conflitos e dependências.
- Arquivos alterados, ações executadas e evidências acessíveis.
- Testes e verificações executados, não executados e seus resultados.
- Riscos, impedimentos, trabalho não integrado e próximo passo.

Ao retomar, ler esse registro, conferir a fonte atual e reconciliar mudanças. A memória da conversa e um resumo informal não substituem os materiais oficiais. O checkpoint não deve virar um backlog concorrente.

## Exemplos e compatibilidade

Manter demonstrações fictícias identificadas como exemplo, separadas das regras do método. Um exemplo não aprova escolhas para outro produto nem prova que o método foi testado em todas as ferramentas.

O histórico do processo contém instruções específicas para ChatGPT e Codex. O núcleo reorganizado descreve responsabilidades portáveis; o uso com Gemini ou outras ferramentas exige conferir capacidades e registrar limitações. Não apresentar portabilidade prevista como homologação de ponta a ponta.

### Campos usados por instruções anteriores

Projetos com prompts e habilidades existentes podem manter os identificadores abaixo durante a adaptação. Eles são rótulos de relatório, não comandos que comprovem execução. Novos usuários podem usar o registro curto em português descrito acima.

| Identificadores preservados | Como interpretar |
| --- | --- |
| `ENGINE_STATUS`, `SOURCE`, `ENGINE_SOURCE`, `BRANCH`, `COMMIT`, `LOADED_COMMIT` | Estado do carregamento e versão do método realmente acessada; nomes alternativos continuam disponíveis para consumidores anteriores |
| `PROCESS_LOADED`, `DOCUMENTS_CONSUMED` | Extensão da leitura e lista de materiais consumidos. Usar `complete` só para leitura completa do método; para leitura completa do escopo da tarefa, indicar `task-scope` e fontes |
| `CURRENT_STAGE`, `DISCOVERY_READINESS`, `CANONICAL_DOCUMENTS_CREATED`, `NEXT_ELIGIBLE_ACTION`, `NEXT_ACTION` | Etapa real, suficiência dos materiais existentes, documentos efetivamente registrados e próxima ação elegível |
| `DOCUMENT_CONSISTENCY`, `TECH_STACK_STATUS`, `CURRENT_FOUNDATION_STATUS`, `BACKLOG_STATUS` | Situação verificada de documentos, tecnologias, preparação e Issues; declarar o que não foi conferido |
| `NEXT_EXECUTABLE_ITEM`, `BLOCKERS`, `PROPOSED_FIRST_SLICE` | Próximo item pronto, impedimentos e entrega proposta. O nome antigo `PROPOSED_FIRST_SLICE` pode ser mantido como compatibilidade; no texto, descrever a entrega pequena e verificável |
| `ENGINE_VERSION`, `PROJECT_STAGE`, `LAST_CANONICAL_DOCUMENT`, `NEXT_DOCUMENT`, `PROJECT_DOC_DESTINATION` | Campos opcionais do checkpoint: versão, etapa, último registro, próximo material necessário e destino autorizado |

Verificar os consumidores antes de alterar esses rótulos, nomes de documentos ou automações locais. Usar o procedimento de adaptação do [guia de handoffs](../handoffs.md) e verificar os consumidores no ambiente de destino; modelos publicados não comprovam configurações externas atualizadas.

[Voltar ao guia](../../README.md)
