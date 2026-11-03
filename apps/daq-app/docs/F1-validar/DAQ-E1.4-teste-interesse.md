# E1.4 · Teste de interesse — DAQ

Etapa: E1.4 · Responsável: Negócio; Construtor publica a página · Duração: 1 a 2 semanas
Página: [`apps/daq-app/landing/index.html`](../../landing/index.html) · Resultado vai para a T01, seção "Teste de interesse".

> **Status: aguarda aprovação da equipe.** A meta abaixo precisa ser aprovada **antes** de publicar a página ou enviar qualquer
> mensagem. Publicar, impulsionar e mandar mensagens são ações externas: só com confirmação.

## 1. O que o teste mede

**Público:** o **parceiro** (hipótese central, suposição 1). Quem produz notícia local em SC: dono de página ou perfil de cidade,
jornalista, radialista, dono de jornal ou portal pequeno.

**Comportamento medido:** a pessoa **se candidata a parceiro da sua cidade** num formulário que pede cidade, perfil, tamanho da
audiência e contato. Candidatar-se é mais do que "entrar numa lista", então a meta é próxima da referência de lista de espera (~10%).

O comércio (suposição 2) **não** entra nesta página. O teste dele é a venda antecipada presencial já prevista na T01
(≥ 6 de 30 comércios), feita com o parceiro candidato depois desta etapa.

## 2. Meta (fixada antes · proposta, aguarda aprovação)

| Item | Meta |
| --- | --- |
| Visitantes qualificados | **≥ 200** vindos dos canais qualificados (abaixo), medidos por `utm_source` |
| Candidaturas completas | **≥ 10%** dos visitantes qualificados (≥ 20 com 200 visitantes) |
| Espalhamento | Candidatos de **≥ 10 cidades ou bairros diferentes** |
| Cidades-piloto | **≥ 1 candidato** em cada cidade-piloto (Pomerode, Rio do Sul, bairro de Florianópolis) |
| Qualidade | **≥ 50%** das candidaturas com audiência atual ≥ 1.000 pessoas (seguidores, membros ou ouvintes) |

**Como ler o resultado**
- Bateu todas: sinal forte para a suposição 1 → seguir para as cartas de intenção.
- Bateu a conversão mas não o espalhamento: o interesse existe mas é concentrado. Rever as cidades.
- Menos de 5%: a oferta não atrai. Rever a taxa e o texto antes de qualquer construção.

## 3. Duas versões do texto (A/B)

As duas têm o mesmo título e a mesma chamada. **Muda só a forma de entrada (a taxa)**, que é a maior dúvida aberta (regra C1).
A página sorteia a versão para cada visitante e guarda no formulário qual ele viu.

| | Versão A · taxa em anúncio | Versão B · começa pagando em conteúdo |
| --- | --- | --- |
| Bloco "Quanto custa" | "Você não paga mensalidade. A plataforma fica com a receita do 1º anúncio que você vender no mês. Todos os outros anúncios locais são 100% seus." | "Você não paga mensalidade nem entrega anúncio no começo. Até a sua página se pagar, você cede algumas matérias de serviço por mês para a rede. Depois, a plataforma fica só com a receita do 1º anúncio do mês. O resto é 100% seu." |

**Atenção:** com 200 a 500 visitantes, a diferença entre A e B só é confiável se for grande (ex.: 6% contra 14%). Diferença
pequena = empate; nesse caso, decidir pelas entrevistas da E1.3.

**Texto comum (as duas versões)**
- **Título:** A notícia da sua cidade pode virar o seu negócio.
- **Subtítulo:** Uma rede de notícias de Santa Catarina em que cada cidade e bairro tem um parceiro local. Você publica; a
  plataforma entrega a página, a venda de anúncios, a cobrança e o relatório para o comércio.
- **3 benefícios:**
  1. **Venda sem improviso:** tabela de preços, contrato, cobrança por Pix e nota fiscal prontos.
  2. **Prova de resultado para o comércio:** cada anúncio tem botão de WhatsApp e o anunciante recebe um relatório todo mês.
  3. **Sua marca, sua cidade:** a comunidade da sua cidade é sua, e você pode trazer a página que já tem.
- **Chamada única:** Quero ser o parceiro da minha cidade.
- **Honestidade obrigatória:** a página diz que o projeto **está em teste** e que a candidatura **não é contrato**. **Sem promessa
  de ganho** (risco de parecer oferta de franquia; ver T01, Crítica item 3).

## 4. Canais de tráfego (200 a 500 visitantes qualificados)

O público é pequeno (algumas centenas de pessoas em SC), então o tráfego vem de **abordagem direta**, não de anúncio amplo.

| Canal | Como | `utm_source` | Visitantes esperados **[estimativa]** |
| --- | --- | --- | --- |
| Mensagem direta a páginas e perfis de notícia de cidades de SC | Negócio manda mensagem individual (Instagram/Facebook) com o link, 150–300 contatos | `dm` | 60–150 |
| Grupos e listas de jornalistas e comunicadores de SC | Postagem com o link, com permissão do administrador | `grupos` | 40–100 |
| Rádios e jornais pequenos | E-mail ou mensagem ao responsável | `veiculos` | 20–50 |
| Anúncio pago na Meta, só SC, interesse em jornalismo ou gestão de páginas | R$ 300–600 no total **[estimativa]**, 7 dias | `meta` | 100–250 (menos qualificado) |
| Indicação dos entrevistados da E1.3 | Link ao fim da entrevista, depois do bloco opcional | `entrevista` | 10–20 |

Visitas sem `utm_source` contam no total, mas **não** como qualificadas.

## 5. Antes de publicar (checklist)

- [ ] Equipe aprova a meta (seção 2) e os textos (seção 3).
- [ ] Escolher onde publicar (ex.: Cloudflare Pages, Netlify ou GitHub Pages; todos grátis para uma página estática).
- [ ] Criar o formulário de destino e colar o endereço em `FORM_ENDPOINT` (ex.: Formspree, Tally ou Google Apps Script). Os
      contatos ficam **nesse serviço**, nunca no repositório.
- [ ] Ativar a contagem de visitas sem cookies (ex.: Cloudflare Web Analytics ou Plausible) e colar o código no lugar indicado no `<head>`.
- [ ] Preencher o e-mail de contato da privacidade (`CONTATO_PRIVACIDADE`).
- [ ] Testar no celular: abrir com `?v=a` e `?v=b`, enviar uma candidatura de teste e conferir que chegou com a versão e o `utm_source`.
- [ ] Confirmação explícita antes de publicar e antes de cada canal de divulgação.

## 6. Registro do resultado

| Data | Canal | Visitantes | Candidaturas | Versão A (visitas / cand.) | Versão B (visitas / cand.) |
| --- | --- | --- | --- | --- | --- |
| | | | | | |
