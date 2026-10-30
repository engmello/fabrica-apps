# Fase 2 — Planejar

O mínimo que prova a hipótese, escrito com clareza para os agentes construírem sem adivinhar. 2 semanas.
Semana 1: E2.1, E2.2, E2.3. Semana 2: E2.4, E2.5, E2.6.

## E2.1 · PRD
- **Objetivo:** documento curto que pessoas e agentes leem e entendem o que construir e por quê.
- **Gatilho:** P1 = seguir.
- **Entradas:** T01 completo; síntese das entrevistas.
- **Passos:** 1. Partir das dores. 2. Momento de valor. 3. Cortar o MVP com o teste padrão. 4. 3 a 7 histórias com Dado/Quando/Então. 5. Requisitos não funcionais mensuráveis. 6. Revisão crítica pela IA.
- **Saída:** T03 → `docs/prd.md`.
- **Responsável:** Produto; equipe aprova no P2.
- **IA:** agente `produto` + skill `prd`.
- **Pronto quando:** MVP descrito em uma frase (faz / não faz); toda história com critério.
- **Duração:** 3 dias.

## E2.2 · Modelo de negócio
- **Objetivo:** saber como o app gera valor financeiro antes de desenhar o produto.
- **Gatilho:** P1 = seguir.
- **Entradas:** T01; concorrentes.
- **Passos:** 1. Modelo. 2. Preço ancorado no valor da dor. 3. Fronteira grátis/pago. 4. Atualizar viabilidade.
- **Saída:** `docs/prd.md`, seção 8.
- **Responsável:** Negócio; equipe aprova.
- **IA:** agente `produto` compara concorrentes e simula cenários.
- **Pronto quando:** modelo, preço e fronteira grátis/pago escritos.
- **Duração:** 1 a 2 dias.

## E2.3 · Plano de métricas
- **Objetivo:** saber desde o primeiro dia se o app funciona.
- **Gatilho:** rascunho do PRD com histórias.
- **Entradas:** `docs/prd.md`.
- **Passos:** 1. Métrica principal + meta 90 dias. 2. Funil. 3. Catálogo de eventos (1+ por história). 4. Nenhum dado pessoal em eventos.
- **Saída:** T04 → `docs/metricas.md`.
- **Responsável:** Produto; equipe aprova no P2.
- **IA:** agente `produto` + skill `plano-metricas`.
- **Pronto quando:** toda história com evento; métrica principal com meta numérica.
- **Duração:** 1 dia.

## E2.4 · Protótipo e teste
- **Objetivo:** errar no protótipo, não no código.
- **Gatilho:** PRD com fluxo principal.
- **Entradas:** `docs/prd.md` seções 4 e 5.
- **Passos:** 1. Caminho até o momento de valor com mínimo de telas. 2. Estados de erro, vazio e carregando. 3. Testar com 5 pessoas usando o T08. 4. Ajustar fluxo e PRD.
- **Saída:** protótipo clicável + T08 → `docs/F2-planejar/teste-prototipo.md`.
- **Responsável:** Construtor; Produto aprova.
- **IA:** Claude Design ou Figma; agente `produto` adapta o roteiro e resume os testes.
- **Pronto quando:** 4 de 5 testadores chegam ao momento de valor sem ajuda.
- **Duração:** 3 a 4 dias.

## E2.5 · Arquitetura
- **Objetivo:** escolhas técnicas que o construtor mantém sozinho.
- **Gatilho:** PRD e protótipo em rascunho.
- **Entradas:** `docs/prd.md`, protótipo, `docs/metricas.md`.
- **Passos:** 1. Stack padrão. 2. Modelo de dados com RLS. 3. Autenticação e exclusão de conta. 4. Integrações e segredos. 5. Mapa de dados pessoais. 6. Custos por 100/1.000/10.000 usuários. 7. Riscos de segurança. 8. ADR para cada desvio.
- **Saída:** T09 → `docs/arquitetura.md` + `docs/adr/`.
- **Responsável:** Construtor; Dados/LGPD revisa o mapa de dados.
- **IA:** agente `desenvolvedor` + skill `arquitetura-app`; agente `revisor` analisa riscos.
- **Pronto quando:** dados, autenticação e integrações definidos; custo dentro do orçamento.
- **Duração:** 2 dias.

## E2.6 · Backlog
- **Objetivo:** fila clara para 4 a 6 semanas.
- **Gatilho:** PRD, métricas e arquitetura finais.
- **Entradas:** T03, T04, T09.
- **Passos:** 1. Fatias verticais de até 1 dia. 2. Ordem pelo caminho ao momento de valor. 3. Critério, evento e dependências por tarefa. 4. Marcar áreas críticas. 5. Criar no quadro com etiqueta E3.2 (com confirmação).
- **Saída:** tarefas no quadro (cópia em `docs/F2-planejar/backlog.md`).
- **Responsável:** Produto; Construtor estima.
- **IA:** agente `produto` + skill `quebrar-tarefas`.
- **Pronto quando:** 4 primeiras semanas quebradas e priorizadas.
- **Duração:** 1 dia.

## P2 · Portão 2 — começar a construir
- **Gatilho:** E2.1 a E2.6 concluídas.
- **Entradas:** T03, T04, T08, T09, backlog.
- **Passos:** 1. `/portao P2`. 2. Reunião de 30 min. 3. Decisão no T05. 4. Aprovado → E3.1, e iniciar E4.1 e E4.6.
- **Critérios:** PRD, modelo de negócio e métricas aprovados; protótipo testado; arquitetura aprovada; 4 semanas de backlog.
- **Responsável:** Produto conduz; equipe decide produto; Construtor decide arquitetura.
