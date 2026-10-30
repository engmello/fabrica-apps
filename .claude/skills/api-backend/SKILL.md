---
name: api-backend
description: Cria tabelas, migrações, políticas RLS, funções e endpoints no Supabase (Postgres + Edge Functions) seguindo as convenções do projeto, com validação de entrada e testes de acesso. Use ao criar ou alterar qualquer dado, regra de acesso ou rota de backend.
---

# API e backend (Supabase)

## Migrações

- Criar com `npx supabase migration new <descricao_curta>`; nunca alterar migração já aplicada em staging/produção.
- Toda migração em `supabase/migrations/`, revisável, com comentário no topo explicando o porquê.
- Mudança destrutiva (apagar/renomear coluna) em duas etapas: adicionar novo → migrar dados → remover antigo em versão posterior.
- Descrever o plano de volta no PR.

## Tabelas

```sql
create table public.despesas (
  id uuid primary key default gen_random_uuid(),
  user_id uuid not null references auth.users(id) on delete cascade,
  valor_centavos integer not null check (valor_centavos > 0),
  categoria text not null,
  criado_em timestamptz not null default now()
);
create index on public.despesas (user_id, criado_em desc);

alter table public.despesas enable row level security;
create policy "dono lê" on public.despesas for select using (user_id = auth.uid());
create policy "dono cria" on public.despesas for insert with check (user_id = auth.uid());
create policy "dono altera" on public.despesas for update using (user_id = auth.uid());
create policy "dono apaga" on public.despesas for delete using (user_id = auth.uid());
```

Convenções: nomes em português, snake_case, plural; dinheiro em centavos (inteiro); datas `timestamptz`;
`on delete cascade` a partir de `auth.users` para que excluir a conta apague os dados (LGPD).

## Regras de acesso

- **RLS em todas as tabelas**, sem exceção. Tabela sem política = ninguém acessa (é o comportamento desejado até haver política).
- A chave `service_role` só existe em Edge Functions e CI; nunca no app.
- Teste de RLS obrigatório: usuário A não lê nem altera dados do usuário B.

## Edge Functions (quando a regra não cabe em RLS)

- Validar toda entrada com Zod; responder 400 com mensagem clara.
- Autenticar pelo JWT do usuário; checar permissão explicitamente.
- Não registrar dados pessoais em logs.
- Limitar taxa em rotas públicas (formulários, envio de e-mail).
- Idempotência em pagamentos e webhooks (guardar o ID do evento processado).

## Testes

- Teste de RLS (dois usuários) para cada tabela nova.
- Teste de cada função: entrada válida, inválida, sem autenticação, sem permissão.
