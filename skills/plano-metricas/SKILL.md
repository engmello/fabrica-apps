---
name: plano-metricas
description: Define a métrica principal, o funil e o catálogo de eventos de analytics de um app, ligando cada funcionalidade a eventos com nomes padronizados e sem dados pessoais. Use na Fase 2, ao adicionar funcionalidades, ou ao planejar uma nova versão.
---

# Plano de métricas

Saída: `docs/metricas.md`.

## 1. Métrica principal

Uma só. Precisa representar **valor entregue ao usuário** e ser influenciável pelo produto.
- Boas: "usuários que concluíram 3+ tarefas na semana", "retenção no dia 7", "despesas registradas por usuário ativo/semana".
- Ruins (vaidade): downloads, cadastros, page views, seguidores.
Defina: fórmula exata, por que representa valor, meta para 90 dias após o lançamento.

## 2. Funil

| Etapa | Definição | Evento que marca | Meta |
Aquisição → Ativação (chegou ao momento de valor) → Retenção (voltou na semana 2) → Conversão (pagou) → Indicação.

## 3. Catálogo de eventos

Regras de nome: `objeto_acao`, minúsculas, sem acento, verbo no particípio (`tarefa_concluida`,
`assinatura_iniciada`). Um evento por fato; variações vão em propriedades, não em eventos novos.

| Evento | Quando dispara | Propriedades | História | Status (Planejado/Em staging/Ativo) |

Proibido em propriedades: nome, e-mail, telefone, CPF, endereço, texto livre digitado pelo usuário,
localização precisa. Identifique o usuário só pelo ID interno.

Cada história do PRD precisa de pelo menos um evento. Se não precisar, justifique.

## 4. Saúde técnica

Sessões sem falha (>99%), tempo de abertura (<2 s), erros novos/dia — fonte: Sentry.

## 5. Métricas do processo

Tempo da ideia validada ao lançamento, tempo médio por funcionalidade, bugs em produção por versão,
custo mensal de IA + infraestrutura.

## Ao planejar uma versão

Leia o funil, encontre a etapa com maior perda, e proponha hipóteses no formato
"mudar X deve melhorar Y em Z%", com os eventos que vão medir o resultado.
