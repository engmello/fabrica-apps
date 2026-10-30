---
description: Abre um novo app no processo (E0.1 + E0.2) — sigla, pasta, registro e ficha da ideia
argument-hint: <SIGLA> <nome do app> — <ideia em uma frase>
---

Use a skill `processo-apps` e execute as etapas **E0.1** e **E0.2** para: $ARGUMENTS

1. Se faltar sigla (3 letras), nome ou a ideia, pergunte antes de criar qualquer coisa.
2. Confira se a pasta `apps/<sigla-minúscula>-app/` já existe. Se existir, pare e avise.
3. Crie a estrutura:
   ```
   apps/<sigla>-app/docs/
   ├── registro.md            (template T07, preenchido com sigla, nome, data de hoje e fase F0)
   ├── portoes.md             (template T05)
   ├── F1-validar/entrevistas/
   ├── F2-planejar/
   ├── adr/                   (copie template-repo/docs/adr/000-template.md)
   ├── legal/
   ├── F4-lancar/
   └── releases/
   ```
4. Crie `docs/F1-validar/<SIGLA>-T01-ficha-ideia.md` a partir do T01, preenchendo problema, público e
   hipótese em rascunho com o que foi informado (marque o que for suposição).
5. Pergunte quem é o dono do produto e o construtor, se não souber, e preencha no registro.
6. No registro, marque E0.1 e E0.2 como `Concluída` com a data e o link das saídas.
7. Termine dizendo: a próxima etapa é **E1.1 · Hipótese e suposições** (`/etapa E1.1`) e o lembrete
   de criar a etiqueta da sigla no quadro e o cartão na coluna "Ideias".
8. Se estiver num repositório git, faça um commit com a mensagem `<SIGLA>: abre o app (E0.1, E0.2)` e,
   numa sessão na nuvem, envie a branch para o GitHub para que a equipe veja.
