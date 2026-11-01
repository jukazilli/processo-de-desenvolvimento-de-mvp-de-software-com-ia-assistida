# Exemplo de ativação e primeira saída

> Simulação documental. Não houve pesquisa de mercado, entrevistas, acesso a um produto, aprovação externa ou execução de software.

## Entrada: ideia e discovery

```text
Estou trabalhando em uma plataforma de adoção de pets.
Consuma o processo em https://github.com/jukazilli/processo-de-desenvolvimento-de-mvp-de-software-com-ia-assistida
para iniciar o discovery.
```

## Comportamento esperado

A IA lê o processo, avalia brevemente os materiais e entra na etapa 02. Não responde somente “carregado”, não exige repositório para analisar e não escolhe funcionalidades sem base. Pode responder: “Vou começar pelo problema e pelas pessoas envolvidas. Por enquanto tenho apenas sua ideia; vou separar hipóteses de achados e preparar a seção de discovery para revisão. Você pretende atender uma região específica e já possui materiais ou contatos de quem participa das adoções?”

Antes ou junto das perguntas, ela explicita o objetivo conhecido, hipóteses iniciais e uma investigação útil, sem fingir que pesquisou. Uma análise parcial não é conclusão da etapa. O [documento ilustrativo](PROJETO.md) mostra a saída no mesmo artefato, com seções 01, 02, fontes e continuidade.

## Entrada: materiais existentes e etapa 04

```text
Considere os requisitos aprovados e as referências no repositório do meu produto.
Use o mesmo processo para executar a etapa 04.
```

No uso real, fornecer o link acessível. A IA confere escopo e materiais, aproveita o que estiver suficiente e entrega a seção 04 de `docs/PROJETO.md` desse produto. Se o link não foi fornecido ou não abre, informa o impedimento; não afirma ter lido requisitos. Continua apenas o que puder analisar sem inventá-los.

## Revisão e persistência

“Pode registrar essa proposta como rascunho no meu repositório” autoriza salvar esse estado, não aprovar o produto. “Aprovo o recorte descrito e autorizo consolidá-lo” pode aprovar e autorizar o registro no mesmo ato. Alterações materiais continuam pedindo decisão pertinente; sem escrita autorizada, a seção fica apresentada, ainda não salva no produto.

[Processo](../../README.md) · [Explicações](../../docs/como-usar.md)
