---
name: arquitetura-app
description: Define ou revisa a arquitetura de um app usando a stack padrão (Expo/React Native, Next.js, Supabase, Sentry, PostHog) — modelo de dados com RLS, autenticação, integrações, custos e riscos de segurança/LGPD — e registra decisões como ADR. Use na Fase 2, ao criar o projeto, ou antes de mudanças estruturais.
---

# Arquitetura do app

## Princípio

Escolha o que uma pessoa sozinha consegue manter. **Use a stack padrão**; desvie só com motivo escrito em ADR.

| Camada | Padrão | Desviar quando |
| --- | --- | --- |
| Mobile | React Native + Expo (TS) | Precisa de recurso nativo pesado (AR, áudio em tempo real) |
| Web | Next.js + Tailwind | Site só estático → Astro |
| Backend | Supabase (Postgres, Auth, Storage, Edge Functions) | Regras de negócio muito complexas ou requisitos de dados fora do Brasil/UE |
| Erros | Sentry | — |
| Analytics/flags | PostHog | — |
| Pagamentos | RevenueCat (assinaturas nas lojas) · Stripe ou Mercado Pago (web) | — |
| Build/deploy | EAS · Vercel | — |

## Entregáveis (`docs/arquitetura.md`)

1. **Visão geral**: diagrama simples de componentes (app, web, Supabase, serviços externos).
2. **Modelo de dados**: tabelas, colunas principais, relações. Para cada tabela: dono do registro e
   política RLS ("usuário só lê/escreve onde `user_id = auth.uid()`").
3. **Autenticação**: métodos (e-mail mágico, Google, Apple — Apple é obrigatório no iOS se houver login social), sessão, exclusão de conta.
4. **Integrações**: cada serviço externo, o que envia, chaves necessárias (só em variáveis de ambiente).
5. **Mapa de dados pessoais**: dado → tabela → finalidade → retenção (alinhar com o PRD).
6. **Ambientes**: dev, staging, produção — projetos Supabase separados, segredos separados.
7. **Custos**: estimativa mensal por 100, 1.000 e 10.000 usuários ativos, incluindo IA se o app usar.
8. **Riscos de segurança** (análise curta): quem pode acessar o quê, o que acontece se uma chave vazar,
   dados sensíveis, abuso (spam, uploads), backup e restauração.

## ADR

Toda decisão relevante (escolha de serviço, mudança de modelo de dados, desvio da stack) vira
`docs/adr/NNN-titulo.md` usando `docs/adr/000-template.md`.

## Sinais de alerta

Microserviços, Kubernetes ou servidor próprio para um MVP; tabela sem RLS; chave de serviço
(`service_role`) usada no app cliente; custo que cresce mais rápido que a receita por usuário.
