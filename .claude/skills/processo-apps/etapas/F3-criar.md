# Fase 3 — Criar (solo)

MVP completo em staging, testado e aceito. O construtor trabalha com os agentes; a equipe acompanha pelo quadro e pela demo.
4 a 6 ciclos semanais. E4.1 e E4.6 começam em paralelo; E4.2 e E4.3 acontecem no fim desta fase e alimentam o P3.

## E3.1 · Setup do projeto
- **Objetivo:** o app nasce do template com a base pronta em um dia.
- **Gatilho:** P2 aprovado.
- **Entradas:** `template-repo/` desta skill; `docs/arquitetura.md`.
- **Passos:** 1. Criar o repositório vazio `<sigla>-app` no GitHub (pessoa da equipe, pela página do GitHub). 2. Copiar `template-repo/` e os `docs/` de `apps/<sigla>-app/` para ele. 3. Criar o app (Expo e/ou Next.js) conforme a arquitetura. 4. Preencher o `CLAUDE.md` e enviar (push com confirmação). 5. Em `apps/<sigla>-app/` do repositório da fábrica, deixar só um `README.md` com o link do novo repositório. 5. Projetos dev/staging/produção com segredos separados. 6. Sentry, PostHog e backup do banco.
- **Saída:** repositório publicando em staging.
- **Responsável:** Construtor.
- **IA:** agente `desenvolvedor`.
- **Pronto quando:** commit vazio passa no CI e publica sozinho em staging.
- **Duração:** 1 dia.

## E3.2 · Ciclo de funcionalidade ↻
- **Objetivo:** cada tarefa vira funcionalidade testada, instrumentada e revisada.
- **Gatilho:** tarefa no topo da semana.
- **Entradas:** tarefa com critérios e evento; `CLAUDE.md`; skills técnicas.
- **Passos:** 1. Especificar (mini-spec aprovada). 2. Testes primeiro. 3. Implementar em branch própria. 4. Instrumentar o evento. 5. Revisar (Revisor + leitura das áreas críticas). 6. Integrar (CI verde, merge → staging).
- **Saída:** funcionalidade em staging; tarefa em "Em revisão".
- **Responsável:** Construtor executa e aprova o PR; Produto aceita na demo.
- **IA:** `/nova-feature`.
- **Pronto quando:** definição de pronto do `CLAUDE.md` cumprida e evento visível no PostHog de staging.
- **Duração:** ½ a 1 dia por tarefa; no máximo 2 abertas.

## E3.3 · Demo semanal ↻
- **Objetivo:** a equipe aceita o que foi feito sem participar do código.
- **Gatilho:** toda sexta.
- **Entradas:** tarefas em "Em revisão"; resumo semanal.
- **Passos:** 1. Resumo da semana no canal. 2. Mostrar cada item em staging. 3. Aceitar ou devolver com motivo.
- **Saída:** itens aceitos/devolvidos no quadro; nota em `docs/registro.md`.
- **Responsável:** Construtor apresenta; Produto aceita; Suporte testa.
- **IA:** agente `produto` escreve o resumo a partir do `git log` da semana e do quadro.
- **Pronto quando:** todos os itens com decisão.
- **Duração:** 15 minutos.

## E3.4 · Documentos legais
- **Objetivo:** política de privacidade e termos corretos e publicados antes do beta.
- **Gatilho:** arquitetura aprovada.
- **Entradas:** mapa de dados (T09); PRD seções 7 e 8.
- **Passos:** 1. Preencher o T10. 2. Conferir que o texto bate com o que o app coleta. 3. Revisão jurídica. 4. Publicar e linkar no app e nas lojas.
- **Saída:** T10 → `docs/legal/privacidade.md` e `docs/legal/termos.md`, publicados.
- **Responsável:** Dados/LGPD; Construtor publica.
- **IA:** agente `produto` preenche a partir do mapa de dados.
- **Pronto quando:** publicados, revisados e coerentes com o mapa de dados.
- **Duração:** 2 a 3 dias + revisão jurídica.

## P3 · Portão 3 — pronto para lançar
- **Gatilho:** backlog do MVP concluído e beta fechado (E4.3) realizado.
- **Entradas:** T06; resultado do beta (T11).
- **Passos:** 1. Checklist completo. 2. Equipe testa em staging. 3. `/portao P3` e reunião de 30 min. 4. Decisão no T05. 5. Aprovado → E4.7.
- **Critérios:** checklist completo; beta sem bug crítico; maioria chega ao momento de valor; documentos legais publicados.
- **Responsável:** Construtor conduz; equipe decide.
