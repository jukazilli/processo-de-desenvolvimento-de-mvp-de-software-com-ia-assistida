# Pesquisa e comparação de referências — benchmarking

Comparar referências ajuda a entender soluções existentes e decidir o que adaptar. A pergunta vem antes da busca: qual decisão precisamos tomar e quais dúvidas podem mudar essa decisão? O resultado pode caber em um comentário da Issue ou exigir um estudo próprio, conforme impacto e incerteza.

Comparação de produto e padrões não é a mesma coisa que benchmark de desempenho. No primeiro caso, analisamos alternativas e contexto; no segundo, medimos uma carga em condições declaradas. Nenhum dos dois, sozinho, comprova necessidade de usuário, segurança ou adequação da solução.

## Quando comparar e quando reaproveitar

Comparar alternativas é necessário nas escolhas relevantes de produto, experiência, qualidade, arquitetura, tecnologias e infraestrutura. Registrar a comparação já existente pode atender à etapa se suas condições continuarem válidas. Não repetir uma pesquisa suficiente nem exigir pesquisa de mercado ampla para toda correção.

Uma correção localizada pode conferir o padrão existente, a documentação da versão instalada e os testes afetados. Uma escolha com impacto em dados, custo, operação, acesso ou identidade requer mais evidência. Definir uma pergunta e um limite de investigação evita pesquisar indefinidamente sem resolver o trabalho.

## Como realizar

1. Definir a pergunta, o escopo, o responsável e a decisão que depende da resposta. Separar critérios obrigatórios de preferências.
2. Levantar o que já existe no projeto: decisões, requisitos, pesquisas, código, componentes, métricas e restrições. Incluir manter a solução atual entre as alternativas quando fizer sentido.
3. Escolher referências comparáveis. Podem ser padrões documentados, produtos observados, implementações públicas, arquiteturas e alternativas técnicas. Usar poucas opções relevantes; justificar opção única quando uma restrição realmente eliminar as demais.
4. Ler as fontes originais. Registrar URL ou caminho, autor/provedor, data da consulta, versão pertinente, afirmação sustentada e limite de aplicação. Um resultado de busca ou uma resposta de IA é um ponto de partida, não a evidência final de uma escolha material.
5. Comparar pelo mesmo conjunto de critérios e condições. Eliminar alternativas incompatíveis com exigências reais antes de atribuir notas. Informações ausentes ficam como não verificadas, não como zero ou nota inventada.
6. Identificar o que a leitura não comprova e planejar validação adequada: pesquisa com usuários, protótipo, experimento técnico, teste, medição ou revisão especializada. Indicar condições, resultado esperado e limites antes de executar.
7. Registrar conclusão, alternativas rejeitadas, consequências, incertezas e condições para reavaliar. Encaminhar a recomendação para decisão humana quando pertinente.
8. Vincular a decisão e as Issues derivadas. Atualizar a fonte oficial quando a escolha for aprovada; guardar o detalhe no lugar escolhido sem duplicá-lo no README, na Issue e num manifesto paralelo.

Usar o [modelo de comparação](modelos/comparacao.md) quando necessário. Um registro existente que já responda aos campos essenciais pode ser reaproveitado.

## Comparar por etapa

| Etapa | Pergunta ou referência útil | Evidência para avançar |
| --- | --- | --- |
| 01 — Entrada | Que material já atende ao objetivo e o que ainda falta? | Fonte, versão, aprovação e lacunas conferidas; comparação externa só se houver dúvida relevante |
| 02 — Problema | Como pessoas resolvem a necessidade hoje? Que serviços ou alternativas já existem? | Evidência existente e pesquisa apropriada; a aparência de um concorrente não comprova demanda |
| 03 — Produto | Qual proposta e escopo atendem ao objetivo com as restrições reais? | Alternativas e critérios de valor; metas e estimativas identificadas, sem alegar validação que não ocorreu |
| 04 — UX | Como tarefas semelhantes são realizadas, inclusive falhas e retomada? | Referências contextualizadas e validação das hipóteses importantes com pessoas ou protótipo |
| 05 — UI | Que hierarquia, componentes e estados atendem à tarefa? | Padrões, identidade, acessibilidade e comportamento conferidos; imagem gerada não equivale a teste |
| 06 — Qualidade | Que requisitos e verificações cobrem os riscos? | Padrões aplicáveis, objetivos mensuráveis e critérios de teste; norma citada não comprova conformidade |
| 07 — Arquitetura | Quais estruturas resolvem as restrições com complexidade aceitável? | Alternativas, limites, dados e consequências; prova técnica se houver incerteza que afeta a decisão |
| 08 — Tecnologias | O que existe, é compatível e tem suporte para o caso? | Documentação e versão, origem de dependências, licença e verificação dos contratos importantes |
| 09 — Infraestrutura | Quais serviços cabem no runtime, risco, região, custo e operação? | Fontes atuais, cenários e limites; validar integração e custo no contexto previsto |
| 10 — Trabalho | Que estrutura e recursos reais facilitam assumir a próxima Issue? | Configuração observada e documentação do GitHub; não criar fluxo novo só por preferência do agente |
| 11 — Fundação | A configuração corresponde ao plano e à versão escolhida? | Comandos conferidos e execução no ambiente autorizado; um guia de setup não comprova ambiente pronto |
| 12 — Desenvolvimento | Existe solução equivalente e como o contrato será verificado? | Código local, padrões e documentação da versão; revisão e testes, inclusive falhas relevantes |
| 13 — Validação | O candidato atende aos critérios nas condições pertinentes? | Resultados reais de teste e ambiente; benchmarks de terceiros não substituem a validação do candidato |
| 14 — Operação | O resultado atual atende ao objetivo e o que mudou? | Métricas e feedback observados, comparados à base e às condições do próprio produto |

As etapas 04–09 concentram escolhas que pedem comparação técnica ou de experiência quando relevantes. Nas demais, a conferência pode ser principalmente de evidências internas e execução. Isso organiza o esforço; não é um ranking de probabilidade de erro de IA.

## UX e UI: aprender com quem documenta padrões

O [GOV.UK Design System](https://design-system.service.gov.uk/patterns/) organiza padrões por tarefas e tipos de página. O [Carbon Design System](https://www.carbondesignsystem.com/building-blocks/core/components/overview/components) documenta componentes e seus problemas de interface. Eles são referências possíveis para examinar hierarquia, formulários, feedback e consistência, sem transformar a identidade de outro produto na identidade do seu.

Comparar tarefa, público, dispositivo, contexto, volume de informação e estados de falha. Registrar o padrão observado, o problema que ele resolve, o que será adaptado e o que será descartado. Não atribuir melhoria de conversão ou usabilidade a uma tela sem dados que sustentem essa conclusão.

A pesquisa com usuários ajuda a verificar necessidades; critérios de acessibilidade e sua avaliação ajudam a verificar barreiras. As orientações da [W3C/WAI](https://www.w3.org/WAI/test-evaluate/) deixam claro que ferramentas automáticas não determinam acessibilidade sozinhas. Complementar com avaliação humana e uso real conforme o caso.

## Engenharia, arquitetura e tecnologias

Partir de requisitos e restrições. Um sistema usado por uma grande empresa pode resolver escala, equipes e operação muito diferentes das suas. Comparar alternativas de estrutura e consequências, registrando decisões significativas em ADR quando útil. C4 é uma referência para comunicar a estrutura; não escolhe por si só o padrão arquitetural do produto.

Na escolha tecnológica, verificar documentação correspondente à versão, suporte, manutenção, licença, compatibilidade e regras de uso. Conferir pacote, origem e responsável antes de instalar: um nome aparentemente plausível não comprova existência, legitimidade ou adequação. Uma dependência já conhecida pode ser suficiente; uma nova deve ter justificativa.

Usar critérios eliminatórios para incompatibilidades reais e preferências para os compromissos aceitáveis. Notas e pesos podem explicar raciocínio, mas devem indicar como foram obtidos. Não apresentar pontuação subjetiva como medição científica.

## Infraestrutura e custo

Comparar os serviços necessários ao plano, sem escolher fornecedor primeiro e reconstruir o produto para caber nele. Frameworks de arquitetura em nuvem ajudam a revisar preocupações como segurança, confiabilidade, operação, desempenho e custo; não obrigam usar o provedor que publicou a orientação.

Registrar data, plano, região, moeda, limites, crédito temporário, cobranças mínimas e condições de atualização relevantes. Explicitar premissas de usuários, tráfego, armazenamento, processamento, saída de dados, mensagens, backups e logs conforme o projeto. Valores desconhecidos permanecem a verificar. Estimativa não é fatura real, e camada gratuita não é garantia de operação sem custo.

Experimentos precisam de escopo, condições e autorização de gasto. Revalidar preço e compatibilidade antes da contratação ou mudança de recurso. A escolha aprovada não comprova que integração, backup ou recuperação funcionam: isso exige execução e evidência pertinentes.

## Quando a comparação é suficiente

A pergunta está respondida no grau necessário à decisão; restrições foram verificadas; alternativas e consequências estão claras; as incertezas restantes têm tratamento e responsável. A decisão pode ser seguir, experimentar, reduzir escopo ou não construir.

Definir gatilhos para reavaliar: mudança de requisito, versão, fornecedor, equipe, custo, risco, volume ou evidência de uso. Uma data de consulta registra a origem; não torna a informação válida por um prazo arbitrário. Fontes mutáveis precisam ser conferidas no momento em que sustentam uma ação relevante.

## Fontes e limites

As [fontes de referência](../docs/fontes-de-referencia.md) distinguem orientações, padrões e pesquisa empírica. As regras operacionais deste capítulo são uma adaptação do método para o contexto de desenvolvimento com IA. Não representam certificação nem adoção integral de cada framework citado.

[Verificação com IA](verificacao-com-ia.md) · [Pesquisa em Issue](modelos/pesquisa.md) · [Voltar ao guia](../README.md)

## Onde consolidar os achados

Apresentar achados e comparação na seção da etapa em `docs/PROJETO.md`, com referências identificadas na seção 15 — Fontes e evidências. Discussão e material bruto podem ficar na Issue ou em anexo vinculado. Separar achado, inferência, hipótese e recomendação; salvar como rascunho não aprova a conclusão.
