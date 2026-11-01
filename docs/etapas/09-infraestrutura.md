# 09. Planejar infraestrutura, custos e segurança

**Objetivo:** Planejar onde a solução roda, como é operada e quais condições de custo e acesso se aplicam.

## Entradas

- Arquitetura, tecnologias e necessidades operacionais.
- Orçamento, ambientes, contas, fornecedores e permissões existentes.

## Como realizar

1. Esclarecer objetivo, escala, dados, disponibilidade, preferência por ambiente local ou remoto e tolerância a complexidade e custo.
2. Comparar serviços adequados e conferir fontes oficiais atuais para preço, limites, regiões, compatibilidade, segurança e restrições de produção.
3. Mapear serviços de aplicação, dados, autenticação, mídia, processamento, observabilidade, entrega e recuperação que forem necessários.
4. Definir segregação de ambientes, credenciais, exposição pública/privada, acesso mínimo, backups, recuperação e retorno de versão.
5. Informar limites da camada gratuita e condições de cobrança. Contratação, upgrade ou recurso potencialmente cobrável exigem autorização explícita do responsável.
6. Planejar a configuração por API, CLI, infraestrutura como código ou conector autorizado; usar automação de navegador ou instrução manual segura quando necessário.

## O que registrar

- Plano de ambientes e serviços compatíveis, com custos datados, limites e riscos.
- Plano de implantação, monitoramento e recuperação.
- Issues de configuração, dependências e ações humanas necessárias.

## Critério de conclusão

A infraestrutura está planejada de modo executável, com autorizações e dependências claras. A existência do plano não comprova que os ambientes já foram criados ou validados.

## Aproveitar ou não aplicar

Aproveitar infraestrutura existente se atender aos requisitos. Execução só local ou pré-produção simplificada pode ser adequada ao objetivo; registrar limites e risco da escolha.

## Transferência para a próxima atividade

Transferir plano e ações autorizadas para a etapa 10 e execução na etapa 11. Limitação que impacta tecnologia ou arquitetura retorna à decisão correspondente.

## Orientação detalhada

Consultar o capítulo de [infraestrutura](../praticas/infraestrutura.md) para as regras e exemplos aplicáveis. Esse capítulo aprofunda a etapa; ele não cria uma etapa adicional.

Aplicar as [regras do processo](../regras-do-processo.md). O formato do registro pode ser um documento, Issue ou atualização de material existente, conforme a fonte oficial escolhida para o assunto. O número da etapa não obriga criar um arquivo com esse número.

---

[Voltar ao guia](../../README.md) · [Etapa anterior](08-tecnologias.md) · [Próxima etapa](10-trabalho-no-github.md)
