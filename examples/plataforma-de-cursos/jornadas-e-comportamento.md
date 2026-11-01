---
document_id: DOC-05
title: Jornadas e comportamento
status: fictional-example
version: 2.0.0
depends_on:
  - DOC-02
  - Principios_de_UX_UI
---

# Jornadas e comportamento

> **Estudo fictício, versão 2.0.** Requisitos, decisões, aprovações e cenários abaixo são ilustrativos. Nenhuma aplicação, pesquisa com usuários, contratação, implantação ou teste deste produto foi executado. Consulte o [índice e a autoridade de cada assunto](README.md).

## Jornada 1 — Criar cliente e preparar implantação

**Passos ilustrativos:**

1. Consultor abre Empresas.
2. Criar empresa.
3. Informar dados essenciais.
4. Selecionar módulos do software corporativo contratados.
5. Salvar.
6. Empresa criada.
7. Próxima ação sugerida: criar turma ou convidar gestor.

### Exceções

- empresa duplicada: avisar antes de concluir;
- erro de rede: preservar campos quando possível;
- sem permissão: bloquear antes de exibir formulário editável.

---

## Jornada 2 — Criar turma e atribuir trilha

**Passos ilustrativos:**

1. Abrir empresa.
2. Criar turma.
3. definir nome/período/instrutor.
4. selecionar público/perfis.
5. regra de atribuição sugere trilhas compatíveis.
6. consultor revisa.
7. confirma turma.
8. convites / matrículas.

A sugestão de trilha não pode ocultar quais critérios foram usados.

---

## Jornada 3 — Primeiro acesso do aluno

**Passos ilustrativos:**

1. Recebe convite.
2. abre link.
3. autentica / cria credencial conforme método aprovado.
4. aceita acesso à empresa/turma.
5. vê Minha trilha.
6. identifica próxima atividade.

### Estado sem conteúdo

Se ainda não houver trilha atribuída, explicar que o treinamento está sendo preparado; não mostrar tela vazia genérica.

---

## Jornada 4 — Consumir aula

**Passos ilustrativos:**

1. Minha trilha.
2. Continuar treinamento.
3. aula atual.
4. consome vídeo/texto/material.
5. marca ou sistema registra conclusão conforme regra.
6. próxima atividade.

Se houver pré-requisito não concluído, mostrar qual etapa falta e oferecer caminho direto para ela.

---

## Jornada 5 — Realizar quiz

**Sequência e alternativas ilustrativas:**

- Abrir avaliação
- ler instruções
- responder questões
- revisar quando permitido
- enviar
- resultado
- Se aprovado, seguir para a próxima etapa.
- Caso contrário, orientar revisão ou nova tentativa conforme a política.

Erros de envio não podem apagar respostas já preenchidas quando tecnicamente evitável.

---

## Jornada 6 — Tarefa prática

### Beta

**Passos ilustrativos:**

1. Aluno recebe instrução prática.
2. executa atividade no ambiente apropriado do software corporativo.
3. registra conclusão / evidência permitida.
4. se validação manual for exigida.
5. instrutor recebe pendência.
6. aprova ou devolve com orientação.

O Beta não consulta automaticamente o software corporativo para validar a ação.

---

## Jornada 7 — Gestor acompanha equipe

**Passos ilustrativos:**

1. Gestor entra.
2. vê somente sua empresa.
3. Equipe / Progresso.
4. filtra por turma ou trilha.
5. identifica não iniciados / em andamento / concluídos.

O gestor não deve acessar dados de outras empresas nem recursos de autoria de conteúdo.

---

## Jornada 8 — Consultor identifica bloqueio

**Passos ilustrativos:**

1. Acompanhamento.
2. lista prioriza atrasos / tarefas pendentes.
3. consultor abre aluno ou turma.
4. vê contexto do bloqueio.
5. executa ação permitida:.
6. orientar.
7. reabrir tentativa, se política permitir.
8. validar tarefa.
9. ajustar matrícula.

O produto informa o sinal; a decisão de implantação continua humana.

---

## Jornada 9 — Conclusão e certificado

1. Ao concluir o último requisito, o sistema confere os critérios da trilha.
2. Se faltar algum requisito, mostra a pendência concreta.
3. Se houver elegibilidade, gera o registro de conclusão e disponibiliza o certificado.
4. Notifica o aluno quando aplicável.

## Histórias de uso prioritárias

### LRN-01

Como aluno, quero abrir o AVA e ver minha próxima atividade para continuar o treinamento sem procurar manualmente o curso correto.

### CON-01

Como consultor, quero configurar os módulos contratados por uma empresa para que as trilhas atribuídas reflitam a implantação real.

### MGR-01

Como gestor do cliente, quero acompanhar o progresso da minha equipe para saber quem ainda precisa concluir treinamento.

### ASM-01

Como instrutor, quero validar uma tarefa prática quando ela exigir conferência humana para registrar a conclusão corretamente.

### CERT-01

Como aluno, quero obter meu certificado quando cumprir os critérios definidos para comprovar a conclusão.

## Reentrada e retomada

Ao voltar para a plataforma, o usuário deve recuperar contexto de forma previsível:

- aluno retorna à próxima atividade pendente;
- consultor retorna à empresa/turma recentemente trabalhada quando seguro;
- formulários não salvos devem alertar antes de abandono quando houver risco de perda.

## Acessibilidade comportamental

- ações não dependem exclusivamente de cor;
- foco de teclado deve acompanhar modais e confirmações;
- vídeos devem suportar legendas quando o conteúdo as fornecer;
- mensagens de erro devem apontar campo e correção;
- timers, se existirem futuramente, não podem ser única forma de concluir tarefa sem necessidade pedagógica.
