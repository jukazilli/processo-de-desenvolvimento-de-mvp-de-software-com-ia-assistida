# Conferir informações e resultados produzidos com IA

Uma resposta pode ser bem escrita e ainda conter informação incorreta, referência inexistente ou uma conclusão que as fontes não sustentam. O NIST AI 600-1 trata de confabulação, confiança excessiva e integridade da informação. Aqui usamos essas preocupações para orientar a revisão do trabalho assistido por IA, inclusive quando o produto final não possui recursos de IA.

As orientações abaixo são controles propostos pelo método, não taxas medidas de falha. A intensidade da revisão depende da tarefa, das evidências disponíveis, do impacto de um erro e da possibilidade de detectá-lo antes de causar consequência.

## Onde reforçar a conferência

Reforçar a revisão quando falta contexto, a informação muda rapidamente, a resposta faz inferências sobre pessoas, há muitas versões ou integrações, ou uma escolha afeta dados, acesso, custo e operação. Quanto maior a consequência de aceitar uma afirmação errada, mais forte precisa ser a evidência antes da ação.

| Situação | Erro que pode passar despercebido | Prevenir | Detectar ou comprovar |
| --- | --- | --- | --- |
| Problema, público e mercado | Persona, entrevista, necessidade ou resultado inventados | Usar fontes e materiais reais; marcar hipótese | Conferir evidência de origem; pesquisar com usuários quando necessário |
| Requisitos e regras | Transformar sugestão em obrigação ou preencher lacuna silenciosamente | Separar decisão, proposta, inferência e dúvida | Revisão do responsável e rastreio do requisito até sua fonte |
| UX/UI | Inferir funcionamento, acessibilidade ou melhora de desempenho a partir de imagem | Analisar tarefa e estados; registrar o que a imagem permite observar | Protótipo, avaliação humana, critérios verificáveis e pesquisa aplicável |
| Engenharia e segurança | Declarar sistema seguro ou conforme só por citar um padrão | Selecionar versão e requisitos aplicáveis; definir verificação | Testes positivos/negativos, revisão técnica e evidência no escopo declarado |
| Arquitetura | Copiar padrão sem considerar escala, equipe e limites | Comparar alternativas contra restrições e registrar consequências | Revisar limites e contratos; experimentar a incerteza técnica relevante |
| Bibliotecas e APIs | Nome plausível inexistente, origem suspeita ou API de outra versão | Conferir registro, origem e documentação da versão; reaproveitar dependências aprovadas | Conferir pacote e contratos, análise de código, tipos e testes pertinentes |
| Infraestrutura e custos | Preço antigo, limite omitido, região ou runtime incompatível | Consultar condições oficiais atuais e explicitar premissas | Validação no ambiente autorizado; conferir limites e cálculo do cenário |
| Código e testes | Implementação errada com teste que repete a mesma suposição | Derivar teste de requisito e risco, não só da implementação | Revisão do diff, casos negativos, integração e regressão conforme o caso |
| Execução e documentação | Afirmar leitura, teste, merge, deploy ou alteração que não ocorreu | Pedir resultado observável e registrar limitações | Conferir saída, commit, PR, artefato, ambiente e vínculos reais |
| Operação e aprendizado | Diagnóstico ou tendência apresentados como fato sem dados | Separar causa confirmada de hipótese e cenário estimado | Logs, reprodução, métricas e feedback sob condições identificadas |

Essa tabela prioriza tipos de revisão pelo contexto. Não autoriza dizer que uma etapa alucina mais do que outra em qualquer modelo, prompt ou ambiente. Para medir isso, seria necessário um experimento com tarefas, versões, condições e critérios definidos.

## Procedimento de verificação

1. Destacar a afirmação que sustenta a decisão ou ação. Distinguir fato consultado, observação local, inferência, estimativa e proposta.
2. Abrir a fonte original e conferir se ela realmente sustenta a afirmação. Verificar versão, escopo, autoria, data pertinente e condições. Um link existente não comprova que o conteúdo diga o que foi atribuído a ele.
3. Comparar a informação com requisitos, decisões e ambiente do projeto. Uma capacidade do fornecedor não comprova que a conta, o plano ou a configuração atual a disponibilizem.
4. Escolher como comprovar o que ainda falta: revisão de domínio, consulta ao responsável, pesquisa, protótipo, teste, experimento ou medição. Registrar resultado e limites no lugar oficial.
5. Corrigir erro ou excesso de certeza e atualizar o encaminhamento. Uma lacuna que afeta uma ação relevante impede tratá-la como comprovada; partes independentes já autorizadas podem continuar.
6. Vincular conclusão, fonte e evidência à decisão e à Issue/PR. Registrar o que foi realmente verificado e o que permanece pendente antes do próximo handoff.

Uma segunda resposta do mesmo modelo, a concordância entre agentes ou a autoavaliação de confiança não substituem a fonte nem a execução. Uma revisão feita pelo próprio autor pode ser útil, mas deve ser identificada como tal.

## Usar pesquisa e testes para perguntas diferentes

Uma referência pública mostra uma opção ou orientação; uma hipótese descreve o que ainda não sabemos; uma decisão registra o que foi escolhido; um teste ou medição comprova um comportamento sob condições. Manter essas categorias explícitas evita apresentar benchmarking como validação do produto.

Para acessibilidade, selecionar critérios aplicáveis e combinar avaliação apropriada; uma ferramenta automática ou imagem isolada não prova conformidade. Para segurança, a seleção de requisitos e versão é o início da verificação, não uma garantia de ausência de vulnerabilidades. Para desempenho, registrar carga, ambiente, dados e método antes de comparar resultados.

Em dependências, conferir mais do que o nome existir. O estudo de Spracklen e colaboradores, apresentado na USENIX Security 2025, observou recomendações de pacotes inexistentes nas condições avaliadas. Ele motiva a conferência de origem e documentação; seus resultados não representam uma taxa deste método nem uma avaliação dos modelos atuais usados por toda equipe.

## Ação, acesso e conteúdo externo

Textos externos e saídas de IA são fontes a avaliar. Um comando encontrado em uma página não se torna autorizado só por estar na documentação. Conferir a ferramenta, o ambiente, o escopo e a autorização antes de executar, instalar ou contratar. Preservar limites de acesso e evitar expor dados sensíveis em prompts, logs e evidências.

Quando a ferramenta não conseguir acessar uma fonte essencial ou verificar a ação, registrar a limitação e sua consequência. Não criar evidência fictícia para preencher o relatório. Instalação de habilidades e configurações externas precisa de comprovação própria.

## O que registrar sem gerar burocracia

Usar os campos já existentes na Issue, PR, decisão e handoff. Para escolhas materiais, apontar o [registro de comparação](modelos/comparacao.md) se houver. Não manter uma planilha concorrente apenas para repetir o estado da verificação.

Registrar fonte e versão, afirmação sustentada, verificação realizada, resultado, limite, responsável e próximo passo. Se um padrão de erro se repetir, avaliar prevenção reutilizável — teste, regra, guia ou habilidade — antes de criar um recurso novo.

## Base e limites das recomendações

As definições de confabulação e confiança excessiva vêm do [NIST AI 600-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf). A orientação sobre acessibilidade usa a [W3C/WAI](https://www.w3.org/WAI/test-evaluate/). O estudo de pacotes está disponível na [USENIX](https://www.usenix.org/conference/usenixsecurity25/presentation/spracklen). As aplicações práticas à sequência de desenvolvimento são propostas deste método e precisam ser adaptadas e avaliadas pela equipe.

[Comparação de referências](pesquisa-e-benchmarking.md) · [Fontes](../docs/fontes-de-referencia.md) · [Voltar ao guia](../README.md)
