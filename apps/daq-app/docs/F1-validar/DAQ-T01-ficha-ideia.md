# T01 · Ficha da ideia — Daqui SC

Etapas: E0.1, E1.1, E1.2, E1.4, E1.5 · Local: `docs/F1-validar/DAQ-T01-ficha-ideia.md`

> Legenda: **[suposição]** = ainda não validado. Nesta fase quase tudo é suposição.

| Campo | Preencher |
| --- | --- |
| Sigla | DAQ |
| Data | 2026-11-02 |
| Proposto por | Produto (a confirmar) |
| Plataformas previstas | iOS / Android primeiro (produto principal) · Web como portal de notícias e página de vendas para parceiros e anunciantes |

## Problema (rascunho E0.1)
Moradores de municípios e bairros de Santa Catarina não têm uma fonte local, confiável e contínua de notícias
sobre o que acontece perto de casa. **[suposição]** A informação local hoje está espalhada em grupos de WhatsApp,
páginas de Instagram, rádios e portais regionais que só cobrem a cidade em fatos grandes. **[suposição]**
Quem produz conteúdo local (jornalistas, comunicadores, donos de páginas) tem dificuldade para viver disso. **[suposição]**
O comércio local não tem um canal barato e medido para alcançar só quem mora ali. **[suposição]**

## Público (rascunho E0.1)
Mercado de três lados, mais a administração:
- **Leitor:** morador do município ou bairro; acesso gratuito; envia notícias, fotos, sugestões de pauta e comenta. Tudo passa por moderação.
- **Parceiro local:** responsável por um município ou bairro, de preferência jornalista (não obrigatório). Paga mensalidade, publica, modera, cuida das redes da página, vende anúncio local e responde pelo conteúdo da sua página.
- **Anunciante local:** comércio e serviços do município ou bairro.
- **Anunciante estadual:** empresas, marcas e órgãos com atuação em todo o estado.
- **Administração da plataforma:** contas de municípios e bairros, parceiros, mensalidades, repasses, moderação de segundo nível (denúncias e remoções) e anúncios estaduais.

Região: Santa Catarina, por município; nas cidades maiores (ex.: Florianópolis, Joinville, Blumenau), por bairro.

## Modelo de receita (rascunho)
- Anúncio local: 100% para o parceiro.
- Anúncio estadual: 10% para o parceiro da página onde aparece, 90% para a plataforma. **[suposição: repasse proporcional às exibições na página dele]**
- Plataforma: mensalidades dos parceiros + 90% dos anúncios estaduais.
- Valor da mensalidade: **não definido**; testar na validação.

## Funcionalidades previstas (rascunho, não é escopo do MVP)
- Página padronizada por município/bairro: texto, fotos, vídeos e integração forte com redes sociais (compartilhar, publicar, trazer conteúdo).
- Notícia em formato padrão: título, resumo, corpo, mídia, categoria, local, autor.
- Participação do leitor com fila de moderação do parceiro e canal de denúncia para a plataforma.
- Espaços de anúncio locais e estaduais, relatório para o anunciante e cálculo automático de repasses.
- Painel do parceiro: conteúdo, moderação, anúncios vendidos, receita.
- Painel administrativo: municípios/bairros, parceiros, mensalidades, repasses, anúncios estaduais, moderação.

## Hipótese em uma frase (E1.1 · v1, em revisão)

São três lados. Todas as frases são **[suposição]** até as entrevistas (E1.3) e o teste de interesse (E1.4).

**Parceiro (quem paga a plataforma; hipótese central):**
> Para **jornalistas, comunicadores e donos de páginas de notícia de uma cidade ou bairro de SC** que sofrem com
> **não conseguir viver do conteúdo local, por falta de estrutura, marca e um jeito organizado de vender anúncio**,
> **um espaço exclusivo do seu território, com publicação, moderação, venda de anúncios e relatórios prontos**, resolve
> porque **profissionaliza o trabalho e fica com 100% do anúncio local que vender**, ao contrário de **manter sozinho um
> perfil de Instagram, grupo de WhatsApp ou site próprio e vender "publi" avulsa sem medição**.

**Leitor:**
> Para **moradores de cidades pequenas e médias e de bairros das cidades grandes de SC** que sofrem com **saber do que
> acontece perto de casa só por boato em grupo de WhatsApp ou por páginas sem responsável**, **uma página local com
> notícia verificada por alguém da região e espaço para enviar fatos e fotos** resolve porque **junta num só lugar
> informação confiável e a voz do bairro**, ao contrário de **grupos de WhatsApp, páginas de Instagram e portais
> regionais que só falam da cidade quando há tragédia**.

**Anunciante local:**
> Para **comércio e serviços de um município ou bairro** que sofrem com **gastar em impulsionamento, rádio ou panfleto
> sem saber se alcançou quem mora perto**, **um anúncio na página da cidade, vendido por alguém conhecido e com relatório
> de exibições e cliques**, resolve porque **atinge só o público local e mostra o resultado**, ao contrário de
> **impulsionar no Instagram (difícil de operar e sem foco local) ou anunciar na rádio (sem medição)**.

**Anunciante estadual** (lado secundário; depende da escala da rede):
> Para **marcas, redes e órgãos com atuação em SC** que sofrem com **chegar ao interior só pelos grandes grupos, que se
> concentram nas cidades maiores**, **uma rede de páginas locais com compra única e escolha de municípios** resolve
> porque **alcança muitas cidades pequenas num contexto local confiável**, ao contrário de **comprar mídia cidade a
> cidade ou só nos portais estaduais**.

## Suposições mais arriscadas (ordem de risco)

As metas são uma proposta e devem ser aprovadas pela equipe **antes** de qualquer teste. Os valores em R$ são **[suposição]**.
As três primeiras são as que a E1.1 exige; as demais seguem a ordem de risco.

| # | Suposição | Como testar | Meta que confirma | Resultado |
| --- | --- | --- | --- | --- |
| 1 | **(a) Há pessoas dispostas a pagar mensalidade para ser parceiro, e o valor que aceitam paga a plataforma.** | Entrevistar 10 candidatos (jornalistas locais, donos de páginas e perfis de cidade, radialistas) nas cidades-piloto. Depois, oferta real em 3 faixas (R$ 149 · R$ 299 · R$ 499/mês), cada candidato vendo uma só, com carta de intenção e sinal reembolsável (ex.: 1º mês). | ≥ 3 de 10 candidatos pagam o sinal em alguma faixa; ao menos 1 na faixa de R$ 299 ou mais. | |
| 2 | **(b) O comércio local compra anúncio de um parceiro na página da cidade.** | Venda antecipada, numa cidade-piloto, de um pacote de lançamento (ex.: R$ 150/mês por 3 meses) para 30 comércios abordados pelo parceiro candidato com a equipe. | ≥ 6 de 30 (20%) assinam com pagamento ou pedido firme. | |
| 3 | **(c) Uma cidade pequena gera audiência suficiente para o anúncio ter valor.** E o leitor instala e volta a um **app**, em vez de seguir no WhatsApp ou no Instagram. | Página-piloto de 6 semanas (canal de WhatsApp + Instagram + web simples) com o parceiro publicando todo dia; depois, convite para instalar o app (lista de espera ou beta). | Alcance único mensal ≥ 20% da população adulta; ≥ 30% de leitores voltando toda semana; ≥ 5% da audiência entra na lista do app. | |
| 4 | **Um parceiro consegue, sozinho, produzir, moderar, cuidar das redes e vender anúncio, e ganhar o suficiente para ficar.** | Acompanhar o tempo e a receita dos parceiros-piloto por 6 semanas (diário de horas). | Publica ≥ 1 notícia/dia útil em ≤ 4 h/dia; receita de anúncio ≥ 2× a mensalidade ao fim do piloto. | |
| 5 | **(e) Anunciantes estaduais pagam por alcance distribuído em muitas cidades pequenas.** | 8 entrevistas com agências e anunciantes de SC (rede de varejo, cooperativa, banco regional, órgão público); pedir proposta para uma campanha-teste. | ≥ 2 de 8 pedem proposta com valor; ≥ 1 aceita um piloto pago. | |
| 6 | **(d) Os leitores participam enviando conteúdo, e a moderação dá conta do volume.** | No piloto: formulário de envio (WhatsApp ou web) e registro do volume e do tempo de moderação. | ≥ 3 envios aproveitáveis por semana por página; moderação ≤ 30 min/dia; nenhum envio aguarda mais de 24 h. | |
| 7 | **O risco jurídico do conteúdo (parceiro e leitor) é administrável a um custo aceitável.** | Parecer de advogado de mídia/digital sobre o modelo (ver Crítica, item 2) antes do P1. | Parecer sem impedimento; custo de conformidade (termos, contrato, seguro, processo de remoção) cabe no cenário provável da E1.5. | |

## Crítica cética (E1.1, passo 3)

Objetivo: tentar derrubar a ideia antes de gastar com ela. Itens com **[a confirmar]** precisam de fonte ou parecer.

### 1. Concorrência em SC: o espaço é menos vazio do que parece
- **Portais estaduais:** ND+ (Grupo ND) e NSC Total (NSC Comunicação, afiliada da Globo) dominam a audiência digital e
  vêm abrindo sucursais no interior. Cobrem as cidades grandes e médias, mas raramente o bairro ou a cidade pequena no dia a dia.
- **Redes regionais com venda unificada:** a ADI-SC lançou a **SCPortais**, uma rede de portais regionais **integrada
  comercialmente** para campanhas no interior. É concorrente direta do lado do **anunciante estadual** e pode ser concorrente,
  ou canal de recrutamento, do lado do parceiro. **[a confirmar o tamanho e a situação atual na E1.2]**
- **Jornais e portais locais** (filiados à Adjori-SC e independentes) e **rádios AM/FM locais**: já têm a relação com o
  comércio, que é exatamente o que o parceiro precisa construir. Muitas rádios mantêm site e Instagram.
- **Grupos de WhatsApp e páginas de Instagram ("Acontece em…", "Fulano News")**: é o concorrente real do leitor. São
  grátis, imediatos e já instalados. O app só vence se oferecer algo que eles não oferecem (confiança, organização, arquivo),
  e mesmo assim o leitor pode preferir receber no WhatsApp.
- **Lado bom:** o Atlas da Notícia (2024, citado em estudo da UFSC de 2025) aponta que 124 dos 295 municípios de SC não
  têm veículo local de notícia e cerca de 2/3 têm nenhum ou poucos. Há "desertos de notícia", mas costumam ser os
  municípios menores, com menos comércio para pagar a conta. **[a confirmar na E1.2]**
- **Conclusão:** o diferencial não pode ser "ter notícia local"; tem que ser **o modelo de negócio para o parceiro**.
  Na E1.2, pesquisar quem já faz "rede de jornalistas locais" (no Brasil e fora) e por que deu certo ou falhou.

### 2. Responsabilidade legal pelo conteúdo
Isto exige parecer de advogado antes do P1. Os pontos abaixo **não são orientação jurídica [a confirmar]**.
- **Marco Civil, art. 19, e a decisão do STF (jun/2025, Temas 987 e 533):** o STF declarou o art. 19 parcialmente
  inconstitucional. Em regra, o provedor passa a poder responder por conteúdo ilícito de terceiro **depois de notificação
  extrajudicial**, sem esperar ordem judicial. Para **crimes contra a honra** continua valendo a ordem judicial. Há regra mais
  dura para **conteúdo pago ou impulsionado**. Recursos (embargos) ainda estavam em análise; conferir o texto final da tese.
- **Moderação prévia é controle editorial.** Se todo conteúdo do leitor passa pela aprovação do parceiro antes de ir ao
  ar, o parceiro (e talvez a plataforma) deixa de ser "mero hospedeiro" daquilo e pode responder como se fosse autor ou editor.
  Moderar tudo antes reduz o risco de conteúdo ruim no ar, mas aumenta a responsabilidade por cada coisa aprovada. É preciso
  decidir conscientemente qual conteúdo é editorial e qual é comentário.
- **Conteúdo do parceiro é jornalístico**, e quem responde é o autor ou editor. A plataforma, com marca própria ("Daqui SC"),
  pode ser vista como **veículo de comunicação** e não só como provedor. Nesse caso entra no polo das ações e da
  **Lei 13.188/2015 (direito de resposta)**: pedido em até 60 dias da publicação, resposta em até 7 dias, senão ação judicial
  com rito rápido. Precisa de processo, prazo e responsável definidos em contrato.
- **Período eleitoral:** notícia local é muito política. Há regras de propaganda eleitoral, impulsionamento e publicidade
  institucional (órgãos públicos ficam impedidos de anunciar nos 3 meses antes da eleição, Lei 9.504/97, art. 73). As próximas
  eleições municipais são em 2028; as gerais de 2026 acabaram de passar.
- **LGPD e imagem:** fotos enviadas por leitores trazem rostos, placas e às vezes menores (ECA). Exigem termo de envio,
  cessão de direitos, base legal e processo de remoção.
- **Contrato com o parceiro:** precisa de cláusula de responsabilidade solidária ou regressiva, padrão editorial mínimo,
  dever de checagem e remoção, e seguro de responsabilidade civil **[a avaliar]**.

### 3. Parceiro pagante: parece franquia, e a rotatividade pode matar o modelo
- **Risco de virar franquia sem querer.** Usar a marca + sistema + método + taxa periódica + território exclusivo é muito
  parecido com franquia. Pela **Lei 13.966/2019**, isso exige **Circular de Oferta de Franquia (COF)** entregue 10 dias antes
  da assinatura, sob pena de anulação e devolução de valores. **[a confirmar com advogado]** Alternativa: estruturar como
  licença de software (SaaS) + contrato de parceria editorial, sem promessa de ganho.
- **Promessa implícita de renda.** Se o parceiro paga para entrar e não fatura, a percepção vira "paguei para trabalhar",
  um risco de reputação no boca a boca das cidades pequenas.
- **Conta do parceiro [suposição]:** numa cidade de 30 mil habitantes, 10 anunciantes a R$ 150 dão R$ 1.500/mês. Menos a
  mensalidade de R$ 299, sobra ~R$ 1.200 para um trabalho que pede horas todos os dias. Isso só fecha como **renda extra**
  de quem já faz isso (dono de página, radialista) ou em cidades maiores. Espere rotatividade alta nos primeiros 3–6 meses.
- **Como reduzir a rotatividade:**
  1. Carência ou mensalidade baixa nos primeiros 3 meses, subindo conforme o parceiro vende (ou mensalidade proporcional à receita).
  2. Recrutar quem **já tem audiência e relação com o comércio**, não quem começa do zero.
  3. Kit de vendas pronto (tabela de preços, mídia kit automático, contrato, cobrança e nota pela plataforma).
  4. Conteúdo estadual de base (serviço, tempo, estradas) para a página não ficar vazia quando o parceiro falha.
  5. Território exclusivo condicionado a metas mínimas de publicação.
  6. Plano de saída: o que acontece com a página, os leitores e os anunciantes quando o parceiro sai.

### 4. "Ovo e galinha": por onde começar
- São três lados mais a escala estadual. Sem audiência não há anunciante; sem anunciante o parceiro não paga; sem parceiro
  não há conteúdo nem audiência.
- **Começar pelo parceiro** (oferta): é quem paga, quem traz audiência própria e quem vende para o comércio. Um bom parceiro
  resolve os outros dois lados localmente.
- **Atrair parceiros que já têm audiência** (páginas de cidade com seguidores, blogs, rádios) e oferecer a eles ferramenta e
  receita, não só "um espaço".
- **Anunciante estadual por último:** só faz sentido com dezenas de cidades ativas.
- **Crítica ao "app primeiro" (não é mudança de plano; é para a equipe decidir):** a decisão está tomada, mas é a mais cara de
  desfazer. O leitor de cidade pequena já está no WhatsApp e no Instagram. Dá para validar as suposições 1 a 4 em 6 semanas
  **sem app**: parceiro publicando em canal de WhatsApp + Instagram + página web simples, com venda manual de anúncio. O app entra
  quando houver prova de que parceiros pagam e comércio compra.

### 5. Economia da plataforma (0% do anúncio local)
- A plataforma só ganha com **mensalidade** (cresce com o número de parceiros, não com o sucesso deles) e com **anúncio
  estadual** (depende de escala). No começo, o incentivo fica desalinhado: o parceiro só ganha se vender, e a plataforma ganha
  de qualquer jeito, até ele sair.
- **Teto das mensalidades [suposição]:** SC tem 295 municípios (Atlas da Notícia/IBGE). Somando ~60 bairros nas cidades
  grandes, são ~355 páginas. Com 50% ocupadas a R$ 299, dá ≈ R$ 53 mil/mês no **teto**. Um cenário realista em 12–18 meses
  (20–40 parceiros) dá R$ 6–12 mil/mês.
- **Anúncio estadual [suposição]:** com 30 cidades ativas e ~200 mil leitores/mês, ~4 milhões de exibições/mês a CPM de R$ 15
  e 25% vendido dá ≈ R$ 15 mil/mês brutos, R$ 13,5 mil para a plataforma. A SCPortais disputa o mesmo orçamento.
- **Custo [suposição]:** uma equipe enxuta (produto/construção, comercial estadual, suporte e moderação de 2º nível) + infra +
  jurídico custa facilmente R$ 30–40 mil/mês. **Seriam precisos 100+ parceiros pagantes** ou anúncio estadual forte para empatar.
  A E1.5 deve fazer essa conta com números reais.
- **Ideias para testar:** (1) pequena taxa (10–20%) sobre o anúncio local **vendido e cobrado pela plataforma**, em troca de
  cobrança, nota fiscal e relatório automáticos; (2) mensalidade escalonada pelo tamanho da cidade; (3) serviços pagos ao
  parceiro (gestão de redes, vídeo, cobertura de eventos).

### Veredito do cético
O ponto mais fraco não é a tecnologia nem a notícia. É a **conta do parceiro** (ele ganha o suficiente para pagar e ficar?) e a
**conta da plataforma** (com 0% do local, ela precisa de muitos parceiros). A hipótese central deve ser a do parceiro; a do leitor
vem depois. Se as suposições 1 e 2 falharem nas cidades-piloto, reformular o modelo de receita antes de pensar no app.

## Cidades sugeridas para o teste (E1.1 · proposta)

**Critérios:**
1. **Existe um candidato a parceiro** com audiência ou relação com o comércio. Este é o critério que decide; sem ele a cidade cai.
2. Um tamanho diferente em cada piloto: cidade pequena, cidade média e um bairro de cidade grande (testa o modelo de bairro).
3. Identidade local forte e comércio de rua ativo.
4. Cobertura local existente fraca ou fragmentada (consultar o Atlas da Notícia).
5. A equipe consegue ir presencialmente. **[a confirmar onde a equipe está]**

| # | Cidade | Perfil | Por quê | O que testa |
| --- | --- | --- | --- | --- |
| 1 | **Pomerode** | Pequena, ~34 mil hab. (IBGE 2022) | Identidade forte, turismo e comércio local ativos, perto de Blumenau. | Se cidade pequena gera audiência e anúncio (suposições 2 e 3). |
| 2 | **Rio do Sul** | Média, polo do Alto Vale, ~70 mil hab. **[a confirmar IBGE 2022]** | Polo regional com comércio que atende cidades vizinhas; notícia de utilidade forte (cheias, estradas). | Se a página de uma cidade-polo atrai vizinhos e anunciantes maiores. |
| 3 | **Um bairro de Florianópolis** (ex.: Campeche ou Ingleses) | Bairro populoso de capital | Comunidade ativa em grupos de bairro, comércio próprio, pauta própria (trânsito, obras, praia). | Se o modelo de bairro funciona numa cidade já coberta pela mídia estadual. |

**Alternativas** caso não haja candidato a parceiro: Concórdia ou Videira (oeste, agroindústria), São Bento do Sul ou
Jaraguá do Sul (norte; Jaraguá já tem portais locais fortes, bom para testar concorrência), um bairro de Joinville.
**[a confirmar a cobertura existente na E1.2]**

Fontes consultadas em 2026-11-02:
[Atlas da Notícia / estudo UFSC (via Labcom)](https://ojs.labcom-ifp.ubi.pt/ec/article/download/1637/1131/5690) ·
[SCPortais (ADI-SC)](https://acontecendoaqui.com.br/?p=70393) ·
[ND+ audiência](https://acontecendoaqui.com.br/comunicacao/nd-consolida-lideranca-em-santa-catarina-em-maio-segundo-ivc/) ·
[STF, art. 19, recursos](https://noticias.stf.jus.br/postsnoticias/stf-vai-analisar-recursos-contra-tese-fixada-no-julgamento-do-marco-civil-da-internet/) ·
[Teletime, art. 19 (26/06/2025)](https://teletime.com.br/26/06/2025/art-19-stf-concilia-votos-e-plataformas-terao-responsabilizacao-parcial/) ·
[IBGE Pomerode](https://www.ibge.gov.br/cidades-e-estados/sc/pomerode.html)

## Alternativas atuais
| Alternativa | Tipo | Preço | Reclamações recorrentes |
| --- | --- | --- | --- |
| | | | |

**Diferencial em uma linha:**

## Síntese das entrevistas
- Entrevistas realizadas: __ · Dor confirmada: __%
- Padrões (3+ pessoas):
- Frases representativas (sem nomes):
- Surpresas:

## Teste de interesse
| Item | Valor |
| --- | --- |
| Tipo (lista de espera / pré-venda) | |
| Meta fixada antes | |
| Visitantes qualificados | |
| Conversões | |
| Taxa | |

## Viabilidade
| Item | Pessimista | Provável | Otimista |
| --- | --- | --- | --- |
| Custo para construir o MVP (R$) | | | |
| Custo mensal de operação (R$) | | | |
| Usuários em 12 meses | | | |
| Conversão para pago (%) | | | |
| Preço (R$/mês) | | | |
| Taxa das lojas (%) | | | |
| Receita mensal no mês 12 (R$) | | | |

## Resultado
- [ ] Dor confirmada em 60%+ das entrevistas
- [ ] Meta do teste de interesse atingida
- [ ] Cenário provável cobre os custos em até 12 meses

**Recomendação para o P1:** Seguir / Reformular / Arquivar
