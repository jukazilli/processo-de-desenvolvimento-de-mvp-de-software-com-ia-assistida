---
document_id: DOC-09
title: Rastreabilidade sem uma segunda fila
status: fictional-example
version: 2.0.0
---

# Rastreabilidade sem uma segunda fila

> Demonstração fictícia. Nenhuma Issue, PR, implementação ou evidência de teste do produto foi criada. Os identificadores abaixo são contratos didáticos, não números reais de Issues no GitHub.

## Uma cadeia de vínculos por atividade

Requisito/decisão na fonte oficial; Issue com aceite e dependências; PR e commit para a mudança; testes e evidência ligados ao candidato. A Issue aponta para cada um. O [catálogo de critérios](issues-e-criterios.md) demonstra os 29 IDs preservados, sem tabela operacional concorrente neste arquivo.

| Exemplo | Fonte e aceite | Vínculos a preencher na adoção |
| --- | --- | --- |
| FND-001 — Estrutura | DOC-07 e critérios FND-001 | Issue real, PR, commit e revisão da árvore |
| TEN-003 — Isolamento do gestor | DOC-02, DOC-05, ENG-001/008 e aceite TEN-003 | Issue, implementação, teste negativo de leitura/mutação e resultado no candidato |
| LRN-001 — Próxima atividade | Princípios, DOC-04, DOC-05 e aceite LRN-001 | Issue, asset versionado, aprovação de design, PR e evidência da jornada |

## Quatro informações diferentes

| Dimensão | Exemplo ilustrativo de preenchimento | O que não comprova |
| --- | --- | --- |
| Operação | Em revisão | Aprovação de produto ou funcionamento |
| Decisão | Design aprovado para a próxima versão; link da aprovação | Backend implementado ou versão já disponível |
| Issue/PR | Issue aberta; PR em rascunho | Merge ou liberação |
| Execução e evidência | Código ainda não implementado; testes não executados; liberação pendente | Não preencher com “passou” por haver um plano |

Na execução, estados reais ficam nas Issues/Projects e PRs; a fonte oficial mantém a regra. Uma pesquisa pode estar Feito no próprio escopo com recomendação pendente de decisão; implementação ou release continuam em trabalho separado.

## Revisão de consistência

- Feito exige aceite, evidência e consolidação documental aplicáveis ao escopo.
- Código divergente da decisão exige resolução explícita, não alteração retroativa da intenção.
- Tecnologia ou fornecedor divergente exige reconciliação com a fonte responsável.
- Mudança de requisito atualiza fonte e vínculos das Issues afetadas.
- Resultado referencia execução, versão e condições reais; um campo vazio não significa aprovado.
- Se houver necessidade de relatório, gerar visão datada dos vínculos, indicando origem e limite; não editar outro status em paralelo.

[Índice](README.md) · [Trabalho no GitHub](../../docs/trabalho-no-github.md)
