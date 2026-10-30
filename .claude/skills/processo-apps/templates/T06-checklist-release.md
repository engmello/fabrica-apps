# T06 · Checklist de release — versão [x.y.z]

Etapas: P3, E4.7, E5.4 · Local: `docs/releases/release-x.y.z.md`

| Campo | Preencher |
| --- | --- |
| Versão | |
| Foco / hipótese | |
| Data prevista | |
| Responsável | |

## Qualidade
- [ ] Testes passando no CI
- [ ] Revisão do agente `revisor` sem itens críticos
- [ ] Diff das áreas críticas lido pelo construtor
- [ ] Testado em staging: iOS, Android e web
- [ ] Aceite da equipe na demo

## Dados e segurança
- [ ] Migrações testadas em staging, com plano de volta
- [ ] Backup do banco antes da publicação
- [ ] Nenhuma vulnerabilidade alta nas dependências
- [ ] Eventos novos no PostHog de staging, sem dados pessoais
- [ ] Política de privacidade atualizada, se a coleta mudou

## Publicação
- [ ] Versão incrementada (maior.menor.correção)
- [ ] `CHANGELOG.md` atualizado
- [ ] Notas de versão para o usuário
- [ ] Novidades atrás de feature flag
- [ ] Build enviado às lojas / deploy web preparado

## Lançamento gradual
| Etapa | Data/hora | Sessões sem falha | Avançar? |
| --- | --- | --- | --- |
| 10% | | | |
| 50% | | | |
| 100% | | | |

## Depois
- [ ] Comunicado no canal da equipe
- [ ] Resultado da hipótese medido após 2 semanas:
