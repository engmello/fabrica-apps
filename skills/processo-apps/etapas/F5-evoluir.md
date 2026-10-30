# Fase 5 — Medir e Evoluir

Investir onde os números mostram valor e decidir o futuro do app. Roda em ritmos até o P5 decidir pelo encerramento.

## E5.1 · Monitoramento diário ↻
- **Objetivo:** saber dos problemas antes dos usuários.
- **Gatilho:** todo dia útil, automático.
- **Entradas:** Sentry; PostHog; `docs/metricas.md`.
- **Passos:** 1. Tarefa agendada gera o relatório (falhas, erros novos, métrica principal vs. meta, anomalias). 2. Posta no canal. 3. Vermelho → cartão ou plano de incidentes.
- **Saída:** relatório diário no canal.
- **Responsável:** automático; Construtor age.
- **IA:** tarefa agendada + skill `relatorio-metricas`.
- **Pronto quando:** relatório entregue e todo vermelho com ação.
- **Duração:** 5 minutos de leitura.

## E5.2 · Manutenção semanal ↻
- **Objetivo:** impedir que o app se degrade.
- **Gatilho:** bloco fixo semanal.
- **Entradas:** bugs, avaliações das lojas, alertas de dependências.
- **Passos:** 1. Triagem. 2. Segurança primeiro. 3. Dependências em lotes pequenos com testes. 4. Responder avaliações negativas.
- **Saída:** PRs de manutenção.
- **Responsável:** Construtor; Suporte responde avaliações.
- **IA:** agente `desenvolvedor` atualiza e abre PR; `revisor` confere.
- **Pronto quando:** nenhum bug crítico com mais de 1 semana e nenhuma vulnerabilidade alta.
- **Duração:** 2 a 4 h/semana (máx. 20% do tempo).

## E5.3 · Planejamento de versão ↻
- **Objetivo:** cada versão melhorar a métrica principal.
- **Gatilho:** a cada 2 a 4 semanas.
- **Entradas:** funil; temas de suporte; avaliações; resultado da versão anterior.
- **Passos:** 1. Etapa do funil com maior perda. 2. Cruzar com o qualitativo. 3. Hipóteses "mudar X deve melhorar Y em Z". 4. Priorizar por impacto × esforço. 5. Atualizar PRD e métricas. 6. Quebrar em tarefas (→ E3.2).
- **Saída:** versão no quadro; T03 e T04 atualizados.
- **Responsável:** Produto; equipe aprova o foco.
- **IA:** agente `produto` propõe 3 opções; skill `quebrar-tarefas`.
- **Pronto quando:** foco, hipóteses e tarefas definidos.
- **Duração:** 45 min + ½ dia de preparação.

## E5.4 · Publicação de versão ↻
- **Objetivo:** entregar com frequência sem quebrar nada.
- **Gatilho:** tarefas da versão aceitas na demo.
- **Entradas:** T06.
- **Passos:** 1. Checklist. 2. Changelog e notas para o usuário. 3. Novidades atrás de feature flag. 4. Lançamento gradual (E4.7). 5. Medir a hipótese após 2 semanas.
- **Saída:** `docs/releases/release-x.y.z.md` (T06) com resultado.
- **Responsável:** Construtor.
- **IA:** skill `release`.
- **Pronto quando:** 100% liberado e resultado da hipótese registrado.
- **Duração:** 1 dia + 4 a 7 dias de lançamento gradual.

## E5.5 · Revisão trimestral ↻
- **Objetivo:** revisar custos, saúde técnica e o próprio processo.
- **Gatilho:** a cada trimestre.
- **Entradas:** métricas do produto e do processo; faturas; dívida técnica; propostas `processo`.
- **Passos:** 1. Dossiê. 2. Custos e arquitetura. 3. Métricas do processo. 4. Mudanças no processo (nova versão do plugin e do manual). 5. Seguir para o P5.
- **Saída:** dossiê trimestral; mudanças decididas.
- **Responsável:** Produto conduz; equipe decide.
- **IA:** agente `produto` prepara o dossiê e sugere melhorias nas skills.
- **Pronto quando:** dossiê apresentado e mudanças decididas.
- **Duração:** 1 h, junto com o P5.

## P5 · Portão 5 — continuar, pivotar ou encerrar
- **Gatilho:** revisão trimestral.
- **Entradas:** dossiê do E5.5; meta da métrica principal.
- **Passos:** 1. Métrica vs. meta e tendência de 2 ciclos. 2. Decisão da equipe no T05. 3. Continuar → E5.3 · Pivotar → E1.1 com nova hipótese · Encerrar → E5.6.
- **Critérios:** Continuar: meta atingida ou em alta · Pivotar: há uso, mas de outra forma ou por outro público · Encerrar: dois ciclos sem tração.
- **Responsável:** Produto conduz; equipe decide.

## E5.6 · Encerramento
- **Objetivo:** encerrar com respeito aos usuários e à LGPD.
- **Gatilho:** P5 = encerrar.
- **Entradas:** mapa de dados pessoais; contratos de serviços.
- **Passos:** 1. Avisar usuários com 30+ dias. 2. Encerrar cobranças. 3. Oferecer exportação dos dados. 4. Excluir dados pessoais conforme a política. 5. Retirar das lojas e desligar a infraestrutura. 6. Arquivar o repositório e registrar aprendizados.
- **Saída:** checklist de encerramento em `docs/encerramento.md`.
- **Responsável:** Construtor; Dados/LGPD aprova.
- **IA:** agente `produto` redige avisos; agente `desenvolvedor` prepara exportação e exclusão.
- **Pronto quando:** nenhum dado pessoal restante e nenhum custo recorrente ativo.
- **Duração:** 30 a 45 dias.
