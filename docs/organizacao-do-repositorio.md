# Três responsabilidades separadas

| Local | Público e função | Autoridade |
| --- | --- | --- |
| `README.md` | Entrada da IA: ativação, condução, 14 contratos de etapa e saídas | Framework operacional principal |
| `framework/` | Módulos operacionais e modelos carregados conforme a tarefa | Detalhamento das regras e formatos; ativação e saída padrão vêm do README |
| `docs/` | Pessoas: propósito, uso, revisão, termos, fontes e histórico | Explicação do método, sem outro fluxo de execução |
| `examples/` | Demonstrações fictícias | Material didático, sem aprovação ou execução real presumidas |
| `docs/PROJETO.md` no produto | Conhecimento produzido pela execução do método | Documento principal do produto, com índice e fontes oficiais existentes |

O arquivo `AGENTS.md` da raiz orienta a manutenção **deste repositório**. Ele não é a ativação de um produto do usuário. Instruções locais de outros ambientes precisam ser adaptadas e verificadas, sem instalação presumida.

## Compatibilidade de caminhos

Caminhos anteriores em `docs/praticas/`, `docs/modelos/`, regras, governança e uso com IA permanecem como páginas explicativas com link ao destino operacional. Os consumidores antigos continuam encontrando o assunto. IDs de requisitos, chaves de templates e rótulos de relatório permanecem nos módulos correspondentes. Publicar os destinos não comprova atualização de habilidades privadas de uma máquina.

As páginas de etapas em `docs/etapas/` explicam o que revisar e apontam para o contrato da mesma etapa no README; não mantêm uma segunda lista de ações da IA. Histórico de reorganização permanece identificado como histórico.

[Documentação](README.md) · [Processo](../README.md)
