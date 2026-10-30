# Fábrica de Apps — plugin para o Claude Code

O processo padronizado da equipe, empacotado como ferramenta: **34 etapas, 5 portões, 14 templates,
3 agentes e 11 skills**. O manual para leitura da equipe está no documento "Manual do Processo de Apps";
este plugin é a versão que o Claude executa. Os dois mudam juntos.

## O que vem no plugin

```
fabrica-apps/
├── .claude-plugin/
│   ├── plugin.json            # identificação do plugin (versão = versão do processo)
│   └── marketplace.json       # permite instalar a partir deste repositório
├── commands/
│   ├── novo-app.md            # /novo-app      → E0.1 + E0.2: abre o app no processo
│   ├── etapa.md               # /etapa E2.1    → executa qualquer etapa pela ficha padrão
│   ├── status.md              # /status        → onde cada app está e o que falta
│   ├── portao.md              # /portao P2     → dossiê do portão (a decisão é da equipe)
│   ├── validar-ideia.md       # /validar-ideia → primeira versão rápida da ficha da ideia
│   ├── nova-feature.md        # /nova-feature  → ciclo E3.2: spec → testes → código → revisão
│   └── revisar.md             # /revisar       → revisão independente do branch
├── agents/
│   ├── produto.md             # validação, PRD, métricas, backlog, dossiês
│   ├── desenvolvedor.md       # arquitetura, código, testes, release
│   └── revisor.md             # revisão somente leitura
└── skills/
    ├── processo-apps/         # o processo: SKILL.md + etapas/ (fichas) + templates/ (T01–T14) + template-repo/
    ├── validar-ideia/  prd/  plano-metricas/  quebrar-tarefas/          # produto
    ├── arquitetura-app/  nova-tela/  api-backend/  revisao-codigo/      # técnica
    └── testes/  release/  relatorio-metricas/                           # Onda 2
```

## Como instalar (uma vez por pessoa)

1. Suba esta pasta para um repositório da equipe no GitHub (ex.: `sua-org/fabrica-apps`).
2. No Claude Code, rode:
   ```
   /plugin marketplace add sua-org/fabrica-apps
   /plugin install fabrica-apps@fabrica-apps-marketplace
   ```
3. Reinicie o Claude Code e confira com `/help` se os comandos aparecem.
   Dependendo da versão, os comandos do plugin podem aparecer com prefixo, como `/fabrica-apps:etapa`.

Para testar localmente antes de publicar: `/plugin marketplace add ./caminho/para/fabrica-apps`.
Confira a documentação de plugins do Claude Code se algum comando de instalação tiver mudado.

## Como o processo funciona no dia a dia

1. **Ideia nova** → `/novo-app FIN Finanças — controle de gastos para autônomos`
   Cria `fin-app/docs/` com o registro (T07), o registro de portões (T05) e a ficha da ideia (T01).
2. **Cada etapa** → `/etapa E1.1`, `/etapa E1.2`…
   O Claude lê a ficha, confere as entradas, executa com o agente certo, gera a saída no template e atualiza o registro.
3. **Fim de fase** → `/portao P1`
   O Claude monta o dossiê; a equipe decide na reunião; o Claude registra a decisão informada.
4. **A qualquer momento** → `/status`
5. **Na Fase 3**, a pasta do app vira o repositório (`/etapa E3.1` copia o `template-repo/`) e cada tarefa
   passa por `/nova-feature`.

## Onde ficam os dados de cada app

Tudo de um app vive na pasta `<sigla>-app/`, principalmente em `docs/`. A partir do E3.1 essa pasta é o
repositório do app no GitHub, então documentos e código ficam versionados juntos e os agentes sempre
têm o contexto.

## Como mudar o processo

1. Proposta no quadro com a etiqueta `processo` (problema, evidência, mudança).
2. Decisão na retrospectiva.
3. Pull request neste repositório alterando fichas, templates ou skills, **e** atualização do manual.
4. Subir `version` em `.claude-plugin/plugin.json` (maior.menor.correção, como no manual) e registrar no histórico do manual.
5. Cada pessoa atualiza com `/plugin update fabrica-apps` (ou reinstalando).

## Histórico

| Versão | Data | Mudança |
| --- | --- | --- |
| 1.0.0 | 29/10/2026 | Primeira versão |
