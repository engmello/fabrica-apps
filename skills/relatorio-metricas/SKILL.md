---
name: relatorio-metricas
description: Monta relatórios de métricas e saúde do app a partir do PostHog e do Sentry — relatório diário (E5.1), revisão de versão (E5.3) e dossiê trimestral (E5.5) — comparando com as metas de docs/metricas.md. Use quando pedirem relatório, números do app, como está o funil, ou em tarefas agendadas de monitoramento.
---

# Relatório de métricas

## Fontes
- Metas e definições: `docs/metricas.md` (T04). Sem esse arquivo, avise e não invente metas.
- Dados: conectores ou APIs do PostHog (eventos, funis, retenção) e do Sentry (falhas, erros novos).
  Se não houver acesso, diga qual conexão falta; nunca estime números.
- Nunca inclua dados pessoais no relatório (só agregados e IDs internos quando indispensável).

## Relatório diário (E5.1) — curto, sempre no mesmo formato
```
<SIGLA> · <data> · 🟢/🟡/🔴
Sessões sem falha: x% (meta > 99%)
Erros novos: n — [os 3 principais, com link]
Métrica principal: valor (meta: y) — tendência 7 dias: ↑/↓/→
Anomalias: <o que mudou mais de 20% contra a média de 7 dias, ou "nenhuma">
Ação necessária: <quem, o quê> ou "nenhuma"
```
Vermelho: sessões sem falha < 99%, erro novo afetando > 1% dos usuários, ou métrica principal caindo 3 dias seguidos.

## Revisão de versão (E5.3)
1. Funil completo com conversão entre etapas e comparação com a versão anterior.
2. Etapa com maior perda — é onde a próxima versão deve atuar.
3. Resultado das hipóteses da última versão (meta vs. real).
4. Temas de suporte e avaliações das lojas, por frequência.
5. Três opções de foco para a próxima versão, com hipótese e evento de medição.

## Dossiê trimestral (E5.5 / P5)
- Métrica principal: meta, real e tendência de 2 ciclos.
- Saúde técnica: falhas, desempenho, dívida técnica conhecida.
- Custos do trimestre (IA, infraestrutura, lojas) e custo por usuário ativo.
- Métricas do processo (tempo por funcionalidade, bugs por versão, tempo ideia → lançamento).
- Recomendação para o P5 (continuar / pivotar / encerrar) — a decisão é da equipe.
