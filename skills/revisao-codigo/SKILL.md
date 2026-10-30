---
name: revisao-codigo
description: Checklist de revisão de código do processo — segurança, dados pessoais/LGPD, regras de acesso, desempenho, acessibilidade, testes, analytics e padrões do projeto — com classificação por gravidade. Use ao revisar qualquer branch, PR ou diff.
---

# Revisão de código

Classifique cada achado: **Crítico** (bloqueia merge) · **Importante** (antes do lançamento) · **Sugestão**.

## Segurança — itens críticos

- Segredo, chave ou token no código, em teste ou em log.
- Chave `service_role` ou equivalente acessível no cliente.
- Tabela nova sem RLS, ou política que permite acesso a dados de outro usuário.
- Entrada do usuário sem validação em Edge Function / API.
- SQL montado por concatenação de texto.
- Autorização checada só no cliente.
- Webhook sem verificação de assinatura; pagamento sem idempotência.

## Dados pessoais e LGPD

- Dado pessoal novo sem estar no mapa do PRD/arquitetura (finalidade, base legal, retenção).
- Dado pessoal em log, evento de analytics, mensagem de erro ou URL.
- Exclusão de conta deixando dados órfãos (falta `on delete cascade` ou rotina de limpeza).
- Envio de dados a serviço externo não listado na arquitetura.

## Correção e testes

- Algum critério de aceite sem teste correspondente.
- Teste enfraquecido, pulado (`skip`, `only`) ou apagado.
- Estados de erro e vazio não tratados.
- Condições de corrida, `await` faltando, promessas sem tratamento de erro.
- Migração não reversível sem plano de volta.

## Analytics

- Evento previsto na spec ausente, com nome fora do padrão `objeto_acao` ou disparado antes do sucesso.

## Desempenho

- Consulta sem índice em tabela que vai crescer; N+1 (consulta dentro de laço).
- Lista longa sem virtualização; imagem sem dimensão ou sem otimização.
- Re-render excessivo (objeto/função recriado em props de listas).

## Acessibilidade

- Botão/ícone sem label; área de toque < 44×44; contraste insuficiente; quebra com fonte aumentada.

## Padrão do projeto

- Fora das convenções do `CLAUDE.md` (estrutura, nomes, `any`, cores fora do design system).
- Dependência nova sem justificativa.
- Código fora do escopo da spec.

## Sempre informar

Lista das **áreas críticas tocadas** (autenticação, pagamentos, dados pessoais, migrações) — o construtor
lê esses diffs pessoalmente, mesmo que estejam corretos.
