# 06. Definir requisitos de qualidade e riscos

**Objetivo:** Tornar explícito o que o sistema precisa suportar e como sua qualidade será verificada.

## Entradas

- Escopo, experiência, dados envolvidos, restrições e contexto operacional.
- Código, padrões e resultados de qualidade existentes, quando houver.

## Como realizar

1. Definir volume esperado, picos, perfis de leitura/escrita, disponibilidade, latência, consistência, falhas, tempo real, uso sem rede e processamento assíncrono conforme o caso.
2. Avaliar dados pessoais e sensíveis, autenticação, autorização, separação de acesso, privilégios mínimos, retenção, recuperação e exigências regulatórias aplicáveis.
3. Considerar tamanho da equipe, manutenção, operação, suporte e capacidade de evolução. Identificar premissas e risco residual.
4. Definir práticas de desenvolvimento: código legível, nomes, idioma técnico, reutilização, dependências, tratamento de erro, desempenho, migrações e revisão.
5. Planejar testes unitários, integração, contratos, segurança, acessibilidade e jornadas críticas proporcionalmente aos riscos. Correções recorrentes devem deixar prevenção verificável quando viável.
6. Definir verificações obrigatórias, critério de conclusão e evidência esperada. Não adiar estratégia de teste para a etapa final.

## Pesquisa, comparação e verificação

**Escolher critérios de qualidade verificáveis.** Usar padrões pertinentes como WCAG, OWASP ASVS e NIST SSDF para formular requisitos e verificações, fixando versões e escopo. Não declarar conformidade por citar uma norma; ligar cada afirmação relevante à evidência que poderá comprová-la.

Aplicar a [comparação de referências](../pesquisa-e-benchmarking.md) e os [controles de verificação com IA](../verificacao-com-ia.md). O registro pode aproveitar uma decisão ou Issue existente; uma pesquisa externa nova só se justifica pela dúvida e pelo impacto.

## O que registrar

- Requisitos de qualidade identificados e verificáveis.
- Padrões de desenvolvimento e estratégia de testes.
- Riscos, responsáveis, critérios de aceitação e exceções aprovadas.

## Critério de conclusão

Qualidade e segurança deixam de ser adjetivos vagos: o projeto sabe o que verificar, sob quais condições e com qual evidência.

## Aproveitar ou não aplicar

Conferir requisitos e padrões existentes, alterando apenas o necessário. Uma mudança pequena pode adotar os critérios já aprovados e acrescentar um caso de regressão; não precisa gerar novo plano completo.

## Transferência para a próxima atividade

Transferir para arquitetura as exigências que influenciam estrutura e para execução os critérios de revisão e teste.

## Orientação detalhada

Consultar o capítulo de [padrões de desenvolvimento](../praticas/desenvolvimento.md) para as regras e exemplos aplicáveis. Esse capítulo aprofunda a etapa; ele não cria uma etapa adicional.

Aplicar as [regras do processo](../regras-do-processo.md). O formato do registro pode ser um documento, Issue ou atualização de material existente, conforme a fonte oficial escolhida para o assunto. O número da etapa não obriga criar um arquivo com esse número.

---

[Voltar ao guia](../../README.md) · [Etapa anterior](05-interface-ui.md) · [Próxima etapa](07-arquitetura.md)
