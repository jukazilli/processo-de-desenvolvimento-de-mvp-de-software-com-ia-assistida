# 07. Desenhar a arquitetura da solução

**Objetivo:** Escolher uma estrutura que atenda às necessidades técnicas com complexidade justificável.

## Entradas

- Requisitos de produto, experiência e qualidade.
- Estrutura existente, integrações e decisões técnicas aprovadas.

## Como realizar

1. Descrever contexto, aplicações, módulos, dados, contratos, integrações, limites de confiança e dependências.
2. Comparar alternativas quando a decisão for relevante; explicitar consequências, custos, riscos e adequação à equipe.
3. Definir a organização do repositório: simples, monorepo ou múltiplos repositórios, conforme compartilhamento e independência necessários.
4. Registrar decisões significativas, incluindo opções rejeitadas e condições para reavaliar. Um registro de decisão arquitetural — ADR — pode cumprir essa função.
5. Transformar limites importantes em regras verificáveis quando possível: importações, acesso a dados, autorização e separação entre cliente e servidor.
6. Produzir restrições para a escolha de tecnologias e necessidades para infraestrutura, sem escolher padrões por preferência do agente.

## O que registrar

- Visão da solução e limites claros.
- Decisões arquiteturais com contexto, alternativas e consequências.
- Entradas técnicas para tecnologias, infraestrutura e verificações.

## Critério de conclusão

Outro engenheiro compreende os módulos, suas responsabilidades, dependências e critérios de escolha das tecnologias.

## Aproveitar ou não aplicar

Se a arquitetura atual atende à mudança, registrar a conferência e as partes afetadas. Não redesenhar o sistema inteiro para uma alteração localizada. Divergência real exige decisão registrada.

## Transferência para a próxima atividade

Encaminhar estrutura e restrições à etapa 08 e necessidades operacionais à etapa 09; registrar decisões sem solução no backlog de pesquisa.

## Orientação detalhada

Consultar o capítulo de [engenharia e arquitetura](../praticas/arquitetura.md) para as regras e exemplos aplicáveis. Esse capítulo aprofunda a etapa; ele não cria uma etapa adicional.

Aplicar as [regras do processo](../regras-do-processo.md). O formato do registro pode ser um documento, Issue ou atualização de material existente, conforme a fonte oficial escolhida para o assunto. O número da etapa não obriga criar um arquivo com esse número.

---

[Voltar ao guia](../../README.md) · [Etapa anterior](06-qualidade-e-riscos.md) · [Próxima etapa](08-tecnologias.md)
