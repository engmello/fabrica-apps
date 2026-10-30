---
name: release
description: Prepara e conduz a publicação de uma versão — checklist T06, versionamento semântico, changelog, notas para o usuário, build e envio às lojas (EAS), deploy web (Vercel), atualização OTA, lançamento gradual e plano de volta. Use em E4.2, E4.7, E5.4 ou sempre que alguém pedir para publicar.
---

# Release

Toda ação que publica, envia às lojas ou altera produção **pede confirmação** antes de rodar.

## 1. Preparar
1. Criar `docs/releases/release-x.y.z.md` a partir do T06.
2. Definir a versão: **maior** (quebra compatibilidade ou muda muito a experiência), **menor** (funcionalidade nova),
   **correção** (só correções). Atualizar `version` no `package.json` e no `app.json`/`app.config` (Expo);
   o número de build sobe a cada envio às lojas.
3. Gerar o `CHANGELOG.md` a partir dos commits desde a última tag, agrupando em Novidades / Melhorias / Correções.
4. Escrever as notas para o usuário: curtas, com benefício, sem termos técnicos.
5. Conferir o checklist inteiro com o usuário; não pular itens.

## 2. Publicar
| Alvo | Como | Observação |
| --- | --- | --- |
| Web | merge na `main` → Vercel publica | promover para produção conforme o fluxo do projeto |
| iOS/Android (build nativo) | `eas build --profile production` e `eas submit` | necessário quando muda código nativo, permissões ou SDK |
| Correção só de JavaScript | `eas update --branch production` | atualização OTA, sem revisão da loja; respeitar as regras das lojas |

Criar a tag `vX.Y.Z` após publicar.

## 3. Lançamento gradual
- Lojas: liberação em fases (Apple) e lançamento gradual por percentual (Google Play): 10% → 50% → 100%.
- Funcionalidades novas atrás de feature flag no PostHog, ligadas por percentual.
- Entre etapas, 24–48 h e leitura do Sentry; avançar só com sessões sem falha > 99%.
- Registrar cada etapa na tabela do T06. Não iniciar na sexta.

## 4. Plano de volta
- Web: voltar o deploy anterior no Vercel.
- Mobile: pausar o lançamento gradual; OTA da versão anterior quando aplicável.
- Funcionalidade: desligar a flag.
- Banco: migração reversa ou restauração (plano de incidentes T13).

## 5. Depois
- Comunicar no canal da equipe.
- Após 2 semanas, medir a hipótese da versão e registrar no T06.
- Atualizar `docs/registro.md` (E4.7 ou E5.4).
