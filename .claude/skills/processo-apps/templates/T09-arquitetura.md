# T09 · Arquitetura — [nome do app]

Etapa: E2.5 · Local: `docs/arquitetura.md` · Decisões relevantes também viram ADR em `docs/adr/`

## 1. Visão geral
[Diagrama ou lista de componentes: app mobile, web, Supabase, serviços externos e como se conectam.]

## 2. Stack
| Camada | Escolha | Igual à padrão? | ADR |
| --- | --- | --- | --- |
| Mobile | React Native + Expo | Sim | — |
| Web | Next.js + Tailwind | Sim | — |
| Backend | Supabase | Sim | — |
| Erros | Sentry | Sim | — |
| Analytics | PostHog | Sim | — |
| Pagamentos | | | |

## 3. Modelo de dados
| Tabela | Colunas principais | Dono do registro | Política de acesso (RLS) |
| --- | --- | --- | --- |
| | | `user_id` | dono lê/escreve |

## 4. Autenticação
- Métodos (e-mail, Google, Apple — Apple obrigatório no iOS se houver login social):
- Sessão:
- Exclusão de conta (o que é apagado e como):

## 5. Integrações
| Serviço | Para quê | Dados enviados | Segredos (só em variáveis de ambiente) |
| --- | --- | --- | --- |

## 6. Mapa de dados pessoais
| Dado | Tabela/serviço | Finalidade | Base legal | Retenção | Exclusão |
| --- | --- | --- | --- | --- | --- |

## 7. Ambientes
| Ambiente | Projeto Supabase | URL | Quem publica |
| --- | --- | --- | --- |
| Desenvolvimento | | | Construtor |
| Staging | | | CI no merge |
| Produção | | | Construtor, com aprovação |

## 8. Custos estimados (mensais)
| Item | 100 usuários | 1.000 | 10.000 |
| --- | --- | --- | --- |
| | | | |
| **Total** | | | |

## 9. Riscos de segurança
| Risco | Probabilidade | Impacto | Mitigação |
| --- | --- | --- | --- |
| Chave vazada | | | |
| Acesso a dados de outro usuário | | | RLS + teste de dois usuários |
| Abuso (spam, uploads) | | | |
| Perda de dados | | | Backup diário + restauração testada |
