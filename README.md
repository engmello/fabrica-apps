# Fábrica de Apps — plugin para o Claude Code

O processo padronizado da equipe, empacotado como ferramenta: **34 etapas, 5 portões, 14 templates,
3 agentes e 11 skills**. O manual para leitura da equipe está no documento "Manual do Processo de Apps";
este plugin é a versão que o Claude executa. Os dois mudam juntos.

## Como usar (sem terminal)

O repositório funciona de dois jeitos: **como projeto** (abra-o e tudo já está carregado, sem instalar nada)
ou **como plugin** (instalado uma vez, vale em qualquer pasta).

### Opção 1 — No navegador, em claude.ai/code (mais simples)
1. Acesse **claude.ai/code** e conecte o GitHub, se ainda não estiver conectado.
2. Inicie uma sessão no repositório **engmello/fabrica-apps**.
3. Digite, por exemplo: `/novo-app FIN Finanças — controle de gastos para autônomos`.
4. O Claude cria `apps/fin-app/` numa branch e envia para o GitHub. Revise e faça o merge pelo GitHub
   (ou peça ao Claude para abrir o pull request).

### Opção 2 — No app Claude para computador, aba Code
1. Abra o app Claude, clique na aba **Code** e inicie uma sessão.
2. Escolha **Cloud** e o repositório **engmello/fabrica-apps** (funciona como a Opção 1), **ou**
   escolha **Local** e uma pasta com uma cópia do repositório no seu computador.
3. Digite `/` para ver os comandos (`/novo-app`, `/etapa`, `/status`, `/portao`…) e comece pelo `/novo-app`.

### Opção 3 — Como plugin (para usar em outras pastas)
No app Claude (aba Code, sessão Local) ou no VS Code, adicione o marketplace `engmello/fabrica-apps`
e instale o plugin `fabrica-apps` pelo gerenciador de plugins (botão **+** → Plugins). No terminal:
```
/plugin marketplace add engmello/fabrica-apps
/plugin install fabrica-apps@fabrica-apps-marketplace
```
Instalado como plugin, os comandos podem aparecer com prefixo, como `/fabrica-apps:etapa`.
Sessões na nuvem não carregam plugins instalados — nelas use a Opção 1 ou 2.

## O que tem no repositório

```
fabrica-apps/
├── CLAUDE.md                  # instruções do projeto
├── apps/                      # um app por pasta: <sigla>-app/docs/ (criado por /novo-app)
├── .claude/
│   ├── commands/              # /novo-app /etapa /status /portao /validar-ideia /nova-feature /revisar
│   ├── agents/                # produto, desenvolvedor, revisor
│   └── skills/
│       ├── processo-apps/     # o processo: etapas/ (fichas) + templates/ (T01–T14) + template-repo/
│       ├── validar-ideia/  prd/  plano-metricas/  quebrar-tarefas/
│       ├── arquitetura-app/  nova-tela/  api-backend/  revisao-codigo/
│       └── testes/  release/  relatorio-metricas/
└── .claude-plugin/            # manifesto do plugin e do marketplace
```

## Como o processo funciona no dia a dia

1. **Ideia nova** → `/novo-app FIN Finanças — controle de gastos para autônomos`
   Cria `apps/fin-app/docs/` com o registro (T07), o registro de portões (T05) e a ficha da ideia (T01).
2. **Cada etapa** → `/etapa E1.1`, `/etapa E1.2`…
   O Claude lê a ficha, confere as entradas, executa com o agente certo, gera a saída no template e atualiza o registro.
3. **Fim de fase** → `/portao P1`
   O Claude monta o dossiê; a equipe decide na reunião; o Claude registra a decisão informada.
4. **A qualquer momento** → `/status`
5. **Na Fase 3**, o app ganha repositório próprio (`/etapa E3.1` copia o `template-repo/` e os `docs/`) e cada tarefa
   passa por `/nova-feature`.

## Onde ficam os dados de cada app

Tudo de um app vive em `apps/<sigla>-app/docs/`. No E3.1 o app ganha um repositório próprio no GitHub,
os `docs/` vão junto, e documentos e código passam a ficar versionados lado a lado.

## Como mudar o processo

1. Proposta no quadro com a etiqueta `processo` (problema, evidência, mudança).
2. Decisão na retrospectiva.
3. Pull request neste repositório alterando fichas, templates ou skills, **e** atualização do manual.
4. Subir `version` em `.claude-plugin/plugin.json` (maior.menor.correção, como no manual) e registrar no histórico do manual.
5. Cada pessoa atualiza com `/plugin update fabrica-apps` (ou reinstalando).

## Histórico

| Versão | Data | Mudança |
| --- | --- | --- |
| 1.1.0 | 30/10/2026 | Repositório também funciona como projeto (navegador e app desktop); apps em `apps/` |
| 1.0.0 | 29/10/2026 | Primeira versão |
