# [Nome do app]

[Uma frase: o que o app faz e para quem.]
PRD: `docs/prd.md` · Métricas: `docs/metricas.md` · Arquitetura: `docs/arquitetura.md` · Decisões: `docs/adr/` · Portões: `docs/portoes.md`

## Processo

Este app segue o processo da fábrica de apps (plugin `fabrica-apps`, skill `processo-apps`).
Status de todas as etapas em `docs/registro.md` — consulte com `/status` e execute com `/etapa <código>`.
Funcionalidades novas sempre pelo ciclo E3.2 (`/nova-feature`). Atualize o registro ao concluir uma etapa.

## Stack

- App mobile: React Native + Expo (TypeScript)
- Web: Next.js + Tailwind (TypeScript)
- Backend: Supabase (Postgres, Auth, Storage, RLS)
- Testes: Vitest (unitários), Playwright (web E2E), Maestro (mobile E2E)
- Erros: Sentry · Analytics e feature flags: PostHog
- CI/CD: GitHub Actions · Build mobile: EAS · Web: Vercel

[Apague o que não se aplica a este app.]

## Comandos

- Instalar: `npm install`
- Rodar: `npm run dev`
- Lint e tipos: `npm run lint && npm run typecheck`
- Testes: `npm test`
- E2E: `npm run test:e2e`
- Migração nova: `npx supabase migration new <nome>`

## Estrutura

- `app/` ou `src/app/` — telas e rotas
- `src/components/` — componentes reutilizáveis
- `src/lib/` — clientes (supabase, posthog, sentry) e utilitários
- `src/features/<funcionalidade>/` — lógica por funcionalidade
- `supabase/migrations/` — migrações SQL
- `tests/` — testes E2E

## Convenções

- TypeScript estrito; sem `any`.
- Toda tela tem estados de carregando, erro e vazio.
- Eventos de analytics: `objeto_acao` em minúsculas, sem acento, definidos em `docs/metricas.md`.
- Toda tabela nova tem RLS habilitada e política testada.
- Commits pequenos, mensagem no imperativo em português.
- Uma tarefa por branch: `feat/<id>-<descricao>`, `fix/<id>-<descricao>`.

## Nunca faça

- Commitar segredos, chaves ou `.env`.
- Colocar dados pessoais (nome, e-mail, telefone, CPF) em logs ou eventos de analytics.
- Usar dados reais de usuários em desenvolvimento ou em prompts.
- Enfraquecer ou apagar um teste para fazê-lo passar.
- Adicionar dependência nova sem justificar no PR.
- Publicar em produção sem aprovação explícita do construtor.

## Definição de pronto

1. Critérios de aceite da tarefa cobertos por testes, todos passando.
2. Evento de analytics previsto implementado e verificado em staging.
3. Revisão do agente `revisor` sem itens críticos.
4. Lint, tipos e build passando no CI.
