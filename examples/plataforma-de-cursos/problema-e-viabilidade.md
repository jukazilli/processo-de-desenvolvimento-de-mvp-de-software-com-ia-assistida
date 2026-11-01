---
document_id: DOC-01
title: Pesquisa e Viabilidade
status: fictional-example
version: 2.0.0
---

# Pesquisa e Viabilidade

> **Estudo fictício, versão 2.0.** Requisitos, decisões, aprovações e cenários abaixo são ilustrativos. Nenhuma aplicação, pesquisa com usuários, contratação, implantação ou teste deste produto foi executado. Consulte o [índice e a autoridade de cada assunto](README.md).

## Problema observado

A consultoria treina usuários do software corporativo por reuniões ao vivo e distribui materiais por canais diferentes. Depois do treinamento, falta uma fonte única para saber quem recebeu qual conteúdo, quem concluiu, onde houve dificuldade e se o cliente está pronto para operar os módulos contratados.

## Público afetado

- consultores e instrutores da consultoria;
- gestores dos clientes;
- usuários finais do software corporativo;
- responsáveis por implantação e adoção.

## Necessidades principais

1. organizar treinamento por empresa, perfil e módulo contratado;
2. reutilizar conteúdo sem recriar curso para cada cliente;
3. acompanhar progresso individual e da empresa;
4. avaliar conhecimento com quiz e tarefa prática;
5. registrar evidência de conclusão e certificado;
6. permitir que o consultor use progresso como sinal da implantação.

## Alternativas a investigar

Comparar adaptar uma plataforma existente, melhorar o processo atual ou desenvolver uma solução própria. Ainda não houve levantamento de concorrentes nem entrevistas neste cenário; não é possível concluir que construir é a melhor opção. A [comparação de exemplo](comparacao-e-decisao.md) mostra o formato e as lacunas.

A hipótese de especialização combina módulos contratados, função e turma para atribuir uma trilha. Confirmar se isso resolve uma necessidade relevante antes de investir.

## Diferenciação potencial

- trilhas derivadas do contexto da implantação;
- visão da consultoria sobre clientes e turmas;
- visão restrita do gestor do cliente;
- tarefas práticas vinculadas ao uso do software corporativo;
- possibilidade futura de validar automaticamente ações realizadas no software corporativo;
- linguagem e experiência voltadas para implantação de software, não para ensino escolar genérico.

## Hipóteses ainda não validadas

- clientes valorizarão certificado como evidência formal;
- a visão de progresso reduzirá retrabalho de consultoria;
- trilhas por função reduzirão tempo de capacitação;
- no futuro o produto poderá ser vendido para outras empresas de software;
- integração automática com o software corporativo terá retorno suficiente para justificar complexidade.

## Riscos

- tentar reproduzir recursos de LMS maduros sem necessidade;
- ampliar o escopo para marketplace, comunidade, gamificação ou white-label cedo demais;
- integrar com o software corporativo antes de estabilizar o modelo pedagógico;
- custos de vídeo e armazenamento crescerem sem estratégia;
- baixa adesão se o aluno enxergar o AVA como obrigação paralela ao trabalho;
- dados de clientes diferentes serem expostos entre tenants.

## Limitações do primeiro corte

O Beta não deve depender de integração automática com software corporativo ou sistema de gestão externo. Tarefas práticas podem ser declarativas ou validadas pelo instrutor.

## Critérios de viabilidade

O projeto segue como viável se o Beta conseguir:

- atender múltiplas empresas com segregação clara;
- permitir reutilização de conteúdo;
- atribuir trilhas por contexto;
- registrar progresso e avaliação;
- oferecer operação simples para a consultoria;
- iniciar com custo compatível com o estágio do produto;
- preservar caminho de evolução sem antecipar arquitetura excessiva.

## Recomendação provisória

Investigar um Beta limitado à capacitação de usuários. A viabilidade permanece **pendente de pesquisa e validação**, incluindo alternativas, necessidade real, orçamento e isolamento entre empresas. Não há comprovação de demanda ou retorno financeiro.
