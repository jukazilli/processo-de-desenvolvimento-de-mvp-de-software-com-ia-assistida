# Conversa de planejamento e decisões

> Todo o diálogo é fictício. Não representa pesquisa, aprovação ou execução real. A [entrada por materiais existentes](pontos-de-partida.md) é igualmente válida; esta conversa começa de uma ideia.

## 1. Definir o ponto de partida

**Responsável:** “Quero organizar os treinamentos da consultoria. Hoje materiais e acompanhamento ficam dispersos.”

**IA:** “Vou registrar isso como relato inicial, ainda sem comprovar frequência, impacto ou demanda por uma nova plataforma. Você decide produto; decisões técnicas e custos terão responsáveis identificados. Primeiro vamos comparar melhorar o processo atual, adaptar uma solução existente e construir.”

**Registro esperado:** Issue de pesquisa com pergunta, fontes acessíveis, limites e aceite; índice de autoridades na [governança](governanca-do-exemplo.md). Sem acesso a uma fonte, registrar a lacuna.

## 2. Entender problema e delimitar a proposta

**IA:** “A hipótese é atribuir trilhas por empresa, função e turma. Ainda falta ouvir os envolvidos e avaliar alternativas. O [documento de viabilidade](problema-e-viabilidade.md) mantém essas dúvidas.”

**Responsável:** “Para o exercício, vamos explorar um Beta com cursos, trilhas, progresso, avaliações e certificados. Nada de integração automática ou cobrança.”

**Registro esperado:** [objetivo e escopo](objetivo-e-escopo.md) e [prioridades](prioridades-do-produto.md). A instrução aprova o recorte e autoriza seu registro dentro da simulação; não exige dois comandos de aprovação com o mesmo sentido. Não comprova demanda nem autoriza recursos pagos.

## 3. Descrever experiência e interface

**IA:** “Começaremos pela jornada do aluno: aceitar convite, encontrar a trilha e continuar a próxima atividade. Vou incluir ausência de trilha, convite expirado, falha de rede e acesso negado. As referências apoiam a proposta; não provam usabilidade.”

**Responsável:** “Priorize a próxima atividade e deixe claro em qual empresa a pessoa está.”

**Registro esperado:** [princípios](principios-de-experiencia.md), [jornadas](jornadas-e-comportamento.md) e [interface](interface-e-componentes.md). Um protótipo aprovado comprovaria apenas o design revisado, com versão e escopo, não login funcionando.

## 4. Planejar qualidade, arquitetura e tecnologias

**IA:** “O isolamento entre empresas exige autorização no servidor e testes negativos. Vou comparar alternativas arquiteturais conforme equipe, implantação e requisitos. Tecnologias e fornecedores precisam de versões e compatibilidade verificadas antes da adoção.”

**Responsável:** “Para a narrativa, considere monólito modular com web e API separadas. Documente consequências e o que poderia mudar a escolha.”

**Registro esperado:** [qualidade](qualidade-do-codigo.md), [arquitetura](arquitetura.md), [comparação](comparacao-e-decisao.md) e [tecnologias](tecnologias.md). Escolhas são ilustrativas; as versões e o conjunto não foram instalados. Uma descoberta de incompatibilidade retorna à decisão pertinente.

## 5. Planejar infraestrutura

**IA:** “Qual volume esperado, tipo de dado, região, orçamento e capacidade operacional? A seleção ilustrativa não informa preço vigente. O custo de todos os candidatos continua desconhecido.”

**Responsável:** “Equipe pequena, dados pessoais e de aprendizagem, menos de 500 usuários como hipótese de dimensionamento. Quero pré-produção; qualquer contratação precisa de decisão específica.”

**Registro esperado:** [infraestrutura](infraestrutura-e-fundacao.md), responsabilidades, recuperação e condições para autorização. Login e segredos usam o mecanismo seguro da ferramenta, sem credenciais pelo chat.

## 6. Organizar a execução no GitHub

**IA:** “Vou preparar Issues com objetivo, fonte, aceite, dependências e evidência esperada. O catálogo didático mostra o conteúdo, mas não cria uma fila real nem uma matriz editável de status. Na adoção, os links reais ficam nas Issues.”

**Responsável:** “Prepare primeiro a estrutura do repositório, sem instalar bibliotecas ou criar nuvem.”

**Registro esperado:** [Issue FND-001](issues-e-criterios.md), vínculos de [rastreabilidade](rastreabilidade.md) e [handoff](handoff-de-execucao.md). Esta autorização cobre somente o recorte declarado na narrativa.

## 7. Retomar, verificar e aprender

O próximo executor confere branch, commit, fontes e capacidades. Informa o que leu e o que não consegue acessar. Ao terminar um recorte, registra diff, verificações e pendências reais; atualiza documentação afetada sem transformar proposta em aprovação. A liberação segue [critérios próprios](validacao-e-operacao.md). Este exemplo termina antes de executar qualquer código.

[Índice do exemplo](README.md)
