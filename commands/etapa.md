---
description: Executa uma etapa do processo (ex.: /etapa E2.1) seguindo a ficha padrão
argument-hint: <código da etapa, ex.: E2.1> [pasta do app]
---

Use a skill `processo-apps` para executar a etapa: $ARGUMENTS

1. Identifique o app: a pasta informada, ou a pasta atual se tiver `docs/registro.md`.
   Se houver mais de um app possível ou nenhum, pergunte.
2. Leia a ficha da etapa no arquivo da fase (`etapas/`) e mostre em 3 linhas: objetivo, saída e critério de pronto.
3. Leia `docs/registro.md` e verifique:
   - o **gatilho** foi cumprido (etapa anterior ou portão concluído);
   - todas as **entradas** existem.
   Se algo faltar, diga o que falta e qual etapa produz; pergunte se deve seguir mesmo assim
   (se seguir, registre a justificativa no registro).
4. Marque a etapa como `Em andamento` no registro.
5. Execute os **passos** da ficha, delegando ao agente e às skills indicados no campo **IA**.
   Pare para aprovação humana sempre que a ficha disser "aprova", "equipe" ou "confirmação",
   e antes de qualquer ação externa (publicar, enviar, criar tarefas no quadro, mensagens).
6. Gere a **saída** a partir do template indicado, no local padrão.
7. Confira o critério **Pronto quando**:
   - atendido → marque `Concluída` (ou `Em revisão`, se depender de aprovação da equipe), com data e link;
   - não atendido → mantenha `Em andamento` e liste o que falta.
8. Registre uma linha no Diário do registro e diga qual é a próxima etapa e o responsável.

Se o código for de um portão (P1–P5), use o fluxo de `/portao`.
