---
description: Mostra em que etapa o app está, o que está pendente e o que vem a seguir
argument-hint: [pasta do app, ou vazio para todos os apps do diretório]
---

Use a skill `processo-apps`. Leia `docs/registro.md` do app informado em "$ARGUMENTS"
(se vazio: do diretório atual; se houver várias pastas `*-app/`, de todas).

Responda de forma curta, em português:

1. **Fase atual** e último portão decidido (com data, de `docs/portoes.md`).
2. **Em andamento / em revisão:** etapas, desde quando, e o que falta para o critério de pronto.
3. **Próximas etapas** que já têm o gatilho cumprido, com responsável.
4. **Alertas:** etapas puladas sem justificativa; saídas citadas no registro que não existem no disco;
   etapas paradas há mais de 7 dias; portão pendente com todas as etapas da fase concluídas.
5. Para vários apps: uma linha por app (sigla · fase · próxima etapa · alerta).

Não altere nenhum arquivo.
