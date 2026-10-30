# T13 · Plano de incidentes — [nome do app]

Etapa: E4.6 · Local: `docs/F4-lancar/incidentes.md`

## Níveis de gravidade
| Nível | Exemplos | Resposta |
| --- | --- | --- |
| Crítico | App fora do ar; vazamento ou acesso indevido a dados pessoais; pagamentos falhando | Imediata, a qualquer hora |
| Alto | Funcionalidade principal quebrada para parte dos usuários | Mesmo dia |
| Médio | Erro com contorno; desempenho ruim | Próxima manutenção |

## Quem é acionado
| Papel | Pessoa | Contato | Quando |
| --- | --- | --- | --- |
| Construtor | | | Todos os níveis |
| Dados/LGPD | | | Qualquer incidente com dados pessoais |
| Produto | | | Crítico e alto |
| Suporte | | | Para comunicar usuários |

## Primeiros 30 minutos
1. Confirmar o problema (Sentry, painel do Supabase, teste manual).
2. Abrir um registro do incidente: hora, sintoma, quem está cuidando.
3. Conter: desligar a feature flag, voltar a versão anterior ou bloquear o acesso afetado.
4. Avisar no canal da equipe.

## Roteiros técnicos
- **Voltar versão web:** [comando ou passo no Vercel]
- **Voltar versão mobile:** [atualização OTA para a versão anterior / pausar o lançamento gradual nas lojas]
- **Desligar funcionalidade:** [nome da flag no PostHog]
- **Restaurar backup do banco:** [passos no Supabase] · último teste de restauração: [data]
- **Revogar e trocar chaves:** [onde estão, como gerar novas, onde atualizar]

## Incidentes com dados pessoais (LGPD)
1. Dados/LGPD avalia: quais dados, quantos titulares, risco ou dano relevante?
2. Se houver risco ou dano relevante: comunicar a ANPD e os titulares no prazo e na forma exigidos pela regulamentação vigente — confirmar o prazo atual no site da ANPD.
3. Registrar tudo: o que aconteceu, dados afetados, medidas tomadas.

## Comunicação aos usuários
Modelo: "Identificamos [problema] em [data/hora]. [O que foi afetado]. [O que fizemos]. [O que você deve fazer, se algo]. Dúvidas: [contato]."

## Depois do incidente (até 5 dias)
- [ ] Relato sem culpados: linha do tempo, causa, o que funcionou, o que não funcionou
- [ ] Ações de prevenção no quadro com responsável
- [ ] Proposta `processo` se o plano ou uma skill precisar mudar
