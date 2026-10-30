---
name: quebrar-tarefas
description: Transforma o PRD em backlog — tarefas de até 1 dia, fatiadas na vertical, com critérios de aceite, evento de analytics, dependências e prioridade pelo caminho até o momento de valor. Use na Fase 2 ou ao planejar uma nova versão.
---

# Quebrar tarefas

## Regras

1. **Fatia vertical**: cada tarefa entrega algo utilizável de ponta a ponta (tela + API + dados), não
   uma camada técnica ("criar tabelas", "fazer o backend").
2. **Até 1 dia** de trabalho com agentes. Se for maior, divida: caminho feliz primeiro, depois erros,
   depois casos de borda, depois polimento.
3. **Prioridade**: primeiro o caminho mais curto até o momento de valor; depois o que aumenta retenção;
   por último conveniências.
4. Tarefas de **fundação** (setup, autenticação, CI) entram primeiro, mas também pequenas.

## Formato de cada tarefa

```
ID: APP-012
Título: Registrar despesa com valor e categoria
História: H2
Prioridade: P1 (caminho do momento de valor) | P2 | P3
Estimativa: ½ dia | 1 dia
Depende de: APP-008
Critérios de aceite:
- Dado ..., quando ..., então ...
Evento: despesa_registrada {categoria, offline}
Notas: <riscos, links do protótipo>
```

## Saída

- Lista ordenada para as próximas 4–6 semanas, agrupada por semana (máximo de ~5 tarefas/semana para
  uma pessoa).
- Marque tarefas que tocam áreas críticas (autenticação, pagamentos, dados pessoais, migrações).
- Se houver conector do quadro de tarefas (Linear, Jira, GitHub Projects), ofereça criar as tarefas lá;
  crie somente após confirmação.

## Sinais de problema

Tarefa com "e" no título (são duas), tarefa sem critério verificável, mais de 30 tarefas no MVP
(escopo grande demais — volte ao PRD).
