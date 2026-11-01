# 11. Preparar a fundação do projeto

**Objetivo:** Criar ou conferir uma base técnica utilizável para desenvolver, testar e implantar o que foi planejado.

## Entradas

- Issues de preparação, decisões técnicas e plano de infraestrutura.
- Acesso autorizado a ambientes e ações humanas pendentes identificadas.

## Como realizar

1. Conferir o repositório e versões, ferramentas, dependências aprovadas e configuração local reproduzível.
2. Configurar as automações de qualidade e entrega adequadas ao projeto.
3. Preparar serviços, dados, migrações, autenticação, mídia e processamento necessários, com separação entre cliente e servidor e entre ambientes.
4. Guardar segredos nos mecanismos próprios do ambiente. Não pedir senhas, chaves privadas, códigos de recuperação ou dados de cartão no chat.
5. Encaminhar login, MFA, CAPTCHA, aceite legal e ações sensíveis ao humano pelo mecanismo da ferramenta. Se houver bloqueio, registrar instruções seguras para conclusão.
6. Executar verificações básicas do ambiente, migrações, acesso, implantação, observabilidade e recuperação conforme aplicável; registrar resultado e limitações.

## O que registrar

- Ambiente configurado e verificável, com instruções reproduzíveis.
- Evidências da primeira implantação técnica e verificações aplicáveis.
- Pendências e exceções de preparação explicitadas nas Issues.

## Critério de conclusão

A base permite executar o próximo item com segurança e evidência. Criar contas ou pastas, sozinho, não prova prontidão operacional.

## Aproveitar ou não aplicar

Em projeto existente, conferir a base afetada e preparar apenas lacunas. Uma entrega pode começar com parte da preparação em paralelo se dependências e risco forem explicitamente aceitos.

## Transferência para a próxima atividade

Transferir ao executor da etapa 12 versões, acessos seguros, comandos, decisões, evidências e limitações reais.

## Orientação detalhada

Consultar o capítulo de [infraestrutura](../praticas/infraestrutura.md) para as regras e exemplos aplicáveis. Esse capítulo aprofunda a etapa; ele não cria uma etapa adicional.

Aplicar as [regras do processo](../regras-do-processo.md). O formato do registro pode ser um documento, Issue ou atualização de material existente, conforme a fonte oficial escolhida para o assunto. O número da etapa não obriga criar um arquivo com esse número.

---

[Voltar ao guia](../../README.md) · [Etapa anterior](10-trabalho-no-github.md) · [Próxima etapa](12-desenvolvimento-incremental.md)
