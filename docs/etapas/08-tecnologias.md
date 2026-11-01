# 08. Escolher e validar as tecnologias

**Objetivo:** Definir com quais tecnologias a arquitetura será implementada e quais regras orientam seu uso.

## Entradas

- Arquitetura, requisitos de qualidade, padrões de código e necessidades de interface.
- Tecnologias existentes, versões instaladas, licenças e restrições da organização.

## Como realizar

1. Escolher ou validar linguagens, ambientes de execução, frameworks, bibliotecas por responsabilidade e ferramentas de desenvolvimento.
2. Conferir documentação oficial atual, suporte, versões compatíveis, manutenção, segurança e licença nas decisões relevantes.
3. Comparar opções de acordo com o contexto: legibilidade, testes, desempenho, operação, equipe, custo de atualização e dependência de fornecedor.
4. Definir onde cada biblioteca pode ser usada. Preferir recursos da plataforma e soluções já aprovadas quando suficientes; justificar duplicações necessárias.
5. Registrar política de versões e compatibilidade; o arquivo de dependências travadas — lockfile — registra o conjunto exato instalado.
6. Reabrir decisões afetadas se uma tecnologia exigir mudança arquitetural; não adaptar documentos silenciosamente para justificar uma preferência.

## O que registrar

- Conjunto de tecnologias aprovado e justificado.
- Regras de uso, compatibilidade, versões ou política de atualização.
- Alternativas rejeitadas relevantes e itens de preparação técnica.

## Critério de conclusão

O executor consegue configurar o projeto sem precisar escolher novamente linguagens, ferramentas centrais e bibliotecas de responsabilidade já definida.

## Aproveitar ou não aplicar

Em projeto existente, verificar versões e capacidade antes de propor troca. Não atualizar dependências ou substituir frameworks por conveniência da IA.

## Transferência para a próxima atividade

Entregar escolhas à infraestrutura e transformar configuração e verificações em Issues de preparação.

## Orientação detalhada

Consultar o capítulo de [escolha das tecnologias](../praticas/tecnologias.md) para as regras e exemplos aplicáveis. Esse capítulo aprofunda a etapa; ele não cria uma etapa adicional.

Aplicar as [regras do processo](../regras-do-processo.md). O formato do registro pode ser um documento, Issue ou atualização de material existente, conforme a fonte oficial escolhida para o assunto. O número da etapa não obriga criar um arquivo com esse número.

---

[Voltar ao guia](../../README.md) · [Etapa anterior](07-arquitetura.md) · [Próxima etapa](09-infraestrutura.md)
