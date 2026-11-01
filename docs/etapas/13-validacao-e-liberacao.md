# 13. Validar em pré-produção e liberar

**Objetivo:** Conferir o candidato em condições representativas e liberar uma versão cuja qualidade e limites sejam conhecidos.

## Entradas

- Candidato identificado, critérios de aceite e evidências da implementação.
- Ambiente, dados de teste seguros, autorizações e plano de retorno.

## Como realizar

1. Executar as verificações aplicáveis: formatação, análise de código, tipos, testes, build, dados, segurança, dependências, segredos, limites arquiteturais e consistência documental.
2. Validar jornadas, acessibilidade, aparência e integrações críticas em ambiente representativo; registrar condições e limitações.
3. Conferir migrações, backup e recuperação pertinentes, riscos residuais e monitoramento da liberação.
4. Apresentar evidências e pendências ao responsável pela liberação; obter a autorização aplicável ao ambiente e risco.
5. Promover, sempre que possível, o mesmo artefato ou commit validado. Se o candidato mudar, revalidar as partes afetadas antes da liberação.
6. Confirmar a versão em execução e sua saúde, atualizar os vínculos e registrar o que foi implementado, testado, validado e liberado.

## Pesquisa, comparação e verificação

**Validar o candidato e as condições.** Comparar o resultado observado aos critérios de aceite e risco. Registrar candidato, ambiente, dados, método e limites. Referências públicas e resultados de outro ambiente não comprovam segurança, acessibilidade, desempenho ou liberação deste candidato.

Aplicar a [comparação de referências](../pesquisa-e-benchmarking.md) e os [controles de verificação com IA](../verificacao-com-ia.md). O registro pode aproveitar uma decisão ou Issue existente; uma pesquisa externa nova só se justifica pela dúvida e pelo impacto.

## O que registrar

- Relatório de evidências e decisões de aceite.
- Versão liberada ou impedimento explícito, com plano de correção.
- Plano operacional de acompanhamento e retorno seguro.

## Critério de conclusão

Os critérios de liberação foram atendidos ou as exceções foram aceitas pelo responsável, com evidência acessível e estado real registrado.

## Aproveitar ou não aplicar

Um estudo sem lançamento pode concluir em ambiente local ou protótipo; registrar esse limite. Se não existir pré-produção separada, declarar condições substitutas, riscos e aprovação, sem alegar validação em ambiente inexistente.

## Transferência para a próxima atividade

Transferir à operação a versão, mudanças, riscos, monitoramento, suporte e procedimentos de recuperação. Falhas abrem ou atualizam Issues e retornam à etapa pertinente.

Registrar a passagem para operação pelo [modelo de handoff](../modelos/handoff.md), distinguindo estado do trabalho, aprovação, GitHub e comprovação de execução.

Aplicar as [regras do processo](../regras-do-processo.md). O formato do registro pode ser um documento, Issue ou atualização de material existente, conforme a fonte oficial escolhida para o assunto. O número da etapa não obriga criar um arquivo com esse número.

---

[Voltar ao guia](../../README.md) · [Etapa anterior](12-desenvolvimento-incremental.md) · [Próxima etapa](14-operacao-e-aprendizado.md)
