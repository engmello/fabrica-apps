---
name: nova-tela
description: Cria telas e componentes no padrão do projeto (React Native/Expo ou Next.js, TypeScript) — estrutura de pastas, estados de carregando/erro/vazio, acessibilidade, evento de analytics e testes. Use ao implementar qualquer tela ou componente de interface.
---

# Nova tela

## Estrutura

```
src/features/<funcionalidade>/
├── <Nome>Screen.tsx        # tela (mobile) ou page.tsx (web, em app/)
├── components/             # componentes só desta funcionalidade
├── use<Nome>.ts            # hook com dados e lógica (busca, mutações)
└── <Nome>.test.tsx         # testes
```

A tela só monta a interface; dados e regras ficam no hook. Componentes reutilizáveis vão para `src/components/`.

## Checklist obrigatório

- [ ] **Quatro estados**: carregando (skeleton), erro (mensagem + tentar de novo), vazio (explica e sugere a próxima ação), conteúdo.
- [ ] **Acessibilidade**: `accessibilityLabel`/`aria-label` em ícones e botões sem texto; área de toque ≥ 44×44; contraste AA; funciona com fonte aumentada.
- [ ] **Textos** em português, curtos, sem jargão técnico nas mensagens de erro.
- [ ] **Formulários**: validação ao sair do campo e ao enviar; botão desabilitado durante envio; teclado adequado (numérico, e-mail).
- [ ] **Analytics**: evento previsto na spec disparado no hook, após sucesso, sem dados pessoais.
- [ ] **Desempenho**: listas longas com `FlatList`/virtualização; imagens com tamanho definido.
- [ ] Usa componentes e tokens do design system; nada de cores ou tamanhos soltos.

## Testes

- Renderiza cada um dos quatro estados.
- Cada critério de aceite da spec vira um teste (Testing Library: interaja como o usuário, busque por texto/label, não por classe).
- Hook testado separadamente para regras de negócio.

## Exemplo de hook

```ts
export function useDespesas() {
  const query = useQuery({ queryKey: ['despesas'], queryFn: listarDespesas });
  const criar = useMutation({
    mutationFn: criarDespesa,
    onSuccess: (d) => {
      posthog.capture('despesa_registrada', { categoria: d.categoria, offline: false });
      queryClient.invalidateQueries({ queryKey: ['despesas'] });
    },
  });
  return { ...query, criar };
}
```
