# Fase 4 — Lançar

Primeiros usuários certos, de forma controlada. E4.1 e E4.6 começam após o P2; E4.2 e E4.3 no fim da Fase 3 (alimentam o P3); E4.4, E4.5 e E4.7 após o P3.

## E4.1 · Contas e ficha das lojas
- **Objetivo:** eliminar a burocracia antes que atrase o lançamento.
- **Gatilho:** P2 aprovado.
- **Entradas:** empresa titular (T14); PRD; mapa de dados pessoais.
- **Passos:** 1. Contas Apple e Google da empresa (verificação pode levar semanas). 2. Criar o app nas lojas. 3. Ficha: nome, subtítulo, descrição, palavras-chave, capturas, classificação etária. 4. Formulários de privacidade a partir do mapa de dados.
- **Saída:** T11 parte 1 → `docs/F4-lancar/lojas-e-beta.md`.
- **Responsável:** Negócio; Construtor configura contas.
- **IA:** agente `produto` escreve textos com as frases das entrevistas.
- **Pronto quando:** fichas preenchidas e declarações de privacidade iguais ao T10.
- **Duração:** 2 dias + verificação das contas.

## E4.2 · Beta nas lojas
- **Objetivo:** descobrir rejeições antes da semana de lançamento.
- **Gatilho:** caminho ao momento de valor funcionando em staging.
- **Entradas:** build; T11; T10.
- **Passos:** 1. Revisar contra as diretrizes vigentes (pesquisar a versão atual). 2. Conta de teste para o revisor. 3. TestFlight e teste interno do Google Play (envio com confirmação). 4. Corrigir e reenviar se rejeitado.
- **Saída:** beta aprovado nas duas lojas.
- **Responsável:** Construtor.
- **IA:** agente `revisor` confere contra as diretrizes; skill `release`.
- **Pronto quando:** aprovado pela Apple e pelo Google.
- **Duração:** 1 dia + 1 a 3 dias de revisão.

## E4.3 · Beta fechado
- **Objetivo:** encontrar problemas reais com risco baixo.
- **Gatilho:** E4.2 concluída.
- **Entradas:** lista de espera; T11 parte 2.
- **Passos:** 1. Convidar 20 a 50, priorizando entrevistados. 2. Missão clara e canal de feedback. 3. Acompanhar ativação e retenção. 4. Conversar com 5. 5. Corrigir o que bloqueia o momento de valor.
- **Saída:** T11 parte 2 com resultado.
- **Responsável:** Suporte; Construtor corrige.
- **IA:** agente `produto` agrupa feedback por tema.
- **Pronto quando:** nenhum bug crítico e maioria chegou ao momento de valor.
- **Duração:** 1 a 2 semanas.

## E4.4 · Plano de lançamento
- **Objetivo:** trazer os primeiros 100 a 1.000 usuários certos.
- **Gatilho:** início do beta fechado.
- **Entradas:** síntese das entrevistas; teste de interesse; ficha das lojas.
- **Passos:** 1. Um canal principal. 2. Mensagem, metas, orçamento. 3. Calendário das 2 primeiras semanas. 4. Landing page de lançamento.
- **Saída:** T12 → `docs/F4-lancar/plano-lancamento.md`.
- **Responsável:** Negócio.
- **IA:** agente `produto` produz conteúdo e variações.
- **Pronto quando:** canal, mensagem, metas e calendário aprovados.
- **Duração:** 2 dias.

## E4.5 · Suporte
- **Objetivo:** transformar problemas em confiança e backlog.
- **Gatilho:** fim do beta fechado.
- **Entradas:** dúvidas e problemas do beta.
- **Passos:** 1. Canal único dentro do app. 2. Responsável e prazo de resposta. 3. FAQ com as dúvidas do beta. 4. Etiquetas no quadro (bug, dúvida, pedido).
- **Saída:** canal, FAQ e responsável definidos.
- **Responsável:** Suporte.
- **IA:** agente `produto` rascunha FAQ e respostas-padrão.
- **Pronto quando:** canal ativo, FAQ publicada, prazo combinado.
- **Duração:** 1 dia.

## E4.6 · Plano de incidentes
- **Objetivo:** saber o que fazer se o app cair ou dados vazarem.
- **Gatilho:** P2 aprovado.
- **Entradas:** T09; mapa de dados pessoais.
- **Passos:** 1. Níveis de gravidade. 2. Quem é acionado e como. 3. Roteiros de rollback, feature flag e restauração de backup. 4. Comunicação a usuários e, se for o caso, à ANPD. 5. Testar a restauração do backup.
- **Saída:** T13 → `docs/F4-lancar/incidentes.md`.
- **Responsável:** Construtor; Dados/LGPD aprova.
- **IA:** agente `desenvolvedor` escreve os roteiros técnicos.
- **Pronto quando:** plano aprovado e restauração testada.
- **Duração:** 1 dia.

## E4.7 · Lançamento gradual
- **Objetivo:** limitar o estrago de um problema que escapou.
- **Gatilho:** P3 aprovado.
- **Entradas:** T06; T12; T13.
- **Passos:** 1. 10%, observar 24–48 h. 2. 50%, observar. 3. 100%. 4. Avançar só com sessões sem falha > 99%. 5. Iniciar o plano de lançamento. Não lançar na sexta.
- **Saída:** tabela de lançamento gradual no T06.
- **Responsável:** Construtor.
- **IA:** skill `release`; agente `desenvolvedor` resume o Sentry a cada etapa.
- **Pronto quando:** 100% liberado.
- **Duração:** 4 a 7 dias.

## P4 · Portão 4 — lançamento estável
- **Gatilho:** 7 dias após 100%.
- **Entradas:** Sentry; primeiras métricas; suporte.
- **Passos:** 1. Conferir critérios (`/portao P4`). 2. Decisão no T05. 3. Retrospectiva com propostas `processo`. 4. Aprovado → Fase 5.
- **Critérios:** sessões sem falha > 99% e nenhum bug crítico após 7 dias.
- **Responsável:** Construtor conduz; equipe decide.
