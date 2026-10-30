---
name: processo-apps
description: Processo padronizado da equipe para levar um app da ideia ao encerramento — 34 etapas (IF.1–IF.4, E0.1–E5.6), 5 portões (P1–P5) e 14 templates (T01–T14). Use sempre que o trabalho envolver abrir um app, executar ou checar uma etapa, preparar um portão, ver o status de um app, ou quando alguém mencionar um código de etapa, portão ou template.
---

# Processo de apps — v1.0

Todo app passa pelas mesmas etapas, produz os mesmos artefatos e é decidido nos mesmos portões.
O que muda de um app para outro é o conteúdo, nunca o caminho.

## Onde está cada coisa (relativo à pasta desta skill)

- `etapas/` — a ficha de cada etapa, um arquivo por fase:
  `IF-implantacao.md`, `F0-abertura.md`, `F1-validar.md`, `F2-planejar.md`, `F3-criar.md`, `F4-lancar.md`, `F5-evoluir.md`
- `templates/` — `T01-ficha-ideia.md` … `T14-acordo-equipe.md`
- `template-repo/` — arquivos copiados para o repositório do app no E3.1 (CLAUDE.md, CI, settings, docs)

## Onde ficam os dados de cada app

Cada app vive em uma pasta `<sigla>-app/` (ex.: `fin-app/`), que nasce no E0.2 e vira o repositório no E3.1:

```
<sigla>-app/
├── docs/
│   ├── registro.md          # T07: status de todas as etapas — a fonte para /status
│   ├── portoes.md           # T05
│   ├── F1-validar/          # T01 ficha, T02 entrevistas (sem nomes reais)
│   ├── prd.md               # T03
│   ├── metricas.md          # T04
│   ├── F2-planejar/         # T08 teste de protótipo
│   ├── arquitetura.md       # T09
│   ├── adr/
│   ├── legal/               # T10
│   ├── F4-lancar/           # T11, T12, T13
│   └── releases/            # T06 por versão: release-x.y.z.md
└── (código, a partir do E3.1)
```

## Como executar uma etapa

1. Leia a ficha da etapa no arquivo da fase.
2. Leia `docs/registro.md` e confira: a etapa anterior (gatilho) está concluída e as **entradas** existem?
   Se faltar algo, diga o que falta e qual etapa produz — não invente entradas.
3. Siga os **passos** da ficha, usando o agente/skill indicado no campo **IA**.
4. Produza a **saída** a partir do template indicado, no local padrão acima. Nome: `<SIGLA>-<Txx>-<descrição>-v<n>` quando for um arquivo avulso.
5. Verifique o critério **Pronto quando**. Só marque concluída se for atendido.
6. Atualize `docs/registro.md`: status, data e link da saída. Status válidos:
   `Não iniciada` · `Em andamento` · `Em revisão` · `Concluída` · `Pulada` (exige justificativa).
7. Diga qual é a próxima etapa e quem é o responsável.

## Regras invioláveis

- Nenhuma etapa é pulada sem justificativa escrita no registro.
- Só se avança de fase por um portão com decisão **registrada pela equipe** em `docs/portoes.md`.
  O Claude prepara o dossiê e recomenda; nunca registra a decisão sozinho.
- Etapas marcadas ↻ se repetem; registre cada execução relevante (ex.: entrevistas feitas, versões publicadas).
- Nunca grave dados pessoais reais (nomes, e-mails, telefones) nos documentos de validação.
- Ações externas (publicar, enviar às lojas, mandar mensagens, criar tarefas no quadro) só com confirmação.

## Papéis

Produto · Construtor · Negócio · Suporte · Dados/LGPD. A criação (Fase 3) é solo, do construtor com os agentes;
os portões são decididos pela equipe.

## Mudanças no processo

Se uma etapa não fizer sentido na prática, não improvise: registre uma proposta com a etiqueta `processo`
(problema, evidência, mudança sugerida). Mudanças entram nesta skill e no manual juntas, com nova versão.
