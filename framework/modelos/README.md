# Modelos para adaptar ao projeto

Os arquivos desta pasta são modelos reutilizáveis, não tarefas reais, aprovações ou configurações externas já aplicadas. Substituir os campos em parênteses; excluir campos não aplicáveis com justificativa quando relevante. Evitar preencher um relatório grande para uma mudança pequena.

| Modelo | Quando usar | Destino habitual |
| --- | --- | --- |
| [Trabalho](issue.md) | Funcionalidade, design, infraestrutura ou documentação | Corpo de Issue |
| [Bug](bug.md) | Comportamento observado diferente do esperado | Corpo de Issue; dados sensíveis em canal adequado |
| [Pesquisa](pesquisa.md) | Pergunta ou comparação ainda sem solução aprovada | Corpo de Issue; resultados nos comentários |
| [Comparação](comparacao.md) | Escolha relevante de produto, experiência, arquitetura, tecnologia ou infraestrutura | Comentário ou documento oficial vinculado à pesquisa/decisão |
| [Índice da Issue](indice-da-issue.md) | Assunto com várias decisões, estados ou evidências | Corpo da Issue responsável, com links para o detalhe |
| [Decisão](decisao.md) | Proposta, aprovação ou substituição de escolha relevante | Documento de decisão ou comentário declarado como fonte oficial |
| [PR](pull-request.md) | Alteração revisável em arquivos | Descrição de PR |
| [Handoff](handoff.md) | Troca de executor, ferramenta ou responsabilidade | Comentário ou documento indicado pela Issue |
| [Checkpoint](checkpoint.md) | Pausa e retomada de um recorte | Registro curto no local escolhido pelo projeto |
| [Instruções para agentes](instrucoes-para-agentes.md) | Configurar leitura, execução e prestação de contas | Mecanismo de instruções realmente suportado pelo ambiente |

Para um trabalho simples, usar o modelo de Issue e o fechamento com evidência; acrescentar PR se houver alteração de arquivos. O índice, decisão e handoff são usados quando necessários, sem duplicar o mesmo conteúdo em várias fontes.

## Uso como templates do GitHub

Os arquivos `issue.md`, `bug.md` e `pesquisa.md` têm cabeçalho YAML com `name`, `about` e `title`. Podem ser copiados e adaptados para `.github/ISSUE_TEMPLATE/` no repositório do produto. Não carregam labels, responsáveis ou tipos presumidos. Conferir a configuração e a visualização no repositório antes de declarar o seletor funcionando.

O modelo de PR pode ser adaptado para `.github/pull_request_template.md`. Este repositório usa um template curto específico para sua própria manutenção, apontando para o modelo genérico. Publicar uma pasta de modelos não configura outros repositórios automaticamente.

Conferir as [instruções oficiais do GitHub](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/about-issue-and-pull-request-templates). Ao adaptar um template existente, preservar os campos usados por automações ou atualizar seus consumidores de forma explícita.

[Governança](../governanca.md) · [Trabalho no GitHub](../trabalho-no-github.md) · [Handoffs](../handoffs.md) · [Voltar ao guia](../../README.md)

## Documento principal do produto

O [modelo de projeto](projeto.md) é a saída acumulada padrão em `docs/PROJETO.md` do produto. Os outros modelos servem como formatos de registro: decisão e comparação podem ser blocos da seção pertinente; checkpoint e handoff podem compor a seção 16. Não exigem arquivos separados. Issue, bug e pesquisa continuam formatos para o GitHub; registrar links reais quando publicados. Materiais existentes mantêm autoridade até migração explícita.
