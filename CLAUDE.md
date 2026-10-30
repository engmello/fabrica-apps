# Fábrica de Apps

Este repositório é a ferramenta de processo da equipe para criar, lançar e evoluir apps.
Toda ideia de app passa pelo processo descrito na skill `processo-apps` (34 etapas, 5 portões, templates T01–T14).

## Como trabalhar aqui

- Ideia nova: `/novo-app <SIGLA> <nome> — <ideia em uma frase>` cria `apps/<sigla>-app/`.
- Executar uma etapa: `/etapa <código> <sigla>` (ex.: `/etapa E1.1 FIN`).
- Ver o andamento: `/status` (todos os apps) ou `/status <sigla>`.
- Fim de fase: `/portao <P1–P5> <sigla>` prepara o dossiê; a decisão é sempre da equipe.

## Regras

- Siga a ficha da etapa; não pule etapas sem justificativa no registro do app.
- Nunca registre a decisão de um portão por conta própria.
- Nunca grave nomes, e-mails ou telefones reais nos documentos de validação.
- Ações externas (publicar, enviar às lojas, mensagens, criar tarefas no quadro) só com confirmação.
- Escreva em português, de forma direta e curta.

## Mudanças no próprio processo

Fichas, templates, agentes e comandos ficam em `.claude/`. Uma mudança no processo é feita por pull request,
sobe a versão em `.claude-plugin/plugin.json` e é refletida no Manual do Processo de Apps.
