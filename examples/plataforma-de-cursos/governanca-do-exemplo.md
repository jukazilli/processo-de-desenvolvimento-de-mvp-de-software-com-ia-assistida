# Autoridade e documentação no exemplo

> Arranjo fictício para demonstrar adoção. Não há equipe externa, repositório do produto ou Projects configurado.

## Quem decide

Ana responde por objetivo, escopo e identidade; a pessoa responsável pela engenharia responde por propostas e coerência técnica. Executor e revisor registram suas contribuições; se forem a mesma pessoa, não alegam revisão independente. Liberação e contratação têm responsáveis e autorizações próprios.

O [índice](README.md) aponta para cada fonte oficial por assunto. DOC-02 governa escopo, DOC-05 comportamento, DOC-04 interface, DOC-06 qualidade, DOC-07 arquitetura, TECH-LEAD-VISION tecnologias e o documento de infraestrutura condições de operação. Os IDs são legados do exemplo, não ordem obrigatória do processo. DOC-03 registra prioridades, sem repetir o escopo. Discussões ficam na Issue; a fonte do assunto recebe a decisão consolidada.

## Exemplo de mudança incremental

1. A Issue de convite registra que a tela não trata expiração; a IA apresenta proposta, impacto e dúvida.
2. Ana aprova apenas o comportamento “explicação clara e caminho para pedir novo convite”, identificando versão e escopo no comentário real quando houver execução. A aprovação da aparência não comprova envio de e-mail.
3. O índice da Issue aponta para a aprovação. Uma PR atualiza DOC-05 e os arquivos afetados; o README geral só muda se houver mudança geral ou de índice.
4. Implementação, testes e liberação recebem seus vínculos e resultados próprios. A aprovação de comportamento pode vigorar para uma versão futura; isso deve estar explícito.
5. Se uma decisão for substituída, registrar motivo, responsável, versão e referência à anterior. Não apagar o histórico nem ajustar documentos para encobrir divergência do código.

## Como manter a continuidade

Na Issue: estado operacional, decisão aplicável, fontes/versões, PR e evidências, pendências e próximo passo. No Git: documentos e alterações revisáveis. No handoff: links e o recorte para assumir, sem copiar todos os contratos. Não criar `backlog.md`, `final-v2.md` ou matriz com status concorrentes.

Sem acesso ao GitHub, preparar o conteúdo para importação e declarar que não foi publicado. Antes de retirar uma fila antiga de uso, conferir que IDs, critérios e dependências foram transferidos e que seus consumidores foram adaptados. Um arquivo datado pode permanecer como histórico, sem edição operacional paralela.

[Governança do método](../../docs/governanca.md) · [Índice](README.md)
