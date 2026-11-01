# Regras do processo

Estas regras acompanham as 14 etapas e também valem para mudanças em projetos existentes. O tamanho do registro e das verificações deve acompanhar o escopo e o risco da atividade.

## Decisões, evidências e autorização

A conversa é material de raciocínio. Antes de tratar algo como regra do produto, identifique a decisão, seu responsável, estado de aprovação e fonte oficial. Diferencie evidência, hipótese, proposta, decisão aprovada, pendência e decisão substituída.

A IA deve apontar lacunas e conferir se uma regra existente resolve a questão. Uma escolha que altera produto, identidade, arquitetura, custo ou risco além do autorizado precisa de decisão humana. A ausência de especificação não autoriza preencher lacunas silenciosamente.

Apresentar propostas em unidades que o responsável consiga revisar. Ajustar o mesmo material após correções. Uma instrução explícita pode aprovar conteúdo e autorizar seu registro ao mesmo tempo; usar autorizações já concedidas sem pedir a mesma confirmação repetidamente.

Aprovação de uma decisão, autorização de uma ação e comprovação de execução são informações distintas. Criar arquivo, fechar Issue, mesclar PR, aprovar imagem e liberar software não substituem umas às outras.

## Uma fonte oficial por informação

Definir no início onde cada assunto é mantido e quem pode aprová-lo. O README do produto pode registrar decisões gerais ou ser um índice para documentos oficiais. Não copiar a mesma regra para vários locais editáveis.

Documentos de decisão e especificação usam preferencialmente Markdown versionado. Documentos, imagens, planilhas ou outros materiais recebidos continuam sendo entradas válidas: avaliar seu conteúdo, aprovação e atualidade antes de exigir outro formato. Preservar autoria e proveniência ao consolidar decisões.

O número da etapa organiza a navegação do método, não renomeia automaticamente documentos do produto. Preservar IDs, contratos e arquivos existentes que tenham consumidores; registrar seu papel no índice oficial e adaptar os vínculos antes de qualquer renomeação.

O backlog principal é mantido em Issues. Projects acompanha estado operacional e ciclos quando necessário; PRs contêm mudanças revisáveis. Um detalhe de tela pode ter uma Issue responsável como fonte oficial se o projeto declarar essa escolha e mantiver índice para seus contratos e aprovações.

Comentários registram discussão, evidências, aprovações e substituições. O índice da Issue deve apontar para a decisão vigente; não escolher autoridade apenas pela data de um comentário. Requisitos, trabalho, implementação, testes e evidências ficam vinculados. Um relatório adicional de rastreabilidade só se justifica se atender uma necessidade sem criar estado concorrente.

## Documentação incremental

Criar e atualizar documentação quando o conhecimento é necessário ou uma decisão muda. Não produzir um pacote completo por formalidade. APIs, dados, autorização, modelos de ameaça, ambientes, filas, eventos, dependências, operação, observabilidade, recuperação e decisões técnicas podem precisar de documentos próprios conforme o produto evolui.

Manter histórico por Git e decisões de substituição explícitas. Evitar arquivos concorrentes como `final`, `novo` e cópias numeradas sem função. Revisar documentos afetados na mesma entrega de código; separar o que é esperado do que foi implementado e comprovado.

Um registro aprovado deve ter: responsabilidade clara; escopo e limites; fontes; decisões distintas de hipóteses; pendências; linguagem compreensível sem a conversa; vínculos pertinentes; versão; responsável e evidência de aprovação. Metadados opcionais podem registrar ID, título, estado, dependências e assuntos governados. O Git preserva o histórico principal; metadados não devem duplicar controles sem necessidade.

## Conflitos e mudanças

Conferir a natureza da decisão: objetivo e escopo orientam a solução; requisitos de experiência e qualidade influenciam arquitetura; arquitetura restringe tecnologias; tecnologias e operação influenciam infraestrutura. Esse encadeamento permite revisar uma escolha com evidência nova, mantendo o responsável humano no circuito.

Uma implementação divergente não torna a decisão anterior obsoleta automaticamente. Apontar decisões, versões, consequências e dependências; solicitar resolução ao responsável quando ultrapassar o escopo autorizado. Código observado comprova comportamento existente, não aprovação de produto. Uma automação de consistência não deve alterar documentos para fazer um erro parecer conformidade.

Quando inviabilidade ou nova evidência exigir mudança, registrar a decisão que substitui a anterior e atualizar documentos e vínculos afetados. Decisões técnicas significativas podem usar ADRs com contexto, alternativas, decisão e consequências.

## Qualidade verificável

Planejar verificações com base no risco. Quando aplicável, incluir formatação, análise estática, tipos, testes unitários, integração, contratos, jornadas completas, testes negativos de autorização, build, dependências, segredos, limites arquiteturais, migrações, infraestrutura e consistência documental.

Converter regras importantes em verificações executáveis quando viável. Por exemplo: uma regra de que o cliente não tem acesso administrativo pode ser sustentada por separação de credenciais, conferência de exposição e testes de autorização. A ferramenta não aprova a regra de produto: verifica um contrato definido pelo projeto.

Código existente e testes passando são evidências específicas. Para uma liberação, conferir também o candidato em ambiente representativo, os limites do teste, a documentação e a autorização aplicável. Preferir promover o mesmo artefato ou commit validado; mudanças no candidato exigem verificação do impacto.

Declarar verificações executadas, não executadas, resultados e impedimentos. Não alegar teste, aprovação, acesso ao Projects, configuração externa ou disponibilidade sem evidência. Uma pesquisa ou entrega de design pode ser concluída no seu próprio escopo, mantendo implementação e validação funcional como trabalho separado.

## Identidade e experiência

Derivar a interface da marca, contexto, tarefa e jornada. Componentes populares não são uma justificativa de design. Princípios de experiência orientam a decisão; telas e componentes materializam o que precisa ser apresentado; UX descreve comportamento, estados e transições.

Ao usar referências, registrar origem e aprovação; conferir a imagem final e os arquivos acessíveis. Uma referência visual é entrada para interpretação e validação, não comprovação de responsividade ou funcionamento. Diferenciar arquivo mestre, prévia e captura. Uma exceção aprovada deve continuar rastreável.

## Acesso, credenciais e custos

Usar ferramentas autorizadas adequadas ao serviço e respeitar seus limites. Preferir API, CLI ou configuração reproduzível quando disponíveis; usar conectores e automação de interface quando apropriados. Não contornar controle de acesso.

Login, MFA, CAPTCHA, aceite legal e ações sensíveis devem seguir o mecanismo seguro da ferramenta e a participação humana necessária. Segredos ficam no mecanismo próprio do ambiente; não solicitar senhas, chaves privadas, tokens permanentes, códigos de recuperação ou cartão pelo chat. Logs e evidências devem evitar exposição de dados sensíveis.

Conferir custos atuais antes da ação. Contratação, upgrade e criação de recurso potencialmente cobrável exigem finalidade, condições conhecidas e autorização humana explícita. Classificar custo como gratuito dentro de limites, potencialmente cobrável, cobrável ou desconhecido a revalidar. Orçamento e autorizações já dados precisam ser respeitados no seu escopo.

## Transferência e continuidade

Antes de atuar, o executor confere fontes, versões, objetivo, decisões, dependências, critérios e autorização. Habilidades e agentes locais são capacidades de apoio, não uma memória presumida em toda ferramenta.

Ao transferir, registrar: tarefa e estado real; fontes; branch e commit; decisões; resultado; arquivos e evidências; ações e verificações executadas ou pendentes; impedimentos; risco; próximo passo. Salvar o checkpoint no repositório ou na Issue responsável; um resumo de conversa sozinho não substitui fontes oficiais.

Consultar o [guia de uso com IA](continuidade-e-compatibilidade.md) e o [glossário](../docs/glossario.md). Consultar também os procedimentos de [governança](governanca.md), [trabalho no GitHub](trabalho-no-github.md), [handoffs](handoffs.md) e os [modelos](modelos/README.md). Para escolhas e afirmações relevantes, aplicar [pesquisa e benchmarking](pesquisa-e-benchmarking.md) e [verificação com IA](verificacao-com-ia.md), com fonte, versão, evidência e limites explícitos.

[Voltar ao guia](../README.md)

## Documento principal e contrato de saída

O padrão para novos projetos é `docs/PROJETO.md` no repositório do produto, usando o contrato do README e o modelo `framework/modelos/projeto.md`. Cada etapa apresenta uma seção revisável e a atualiza com fontes, hipóteses, propostas, decisões, evidências e pendências identificadas. Uma saída não significa um arquivo novo. Criar anexos somente por necessidade concreta; indexá-los sem duplicar autoridade.

Nas disposições anteriores sobre fonte oficial, README, documento ou comentário, aplicar este padrão: o conhecimento durável é consolidado no documento principal; a Issue mantém trabalho, discussão, aprovação e evidências vinculadas. O README do produto pode apontar para o documento. Em projeto existente, conferir e mapear autoridades e consumidores antes de migrar; a adoção não autoriza sobrescrever fontes, renumerar IDs ou duplicar contratos. O índice do documento identifica eventuais fontes existentes que ainda têm autoridade por assunto.

Sem destino de escrita autorizado, apresentar a seção em Markdown na conversa, identificada como rascunho ainda não salvo. Não condicionar o início de pesquisa a criar um repositório ou uma Issue. Distinguir documento esperado, rascunho apresentado, versão salva, aprovação e integração.
