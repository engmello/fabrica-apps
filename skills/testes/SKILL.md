---
name: testes
description: Escreve e organiza testes no padrão do projeto — unitários (Vitest), de interface (Testing Library), de regras de acesso (RLS com dois usuários) e de ponta a ponta (Playwright na web, Maestro no mobile) — a partir dos critérios de aceite. Use ao implementar qualquer tarefa, antes do código, ou quando faltar cobertura.
---

# Testes

## Princípio
Os testes nascem dos **critérios de aceite** e são escritos **antes** do código. Cada critério "Dado / Quando / Então"
vira pelo menos um teste com o mesmo nome.

```ts
describe('H2 — Registrar despesa rápida', () => {
  it('dado a tela inicial, quando informo valor e categoria, então a despesa aparece no topo', async () => { … });
  it('dado sem valor, quando toco em salvar, então vejo "Informe o valor" e nada é salvo', async () => { … });
});
```

## Onde ficam e quando usar
| Tipo | Ferramenta | Onde | Quando |
| --- | --- | --- | --- |
| Unitário | Vitest | ao lado do código (`*.test.ts`) | regras de negócio, hooks, utilitários |
| Interface | Testing Library | ao lado da tela (`*.test.tsx`) | estados da tela e interações |
| Regras de acesso | Vitest + cliente Supabase local | `supabase/tests/` | toda tabela nova (usuário A não vê dados de B) |
| Ponta a ponta web | Playwright | `tests/e2e/` | caminho até o momento de valor, login, pagamento |
| Ponta a ponta mobile | Maestro (`.yaml`) | `tests/maestro/` | mesmo caminho no app |

## Regras
- Interaja como o usuário: buscar por texto, label ou papel; nunca por classe CSS ou id interno.
- Um comportamento por teste; nomes em português, descrevendo o comportamento.
- Sem dados pessoais reais: use fábricas com dados fictícios.
- Teste os quatro estados de cada tela (carregando, erro, vazio, conteúdo).
- Teste de ponta a ponta só para os caminhos críticos — são lentos; o resto fica no unitário.
- **Nunca** use `skip`, `only` ou afrouxe uma asserção para fazer passar. Se o teste estiver errado, explique e pergunte.
- Teste instável (passa e falha sem mudança) é bug: corrija ou abra cartão, não ignore.

## Cobertura mínima
- 100% dos critérios de aceite com teste.
- Toda tabela com teste de RLS.
- Caminho até o momento de valor com teste de ponta a ponta antes do P3.
