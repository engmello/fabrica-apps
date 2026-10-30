---
description: Prepara o dossiê de um portão (P1–P5) com as evidências contra os critérios
argument-hint: <P1|P2|P3|P4|P5> [pasta do app]
---

Use a skill `processo-apps` e o agente `produto` para preparar o portão: $ARGUMENTS

1. Leia os critérios do portão na ficha da fase e em `docs/portoes.md`.
2. Confira no `docs/registro.md` se todas as etapas que antecedem o portão estão concluídas.
3. Leia as saídas dessas etapas e monte o dossiê:

```
## Dossiê — <Portão> — <SIGLA> — <data>
### Critérios
| Critério | Evidência (com link) | Atendido? |
### Pontos de atenção
### Riscos se seguir / se não seguir
### Recomendação do agente: <opção> — <justificativa em 2 frases>
### Opções da equipe: <as saídas possíveis deste portão>
```

4. Salve como `docs/dossies/<portao>-<data>.md` e marque o portão `Em revisão` no registro.
5. **Não registre a decisão.** Ela é da equipe. Depois da reunião, se o usuário informar a decisão,
   registre-a em `docs/portoes.md` exatamente como informada (data, participantes, decisão,
   justificativa, próximos passos), marque o portão `Concluída` e indique a próxima etapa conforme a decisão.
