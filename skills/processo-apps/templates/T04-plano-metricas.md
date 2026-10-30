# T04 · Plano de métricas — [nome do app]

Etapas: E2.3, E5.3 · Local: `docs/metricas.md`

## Métrica principal
| Campo | Preencher |
| --- | --- |
| Métrica (fórmula exata) | |
| Por que representa valor | |
| Valor no beta | |
| Meta 90 dias após o lançamento | |
| Onde ver | |

## Funil
| Etapa | Definição | Evento | Meta |
| --- | --- | --- | --- |
| Aquisição | Instalou ou visitou | `app_aberto` (1ª vez) | |
| Ativação | Chegou ao momento de valor | | |
| Retenção | Voltou e usou na semana 2 | | |
| Conversão | Passou para o pago | `assinatura_iniciada` | |
| Indicação | Convidou alguém | | |

## Catálogo de eventos
Padrão `objeto_acao`, minúsculas, sem acento. Proibido: nome, e-mail, telefone, CPF, endereço, texto livre, localização precisa.

| Evento | Quando dispara | Propriedades | História | Status |
| --- | --- | --- | --- | --- |
| `cadastro_concluido` | Fim do cadastro | `metodo` | H1 | Planejado |

## Saúde técnica
| Métrica | Fonte | Limite |
| --- | --- | --- |
| Sessões sem falha | Sentry | > 99% |
| Tempo de abertura | Sentry | < 2 s |
| Erros novos por dia | Sentry | |

## Métricas do processo
| Métrica | Como medir | Valor |
| --- | --- | --- |
| Ideia validada → lançamento | Datas P1 e P4 | |
| Tempo médio por funcionalidade | Quadro | |
| Bugs em produção por versão | Sentry + quadro | |
| Custo mensal IA + infraestrutura | Faturas | |
