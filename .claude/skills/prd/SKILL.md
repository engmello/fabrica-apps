---
name: prd
description: Escreve, revisa ou atualiza o PRD (documento de requisitos) de um app no formato padrão do processo — problema, métrica de sucesso, escopo do MVP, histórias com critérios de aceite, requisitos não funcionais, LGPD, modelo de negócio, plataformas e riscos. Use na Fase 2 ou sempre que o escopo de um app mudar.
---

# PRD

Saída: `docs/prd.md`, seguindo `template-prd.md`. Limite de 3 a 5 páginas.

## Como escrever

1. **Parta das evidências da validação** (ficha da ideia, síntese das entrevistas). Cite-as na seção 1.
   Se não houver validação, avise que o PRD está apoiado em suposições.
2. **Defina o momento de valor**: a primeira vez que o usuário resolve a dor. O MVP inteiro serve a ele.
3. **Corte o MVP**: liste tudo o que foi imaginado; para cada item pergunte "sem isso, o usuário ainda
   resolve a dor principal?". Se sim, vai para "fora do MVP". Um MVP saudável tem 3 a 7 histórias.
4. **Histórias**: "Como [usuário], quero [ação] para [benefício]". Cada uma com 2 a 5 critérios no formato
   **Dado / Quando / Então** e o evento de analytics correspondente (ver skill `plano-metricas`).
5. **Requisitos não funcionais** mensuráveis (ex.: "abre em menos de 2 s", não "rápido").
6. **LGPD**: tabela de cada dado pessoal com finalidade, base legal, local de armazenamento e retenção.
   Inclua sempre exclusão de conta (exigida pelas lojas).
7. **Modelo de negócio**: modelo, preço, fronteira grátis/pago — mesmo que comece gratuito.
8. **Riscos e perguntas em aberto**, cada um com responsável.

## Ao revisar um PRD

Procure ativamente: critérios vagos ("bonito", "intuitivo", "rápido"), histórias sem critério de
aceite, funcionalidades sem evento, dados pessoais sem base legal, escopo grande demais para 4–6
semanas, conflitos com a validação. Entregue a lista de problemas por gravidade.

## Exemplo de história bem escrita

**H2 — Registrar despesa rápida**
Como autônomo, quero registrar uma despesa em até 10 segundos para não esquecer de lançar depois.
- Dado que estou na tela inicial, quando toco em "+" e informo valor e categoria, então a despesa aparece no topo da lista.
- Dado que estou sem internet, quando registro uma despesa, então ela é salva e sincronizada ao reconectar.
- Dado que não informei valor, quando toco em salvar, então vejo "Informe o valor" e nada é salvo.
- Evento: `despesa_registrada` {categoria, offline: bool}
