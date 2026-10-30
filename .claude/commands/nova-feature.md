---
description: Ciclo completo de uma funcionalidade — spec, testes, código, revisão
argument-hint: <id ou descrição da tarefa>
---

Execute o ciclo de funcionalidade para: $ARGUMENTS

1. Use o agente `produto` para escrever a mini-spec da tarefa (a partir do backlog ou do PRD em `docs/prd.md`).
   Mostre a spec e **pare para eu aprovar** antes de continuar.
2. Após minha aprovação, use o agente `desenvolvedor` para implementar em branch própria,
   com testes primeiro e o evento de analytics previsto.
3. Use o agente `revisor` para revisar o branch.
4. Me entregue: link/nome do branch, resumo do PR, parecer do revisor e a lista de áreas críticas
   cujo diff eu preciso ler pessoalmente.

Não faça push nem merge sem minha confirmação.
