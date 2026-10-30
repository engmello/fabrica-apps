# Fase 1 — Validar

Evidência de que o problema existe e de que alguém quer a solução, sem código de produção. 3 a 4 semanas. E1.3 e E1.4 em paralelo.

## E1.1 · Hipótese e suposições
- **Objetivo:** transformar a ideia em afirmação testável.
- **Gatilho:** E0.2 concluída.
- **Entradas:** T01 em rascunho.
- **Passos:** 1. Hipótese no formato padrão. 2. 3 suposições mais arriscadas, com teste e meta. 3. Crítica cética pela IA. 4. Aprovação da equipe.
- **Saída:** T01, seções Hipótese e Suposições → `docs/F1-validar/<SIGLA>-T01-ficha-ideia.md`.
- **Responsável:** Produto; equipe aprova.
- **IA:** agente `produto` + skill `validar-ideia`.
- **Pronto quando:** equipe concorda com a frase e as 3 suposições com metas.
- **Duração:** 1 dia.

## E1.2 · Pesquisa de alternativas
- **Objetivo:** saber o que o público usa hoje e onde há espaço.
- **Gatilho:** E1.1 concluída.
- **Entradas:** T01 com hipótese.
- **Passos:** 1. 5 a 10 alternativas, incluindo as não óbvias. 2. Avaliações negativas nas lojas, agrupadas. 3. Diferencial em uma linha.
- **Saída:** T01, seção Alternativas.
- **Responsável:** Produto.
- **IA:** agente `produto` com pesquisa web + skill `validar-ideia`.
- **Pronto quando:** tabela preenchida e diferencial justificado por reclamações reais.
- **Duração:** 1 a 2 dias.

## E1.3 · Entrevistas ↻
- **Objetivo:** confirmar que a dor existe, é frequente e custa algo.
- **Gatilho:** E1.1 concluída.
- **Entradas:** T01; T02.
- **Passos:** 1. Adaptar o roteiro. 2. Recrutar 8 a 10 pessoas do público. 3. Entrevistar em dupla. 4. Anotar com códigos (E01…), nunca nomes. 5. Sintetizar padrões e % de dor confirmada.
- **Saída:** `docs/F1-validar/entrevistas/E01.md`… e síntese no T01.
- **Responsável:** Produto e Negócio; Produto aprova.
- **IA:** skill `validar-ideia` adapta o roteiro e sintetiza.
- **Pronto quando:** 8+ entrevistas sintetizadas com % de dor confirmada.
- **Duração:** 2 semanas.

## E1.4 · Teste de interesse
- **Objetivo:** medir comportamento real, não opinião.
- **Gatilho:** E1.2 concluída.
- **Entradas:** T01 com hipótese e diferencial.
- **Passos:** 1. Fixar a meta antes. 2. Landing page com uma única chamada. 3. 200 a 500 visitantes do público. 4. Medir e registrar.
- **Saída:** landing page + resultado no T01.
- **Responsável:** Negócio; Construtor publica a página.
- **IA:** agente `desenvolvedor` gera a página; agente `produto` escreve 2 versões do texto.
- **Pronto quando:** tráfego-alvo atingido e resultado comparado com a meta fixada.
- **Duração:** 1 a 2 semanas.

## E1.5 · Viabilidade
- **Objetivo:** confirmar que o app pode se pagar.
- **Gatilho:** primeiros resultados de E1.3 e E1.4.
- **Entradas:** T01; orçamento; preços citados nas entrevistas.
- **Passos:** 1. Custo de construir e mensal. 2. Usuários, conversão, preço. 3. Cenários pessimista/provável/otimista com taxas das lojas.
- **Saída:** T01, seção Viabilidade.
- **Responsável:** Negócio.
- **IA:** agente `produto` monta os cenários.
- **Pronto quando:** 3 cenários com estimativas marcadas.
- **Duração:** 1 dia.

## P1 · Portão 1 — seguir ou parar
- **Gatilho:** E1.3, E1.4 e E1.5 concluídas.
- **Entradas:** T01 completo; síntese das entrevistas.
- **Passos:** 1. Dossiê contra os critérios (`/portao P1`). 2. Reunião de 30 min. 3. Decisão registrada no T05 pela equipe. 4. Seguir → E2.1 · Reformular → E1.1 · Arquivar → ficha arquivada com aprendizados.
- **Critérios:** dor confirmada em 60%+; meta do teste de interesse atingida; cenário provável viável.
- **Responsável:** Produto conduz; equipe decide.
