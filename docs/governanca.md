# Governança e documentação incremental

Governança define quem decide, onde a decisão fica e qual evidência permite avançar. O registro deve ser proporcional ao trabalho: para uma mudança pequena, uma Issue, uma PR e a atualização da fonte afetada podem ser suficientes.

Este guia é definido na etapa 01, refinado na etapa 10 e aplicado durante todas as entregas. A fila de trabalho continua em Issues; os documentos guardam decisões, especificações e instruções duráveis.

## Responsabilidades

Uma pessoa pode exercer vários papéis. Registrar quem decide produto, quem responde pelas decisões técnicas, quem executa, quem revisa e quem autoriza a liberação. A equipe define a revisão possível para seu porte; revisão do próprio autor não deve ser apresentada como revisão independente.

A IA pode propor, pesquisar, implementar e verificar dentro do escopo autorizado. O responsável humano continua decidindo mudanças relevantes de objetivo, comportamento, identidade, custo e risco. Autorizações explícitas já dadas permanecem válidas no seu escopo. Uma instrução pode aprovar conteúdo e autorizar seu registro ao mesmo tempo.

## Onde cada informação fica

| Informação | Fonte indicada | Como usar |
| --- | --- | --- |
| Objetivo, limites e decisões gerais aprovadas | README do produto ou documento oficial indicado por ele | Atualizar somente quando houver mudança pertinente; manter o índice curto |
| Especificações e regras detalhadas | Documento versionado ou Issue responsável declarada no índice | Escolher uma autoridade por assunto; apontar para ela em vez de copiar a regra |
| Decisão arquitetural significativa | Registro de decisão — ADR — no local escolhido pelo projeto | Contexto, alternativas, decisão, consequências, estado e substituições |
| Pesquisa, proposta, tarefa e bug | Issue | Registrar trabalho, evidências e pendências sem promover proposta automaticamente |
| Discussão, aprovação e histórico | Comentários com links e autoria | Preservar a sequência; o índice indica o comentário aplicável |
| Andamento, prioridade e ciclo | Issues e, opcionalmente, Projects | Projects apresenta o trabalho; seu status não aprova produto |
| Código, assets e mudanças documentais | Git, branch e PR | Identificar arquivo e commit; revisar o escopo antes da integração |
| Resultado de teste e operação | Evidência ligada à Issue/PR e versão | Informar condições, resultado e limites; não confundir imagem ou plano com execução |
| Retomada da atividade | Último handoff na Issue ou checkpoint indicado por ela | Apontar para fontes e próximo passo, sem criar outra fila |

Um projeto pode usar documentos para regras gerais e comentários aprovados para detalhes de telas. Deve declarar essa divisão e manter um índice por assunto. Um comentário de aprovação de um ADR registra a revisão e aponta para o ADR; não cria outro texto concorrente para a mesma decisão.

## Como registrar uma decisão

1. Reunir contexto, fontes, alternativas, consequências e pergunta que precisa de decisão. Publicar como proposta, com dúvidas identificadas.
2. Solicitar decisão ao responsável quando necessário. Identificar exatamente o que ele aprovou, suas condições e o que ficou fora.
3. Usar o [modelo de decisão](modelos/decisao.md) para registrar autoria, escopo, versão, evidência de aprovação e vigência. Uma proposta ainda não aprovada deve continuar identificada como proposta.
4. Atualizar a fonte oficial do assunto e seu índice. Quando a decisão for geral, atualizar também o README ou documento geral afetado por PR. Se o assunto for local, não reescrever o README só por rotina.
5. Vincular implementação, validação e outras ações necessárias a Issues. Aprovação visual, por exemplo, não comprova OAuth, autenticação ou persistência funcionando.

Registrar aprovação e vigência separadamente: uma decisão pode estar aprovada para uma versão futura, aguardando consolidação ou depender de uma condição. Não apresentá-la como comportamento já disponível. A aprovação não autoriza automaticamente merge, compra ou publicação que esteja fora das ações autorizadas.

## Decisões mantidas em comentários de Issues

Usar uma Issue responsável por funcionalidade, tela ou contrato. Seu corpo mantém um [índice curto](modelos/indice-da-issue.md) para decisões vigentes, assets, pendências e trabalho relacionado. Os comentários preservam pesquisa, proposta, revisão e aprovação.

Quando uma decisão mudar, publicar um novo registro que indique o que substitui, por que mudou, quem aprovou e em qual escopo passa a valer. Atualizar o índice; não apagar o histórico nem escolher uma decisão só porque seu comentário é o mais recente. Corrigir informação material de um registro aprovado por novo registro ou histórico explícito; não reescrever uma aprovação antiga como se tivesse outro conteúdo.

Assets devem ter caminho e commit ou versão identificáveis, com natureza da evidência: arquivo mestre, prévia, imagem gerada, protótipo ou captura real. Se o arquivo não estiver acessível, registrar a ausência e não alegar conferência visual.

## Evidência para decisões

Uma comparação pode apoiar a proposta; ela não comprova a escolha funcionando. Apontar para a [pesquisa e comparação](pesquisa-e-benchmarking.md) e para a evidência pertinente ao contrato. O registro de comparação ou o documento já existente mantém o detalhe; a decisão identifica o que usa, o que permanece incerto e quando deve ser revista. Aplicar a [verificação com IA](verificacao-com-ia.md) antes de apresentar uma afirmação relevante como comprovada.

## Conflitos

Apontar as fontes, versões e escopos em conflito. Consultar quem tem autoridade no assunto. Enquanto a resolução estiver pendente, manter o conflito visível e trabalhar apenas nas partes independentes já autorizadas.

Não tratar código em execução como aprovação retroativa. Se a realidade mostrar que uma decisão é inviável, propor sua revisão e registrar a resolução, com atualização dos vínculos afetados.

## Documentar junto com a entrega

Antes de começar, identificar documentos afetados. Durante o trabalho, registrar descobertas e propostas na Issue. Ao preparar a PR, atualizar especificações, decisões e instruções necessárias para que outra pessoa compreenda o resultado sem a conversa.

Criar documento novo quando houver conhecimento durável que realmente precise de um lugar próprio: contrato de API, dados, autorização, operação, recuperação ou decisão técnica. Se uma atualização na fonte existente resolver, aproveitá-la. Não converter cada comentário em documento nem gerar manifestos paralelos com o mesmo contrato.

Arquivos de configuração, schemas e contratos executáveis podem existir como código real. Eles precisam de responsabilidade definida e verificação; não são substitutos automáticos de decisão de produto.

Agentes e automações podem atualizar documentos dentro do escopo autorizado, conferir links, apontar decisões sem origem ou preparar correções de consistência. A revisão deve manter a distinção entre uma proposta e uma decisão já aprovada. Uma verificação automática não deve ajustar a documentação para legitimar uma divergência de código nem marcar aprovações que o responsável não deu.

## Critério de conclusão por escopo

| Tipo de trabalho | Evidência de conclusão | O que continua separado |
| --- | --- | --- |
| Pesquisa | Pergunta respondida, fontes e limites registrados, resultados revisados e recomendações encaminhadas | Aprovação de uma escolha ou implementação que não fazia parte da pesquisa |
| Design | Comportamento e referência aprovados no escopo, versões e exceções indexadas, documentação consolidada | Implementação, testes e liberação funcional |
| Implementação | Aceite atendido, PR revisada/integrada conforme o projeto, verificações e documentos atualizados | Liberação se houver uma Issue ou etapa específica para ela |
| Liberação | Versão e ambiente conferidos, autorização e evidências, acompanhamento e retorno definidos | Evoluções e riscos explicitamente aceitos como trabalho futuro |
| Documentação | Fonte e índice atualizados, coerência e links conferidos, revisão e integração pertinentes | Funcionalidade apenas descrita, mas não implementada |

O estado Feito exige aceite do próprio escopo, evidências, auditoria de consistência e consolidação documental aplicável. Uma mudança geral aguardando integração em seu documento oficial continua pendente de consolidação. Uma pesquisa pode terminar mesmo se sua recomendação ainda depender de decisão, desde que isso esteja explícito e rastreado.

No encerramento, publicar resultado, versão, evidências, verificações realizadas/não realizadas, documentos atualizados e trabalho restante. Conferir a Issue, a PR e o Projects separadamente; uma transição não comprova as outras. Usar o [handoff](handoffs.md) quando outra pessoa ou ferramenta precisar assumir.

## Adotar em um projeto existente

Inventariar documentos, Issues, IDs, arquivos e instruções de ferramentas. Escolher as autoridades vigentes e mapear conflitos. Transferir tarefas para Issues sem perder aceite, dependências e histórico; conferir paridade antes de retirar a fila antiga da edição diária. Uma exportação datada pode permanecer como histórico, identificada como tal.

Preservar IDs e links consumidos por ferramentas. Atualizar consumidores antes de renomear arquivos ou campos de relatório. Configurações e habilidades locais só são consideradas atualizadas quando houver evidência no ambiente correspondente.

[Trabalho no GitHub](trabalho-no-github.md) · [Handoffs](handoffs.md) · [Modelos](modelos/README.md) · [Voltar ao guia](../README.md)
