# T01 · Ficha da ideia — Daqui SC

Etapas: E0.1, E1.1, E1.2, E1.4, E1.5 · Local: `docs/F1-validar/DAQ-T01-ficha-ideia.md`

> Legenda: **[suposição]** = ainda não validado. Nesta fase quase tudo é suposição.

| Campo | Preencher |
| --- | --- |
| Sigla | DAQ |
| Data | 2026-11-02 |
| Proposto por | Produto (a confirmar) |
| Plataformas previstas | **Web** (plataforma principal): portal de notícias, páginas locais, painéis do parceiro e da administração, e página de vendas para parceiros e anunciantes. App de loja fora do escopo inicial. |

## Problema (rascunho E0.1)
Moradores de municípios e bairros de Santa Catarina não têm uma fonte local, confiável e contínua de notícias
sobre o que acontece perto de casa. **[suposição]** A informação local hoje está espalhada em grupos de WhatsApp,
páginas de Instagram, rádios e portais regionais que só cobrem a cidade em fatos grandes. **[suposição]**
Quem produz conteúdo local (jornalistas, comunicadores, donos de páginas) tem dificuldade para viver disso. **[suposição]**
O comércio local não tem um canal barato e medido para alcançar só quem mora ali. **[suposição]**

## Público (rascunho E0.1)
Mercado de três lados, mais a administração:
- **Leitor:** morador do município ou bairro; acesso gratuito; envia notícias, fotos, sugestões de pauta e comenta. Tudo passa por moderação.
- **Parceiro local:** responsável por um município ou bairro, de preferência jornalista (não obrigatório). Paga a taxa com a receita do 1º anúncio local do mês (depois dos 2 primeiros), publica, modera, cuida das redes da página, vende anúncio local e responde pelo conteúdo da sua página.
- **Anunciante local:** comércio e serviços do município ou bairro.
- **Anunciante estadual:** empresas, marcas e órgãos com atuação em todo o estado.
- **Administração da plataforma:** contas de municípios e bairros, parceiros, taxas (anúncios que valem como taxa), repasses, moderação de segundo nível (denúncias e remoções) e anúncios estaduais.

Região: Santa Catarina, por município; nas cidades maiores (ex.: Florianópolis, Joinville, Blumenau), por bairro.

## Modelo de receita (rascunho)
- Anúncio local: 100% para o parceiro.
- Anúncio estadual: 10% para o parceiro da página onde aparece, 90% para a plataforma. **[suposição: repasse proporcional às exibições na página dele]**
- **Taxa do parceiro paga em anúncio, não em dinheiro:** a receita do 1º anúncio local vendido no mês fica com a
  plataforma; depois a regra passa a ser os 2 primeiros. Os demais anúncios locais são 100% do parceiro.
  **[a definir: quando passa de 1 para 2 anúncios; se a regra conta anúncios ou valor mínimo; e o que acontece
  quando o parceiro não vende nenhum no mês (paga uma mensalidade? carência? perde o território?)]**
- **Fase de entrada, com taxa paga em conteúdo (proposta de 2026-11-02):** enquanto a página não se pagar, o parceiro não entrega
  anúncio como taxa. Ele paga com conteúdo. Regras em "Estratégias de diferenciação", item C1.
- Plataforma: anúncios locais que valem como taxa + 90% dos anúncios estaduais.
- Preço do anúncio local (e, portanto, o valor da taxa): **não definido**; testar na validação.

## Funcionalidades previstas (rascunho, não é escopo do MVP)
- Página padronizada por município/bairro: texto, fotos, vídeos e integração forte com redes sociais (compartilhar, publicar, trazer conteúdo).
- Notícia em formato padrão: título, resumo, corpo, mídia, categoria, local, autor.
- Participação do leitor com fila de moderação do parceiro e canal de denúncia para a plataforma.
- Espaços de anúncio locais e estaduais, relatório para o anunciante e cálculo automático de repasses.
- Painel do parceiro: conteúdo, moderação, anúncios vendidos, receita.
- Painel administrativo: municípios/bairros, parceiros, taxas, repasses, anúncios estaduais, moderação.

## Hipótese em uma frase (E1.1 · v1, aprovada pela equipe em 2026-11-02)

São três lados. Todas as frases são **[suposição]** até as entrevistas (E1.3) e o teste de interesse (E1.4).

**Parceiro (quem paga a plataforma; hipótese central):**
> Para **jornalistas, comunicadores e donos de páginas de notícia de uma cidade ou bairro de SC** que sofrem com
> **não conseguir viver do conteúdo local, por falta de estrutura, marca e um jeito organizado de vender anúncio**,
> **um espaço exclusivo do seu território na web, com publicação, moderação, venda de anúncios e relatórios prontos, sem
> mensalidade em dinheiro (paga com o 1º anúncio do mês)**, resolve porque **profissionaliza o trabalho sem custo fixo e
> fica com 100% dos demais anúncios locais**, ao contrário de **manter sozinho um
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

As metas foram aprovadas pela equipe em 2026-11-02, antes de qualquer teste. Os valores em R$ são **[suposição]**.
As três primeiras são as que a E1.1 exige; as demais seguem a ordem de risco.

| # | Suposição | Como testar | Meta que confirma | Resultado |
| --- | --- | --- | --- | --- |
| 1 | **(a) Há pessoas dispostas a ser parceiro e a entregar a receita do 1º anúncio do mês (depois dos 2 primeiros) como taxa.** | Entrevistar 10 candidatos (jornalistas locais, donos de páginas e perfis de cidade, radialistas) nas cidades-piloto. Depois, oferta real com a regra explicada por escrito, já com a passagem de 1 para 2 anúncios, e assinatura de carta de intenção. | ≥ 3 de 10 assinam com a regra de 2 anúncios explicada; ≥ 2 vendem o 1º anúncio em até 30 dias do início. | |
| 2 | **(b) O comércio local compra anúncio de um parceiro na página da cidade.** É disso que vive o parceiro **e** a plataforma. | Venda antecipada, numa cidade-piloto, de um pacote de lançamento (ex.: R$ 150/mês por 3 meses **[suposição]**) para 30 comércios abordados pelo parceiro candidato com a equipe. | ≥ 6 de 30 (20%) assinam com pagamento ou pedido firme. | |
| 3 | **(c) Uma cidade pequena gera audiência suficiente na web para o anúncio ter valor**, e o leitor volta ao site em vez de ler só no WhatsApp ou no Instagram. | Página-piloto de 6 semanas na web, divulgada por canal de WhatsApp e Instagram, com o parceiro publicando todo dia. | Alcance único mensal ≥ 20% da população adulta; ≥ 30% dos leitores voltam toda semana; ≥ 50% das visitas chegam pelo link compartilhado e seguem para outra notícia. | |
| 4 | **Um parceiro consegue, sozinho, produzir, moderar, cuidar das redes e vender anúncio, e ganhar o suficiente para ficar.** | Acompanhar o tempo e a receita dos parceiros-piloto por 6 semanas (diário de horas). | Publica ≥ 1 notícia/dia útil em ≤ 4 h/dia; vende ≥ 4 anúncios/mês ao fim do piloto (2 de taxa + ≥ 2 dele). | |
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
  grátis, imediatos e já instalados. Ser web ajuda, porque o link abre direto do WhatsApp sem instalar nada. Mas o site só
  vence se oferecer algo que eles não oferecem (confiança, organização, arquivo), e o leitor pode ler o resumo no grupo e não
  clicar. A audiência depende de o parceiro distribuir bem os links.
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

### 3. Parceiro que paga com anúncio: ainda lembra franquia, e a rotatividade pode matar o modelo
- **O que melhorou com a regra "taxa = 1º anúncio":** não há custo fixo para entrar, e a plataforma só ganha quando o parceiro
  vende. Os incentivos ficam alinhados e some o "paguei para trabalhar".
- **Risco de virar franquia sem querer.** Marca + sistema + método + território exclusivo + remuneração periódica (mesmo que
  em anúncio) ainda se parece com franquia. Pela **Lei 13.966/2019**, isso exige **Circular de Oferta de Franquia (COF)**
  entregue 10 dias antes da assinatura. **[a confirmar com advogado]** Alternativa: licença de uso da plataforma +
  contrato de parceria editorial e de representação comercial, sem promessa de ganho.
- **A passagem de 1 para 2 anúncios** dobra a taxa. Se não estiver escrita desde o início (quando e por quê), vai ser lida
  como "mudaram a regra", que é o gatilho clássico de saída. Fixe a data ou o gatilho no contrato.
- **Mês sem venda:** se o parceiro não vende nenhum anúncio, a plataforma não recebe nada e continua com o custo da página.
  É preciso uma regra (carência, mensalidade mínima ou perda do território após N meses).
- **Conta do parceiro [suposição]:** numa cidade de 30 mil habitantes, 10 anunciantes a R$ 150 dão R$ 1.500/mês. Menos 2
  anúncios de taxa, sobram R$ 1.200 para um trabalho que pede horas todos os dias. Só fecha como **renda extra** de quem já
  faz isso (dono de página, radialista) ou em cidades maiores. Espere rotatividade alta nos primeiros 3–6 meses.
- **Quem fica com qual anúncio:** como o 1º anúncio é da plataforma, o parceiro tende a lançar como "1º" o anúncio mais
  barato. A regra precisa de um valor mínimo e a cobrança precisa passar pela plataforma.
- **Como reduzir a rotatividade:**
  1. Começar com 1 anúncio de taxa e só passar para 2 depois de uma data ou de uma meta de receita do parceiro, escrita no contrato.
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
- **Validar antes de construir:** como a plataforma é web, o piloto pode começar com um site simples (páginas da cidade +
  formulário de envio) e venda manual de anúncio. As suposições 1 a 4 se testam em 6 semanas, antes dos painéis e do cálculo
  automático de repasses.

### 5. Economia da plataforma (taxa paga com anúncio)
- A plataforma ganha com o **1º anúncio de cada parceiro ativo** (depois com os 2 primeiros) e com **90% do anúncio estadual**.
  O lado bom é que ela só ganha se o parceiro vende. O lado ruim é que a receita por página fica **presa ao preço do anúncio
  local**, que numa cidade pequena é baixo, e é zero nos meses sem venda.
- **Teto [suposição]:** SC tem 295 municípios (Atlas da Notícia/IBGE). Somando ~60 bairros nas cidades grandes, são ~355
  páginas. Com 50% ativas e 2 anúncios de taxa a R$ 150, dá ≈ R$ 53 mil/mês no **teto**. Um cenário realista em 12–18 meses
  (20–40 parceiros, metade ainda com 1 anúncio) dá R$ 4,5–9 mil/mês.
- **Anúncio estadual [suposição]:** com 30 cidades ativas e ~200 mil leitores/mês, ~4 milhões de exibições/mês a CPM de R$ 15
  e 25% vendido dá ≈ R$ 15 mil/mês brutos, R$ 13,5 mil para a plataforma. A SCPortais disputa o mesmo orçamento.
- **Custo [suposição]:** uma equipe enxuta (produto/construção, comercial estadual, suporte e moderação de 2º nível) + infra +
  jurídico custa facilmente R$ 30–40 mil/mês. **Seriam precisos 100+ parceiros ativos com 2 anúncios** ou anúncio estadual
  forte para empatar. A E1.5 deve fazer essa conta com números reais.
- **Ideias para testar:** (1) valor mínimo para o anúncio que vale como taxa, maior nas cidades maiores; (2) cobrança de todos
  os anúncios pela plataforma (dá controle, nota fiscal e relatório, e evita disputa sobre qual foi o "1º"); (3) serviços pagos
  ao parceiro (gestão de redes, vídeo, cobertura de eventos).

### Veredito do cético
O ponto mais fraco não é a tecnologia nem a notícia. É a **conta do parceiro** (ele ganha o suficiente para pagar e ficar?) e a
**conta da plataforma** (com a taxa presa a 1–2 anúncios locais baratos, ela precisa de muitos parceiros ativos). A hipótese
central deve ser a do parceiro; a do leitor vem depois. Se as suposições 1 e 2 falharem nas cidades-piloto, reformular o
modelo de receita antes de construir os painéis.

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

## Alternativas atuais (E1.2 · pesquisa de 2026-11-02)

O produto é web e não tem equivalente direto nas lojas. As reclamações vêm de dados de pesquisa sobre veículos locais
(Atlas da Notícia, UFSC), de reclamações públicas (Reclame Aqui, DECO, Trustpilot) e de produtos parecidos de fora do Brasil.
**Para SC, a evidência direta ainda é fraca**, e as entrevistas da E1.3 precisam confirmar cada grupo de reclamações.

| # | Alternativa | Tipo (lado que disputa) | Preço | Reclamações recorrentes |
| --- | --- | --- | --- | --- |
| 1 | **Grupos de WhatsApp e páginas de Instagram/Facebook da cidade** ("Acontece em…") | Informal, grátis (leitor; parceiro, se o dono da página não aderir) | Grátis para o leitor; "publi" avulsa negociada no direct, sem tabela pública | Boato e falta de responsável identificado (estudo da Coalizão, 2026; grupo sem administrador na PB); depende do algoritmo; anunciante não recebe medição **[a confirmar na E1.3]** |
| 2 | **Portais e jornais locais independentes** (Adjori-SC reúne ~190 veículos; ex.: Jornal de Pomerode) | Veículo local (parceiro: concorrente **ou** candidato) | Anúncio local em banner, folheto e guia de compras; preço não publicado | 45,7% têm uma pessoa só para produzir; 68% faturam até R$ 25 mil/mês e 21,5% não têm receita (Atlas, dados de 2021); vivem quase só de anúncio local, com conteúdo nacional copiado e clickbait para gerar clique (UFSC, 2025) |
| 3 | **Portais estaduais com sucursais** (NSC Total, ND+, SCC10) | Grande grupo (leitor; anunciante local e estadual) | Grátis para o leitor; mídia cara para o comércio pequeno **[suposição]** | Concentram a cobertura nas cidades grandes; cidades longe dos polos só aparecem em fato grande (UFSC, 2025). O ND abriu sucursal em Rio do Sul, que é uma das cidades-piloto |
| 4 | **Redes comerciais de portais:** SCPortais (ADI-SC) e rcnonline (Adjori-SC, 30+ sites) | Rede de veículos com venda unificada (anunciante estadual) | Campanha por rede; preço não publicado | Já vendem "o interior numa compra só", o mesmo argumento do anúncio estadual do Daqui SC. Não achei dados recentes da SCPortais (lançada em 2017) **[a confirmar se está ativa]** |
| 5 | **Franquia Portal da Cidade** (portais locais, home based, 50+ unidades em 2021) | Franquia de portal local (parceiro: **concorrente direto do modelo**) | Investimento de R$ 5 a 22 mil (anúncio da rede); royalties não informados | Exige dinheiro para entrar; aceita franqueados sem experiência em jornalismo; situação atual e presença em SC **[a confirmar]** |
| 6 | **Site próprio** (WordPress com tema de notícias, "portal pronto" vendido no Hotmart) | Faça você mesmo (parceiro) | Pagamento único, ou R$ 100–170/mês segundo um vendedor **[alegação de vendedor]** | Entrega o site, mas não traz audiência, venda de anúncio, cobrança nem relatório; manutenção fica com o dono **[suposição]** |
| 7 | **Impulsionamento no Instagram/Facebook (Meta)** | Autoatendimento (anunciante local) | A partir de poucos reais por dia | Conta de anúncio bloqueada sem explicação, saldo retido, recurso sem resposta (Reclame Aqui e DECO, 2026); impulsionar aumenta o alcance mas não traz cliente se o público estiver mal definido (guias de marketing) |
| 8 | **Rádio local AM/FM** (Rio do Sul tinha 6 emissoras em 2015) | Veículo local (anunciante local; parceiro: candidato) | Pacote de spots **[preço a levantar]** | Sem medição de quem ouviu **[suposição]**; tem a relação com o comércio que o parceiro precisa |
| 9 | **Rede social de bairro** (Nextdoor, fora do Brasil) | Plataforma de bairro (leitor) | Grátis; cobra de empresas | Moderação inconsistente, banimento sem explicação, feed tomado por reclamação e briga (Trustpilot e Capterra); recurso pago para empresa comentar (análise de avaliações, ago/2026) |
| 10 | **Redes hiperlocais de fora** (Patch, TAPinto, Axios Local, Village Media) | Referência de modelo (parceiro e plataforma) | TAPinto: US$ 5 mil na entrada + US$ 500–700/mês + 10% da receita de anúncio | Patch: cresceu rápido demais e em 2012 só 100 de 900 sites davam lucro; virou lucrativo depois de cortar custo e ser vendido. Axios Local ainda não dá lucro (mai/2026). Village Media só entra em cidade com hábito de ler notícia local |

**Grupos de reclamação**
1. **Quem produz trabalha sozinho e mal ganha** (alternativas 2, 5, 6): falta estrutura para vender e cobrar anúncio, e a receita depende de anúncio avulso.
2. **Entrar custa dinheiro** (5, 10): franquias cobram entrada e mensalidade antes de o parceiro vender qualquer coisa.
3. **O comércio paga sem saber o resultado** (1, 7, 8): publi sem medição, rádio sem medição e Meta difícil de operar e sujeita a bloqueio.
4. **O leitor não confia na fonte** (1, 9): boato, falta de responsável e moderação que parece arbitrária.
5. **O vazio é menor do que parece** (3, 4, 5): já existem uma franquia de portal local, redes que vendem o interior a anunciantes e sucursais dos grandes grupos.

**Diferencial em uma linha:** é a única opção em que o parceiro local entra **sem investimento nem mensalidade** e recebe pronto o que
hoje ninguém entrega junto (página com marca, venda, cobrança e relatório de anúncio para o comércio), com a plataforma ganhando só
quando ele vende.

*Justificativa:* responde aos grupos 1, 2 e 3. Os grupos 4 e 5 continuam abertos: a confiança do leitor depende do parceiro, não da
plataforma, e o anúncio estadual já tem concorrentes (SCPortais e rcnonline).

**Sinais de alerta**
- **O Portal da Cidade já faz "portal local com dono local" em escala nacional.** É preciso descobrir se está em SC e por que os
  franqueados ficam ou saem. Esse é o melhor dado disponível sobre a suposição 1.
- **Nas cidades-piloto já existe cobertura:** Pomerode tem o Jornal de Pomerode, com portal próprio (a Alesc registrou 100 mil
  visualizações num dia), e Rio do Sul tem sucursal do ND. Os dois casos podem ser **candidatos a parceiro**, e não só concorrentes.
- **Nenhum modelo de fora** cobra a taxa em anúncio. O TAPinto cobra mensalidade **e** porcentagem. Não há caso para copiar,
  e o risco da suposição 1 continua alto.

**O que isso muda para a E1.3 (entrevistas)**
- Parceiros: perguntar a donos de páginas, jornais e rádios como vendem e cobram anúncio hoje, quanto ganham, se já foram
  procurados pelo Portal da Cidade ou pela SCPortais, e o que os faria entrar numa rede.
- Comércio: perguntar onde anunciou da última vez, quanto pagou, como soube se deu resultado e se já teve problema com a Meta.
- Incluir na lista de entrevistas o Jornal de Pomerode e um veículo de Rio do Sul, sem gravar nomes no documento.

## Estratégias de diferenciação para atrair clientes (ideias · 2026-11-02)

Pedido do proponente, a partir da E1.2. Cada ideia responde a um grupo de reclamação (G1 a G5, acima).
Todas são **[suposição]**: entram como perguntas na E1.3 e como oferta no teste de interesse da E1.4.

### A. Anunciante local (comércio)
| # | Ideia | Por que diferencia | Grupo |
| --- | --- | --- | --- |
| A1 | **Botão de WhatsApp e de ligação em todo anúncio**, contando cada contato gerado | O comércio vê clientes, não "exibições". A rádio e a publi avulsa não medem isso | G3 |
| A2 | **Relatório mensal simples no WhatsApp** do anunciante (exibições, cliques, contatos e comparação com o mês anterior) | Prova o resultado sem exigir que ele entre num painel | G3 |
| A3 | **Primeiro mês de teste** com meta de contatos combinada antes; se não bater, o 2º mês sai pela metade | Tira o risco da primeira compra, que é a maior barreira do comércio pequeno | G3 |
| A4 | **Guia comercial da cidade:** página fixa de cada negócio (horário, endereço, WhatsApp, fotos) como plano de entrada barato | É a porta de entrada para o anúncio; o leitor usa como lista telefônica | G3 |
| A5 | **Matéria "Conheça o comércio"** feita pelo parceiro (texto, fotos e vídeo curto), publicada no portal e nas redes | Conteúdo patrocinado já é a forma que funciona nos portais locais de SC (UFSC, 2025) | G1, G3 |
| A6 | **Ofertas da semana e folheto digital** do mercado, da farmácia e da loja | Formato que os portais do interior já vendem, agora com medição | G3 |
| A7 | **Pacotes de datas locais** (festa da cidade, Natal, volta às aulas, eventos de bairro) | Venda pronta e sazonal, mais fácil de o parceiro oferecer | G1 |
| A8 | **Contrato, cobrança por Pix recorrente e nota fiscal pela plataforma**, com atendimento humano | Contraste com a Meta: sem bloqueio sem explicação e sem saldo retido | G3 |
| A9 | **Selo "Apoia o jornalismo da cidade"** para o anunciante usar na loja e nas redes | Anunciar vira imagem local, não só mídia | G4 |

### B. Leitor (gera a audiência que o anúncio vende)
| # | Ideia | Por que diferencia | Grupo |
| --- | --- | --- | --- |
| B1 | **Utilidade diária:** alertas da Defesa Civil e de cheias, estradas, falta de água e luz, farmácia de plantão, vagas de emprego, falecimentos | É o que o grupo de WhatsApp espalha sem organizar; faz o leitor voltar todo dia | G4 |
| B2 | **Canal oficial no WhatsApp** com resumo do dia e link para a notícia | Usa o canal onde o leitor já está e traz o clique para o portal | G4 |
| B3 | **Responsável identificado e "corrigimos" público** em cada notícia | Resposta direta ao boato e à página sem dono | G4 |
| B4 | **"Isso é verdade?":** o leitor manda o que recebeu no grupo e o parceiro checa | Transforma o boato em pauta e em audiência | G4 |
| B5 | **Agenda da cidade e classificados grátis do leitor** | Traz quem não lê notícia; o classificado também é inventário de anúncio | G3, G4 |

### C. Parceiro
| # | Ideia | Por que diferencia | Grupo |
| --- | --- | --- | --- |
| C1 | **Taxa paga em conteúdo até a página se pagar** (detalhe abaixo) | Nenhuma alternativa permite começar sem pagar nem entregar receita; a franquia cobra entrada | G1, G2 |
| C2 | **Trazer a página que ele já tem:** o dono de página, rádio ou jornal entra na rede sem perder sua marca ("Fulano News, na rede Daqui SC") | Recruta quem já tem audiência, que é o que a crítica e a Village Media recomendam | G1, G5 |
| C3 | **Kit de vendas pronto:** tabela de preço sugerida, mídia kit automático com os números da página e roteiro de abordagem | Ataca o "trabalha sozinho e não sabe vender" | G1 |
| C4 | **Conteúdo estadual de base** (tempo, estradas, serviço) para a página nunca ficar vazia | Reduz a carga de quem tem uma pessoa só | G1 |

#### C1 · Taxa paga em conteúdo até a página se pagar
- **Regra proposta:** na fase de entrada, o parceiro não entrega o 1º anúncio do mês como taxa. Em troca, ele cede à plataforma
  um volume combinado de conteúdo, por exemplo **N matérias de utilidade por mês com licença de uso em toda a rede**
  **[N a definir]**. A plataforma usa esse conteúdo no conteúdo estadual de base, nas páginas vizinhas e como inventário para o
  anúncio estadual.
- **Quando termina ("a página se pagou"):** escolher um gatilho e escrevê-lo no contrato desde o início:
  1. receita própria do parceiro ≥ **R$ X/mês** por 2 meses seguidos **[X a definir]**; ou
  2. a página cobre o próprio custo para a plataforma (infraestrutura + suporte) **[custo a calcular na E1.5]**; ou
  3. um prazo máximo (ex.: 6 meses), o que vier primeiro.
  Depois do gatilho entra a regra normal: 1º anúncio do mês e, mais tarde, os 2 primeiros.
- **O que resolve:** o problema do "mês sem venda" (Crítica, item 3) e a barreira de entrada, que é a reclamação contra a franquia.
- **Riscos [a confirmar]:**
  - A plataforma fica mais tempo sem dinheiro, o que piora a conta da E1.5. É preciso um prazo máximo.
  - O conteúdo só vale como pagamento se for reaproveitável (utilidade, serviço), não notícia que vence no dia.
  - Pode ser lido como trabalho sem remuneração ou reforçar a cara de franquia. O contrato deve tratar o conteúdo como
    **licença de uso**, com padrão mínimo de qualidade **[a confirmar com advogado, junto com a suposição 7]**.
  - O parceiro tem incentivo a adiar o gatilho (declarar menos receita). Isso reforça que a cobrança dos anúncios passe pela plataforma.
- **Para testar:** na E1.3, perguntar aos candidatos se preferem começar pagando em conteúdo ou em anúncio. Na E1.4, oferecer as
  duas opções na carta de intenção e contar quantos escolhem cada uma.

Fontes consultadas em 2026-11-02:
[UFSC, financiamento nos quase desertos de SC (Cabral e Huf, 2025)](https://ojs.labcom-ifp.ubi.pt/ec/article/download/1637/1131/5690) ·
[Atlas da Notícia, faturamento e equipes](https://congressoemfoco.com.br/noticia/7852/jornalismo-local-vive-situacao-critica-no-brasil-mostra-atlas-da-noticia) ·
[Coalizão, desinformação local (Agência Brasil, mai/2026)](https://agenciabrasil.ebc.com.br/direitos-humanos/noticia/2026-05/internet-precaria-e-falta-de-identificacao-sao-causas-de-desinformacao) ·
[SCPortais](https://acontecendoaqui.com.br/?p=70393) ·
[Adjori-SC](https://acontecendoaqui.com.br/?p=118035) ·
[Portal da Cidade, 50+ unidades](https://www.portaldofranchising.com.br/noticias/franquia-de-portais-de-conteudo-portal-da-cidade/) ·
[Portal da Cidade, home based](https://www.portaldofranchising.com.br/noticias/portal-da-cidade-tem-franqueados-em-formato-home-based/) ·
[Portal pronto (Hotmart)](https://hotmart.com/pt-br/marketplace/produtos/portal-infoco-smart/I101988798Q) ·
[Meta no Reclame Aqui](https://www.reclameaqui.com.br/empresa/meta-brasil/lista-reclamacoes/) ·
[Impulsionar no Instagram](https://herospark.com/blog/impulsionar-instagram/) ·
[Nextdoor no Trustpilot](https://ca.trustpilot.com/review/nextdoor.com) ·
[Nextdoor, análise de avaliações](https://unstar.app/pt-BR/blog/nextdoor-business-paywall-cant-comment-suspended-2026) ·
[TAPinto](https://en.wikipedia.org/wiki/TAPinto) ·
[TAPinto, custos](https://1851franchise.com/franchise-deep-dive-tapinto-franchise-costs-fees-profit-and-data-2723590) ·
[Patch (Nieman Lab)](https://niemanlab.org/encyclo/patch/?from=front) ·
[Patch (Fortune, 2012)](https://fortune.com/2012/02/15/aol-may-never-be-able-to-patch-up-patch) ·
[Axios Local e 6AM City](https://pressgazette.co.uk/news/new-model-for-local-news-axios-local-6am-city-roll-out-100-us-cities/) ·
[Village Media](https://www.editorandpublisher.com/stories/beyond-news-deserts-how-village-media-is-proving-local-journalism-can-still-grow,262431) ·
[Jornal de Pomerode (Alesc)](https://portalelegis.alesc.sc.gov.br/documentos/NYBJX) ·
[ND em Rio do Sul](https://acontecendoaqui.com.br/comunicacao/grupo-nd-inaugura-mais-uma-sucursal-no-interior-de-santa-catarina/) ·
[Rádios em Rio do Sul (Intercom, 2015)](https://portalintercom.org.br/anais/sul2015/resumos/R45-0431-2.pdf)

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
| Taxa das lojas (%) — não se aplica (web); usar taxa do meio de pagamento | | | |
| Receita mensal no mês 12 (R$) | | | |

## Resultado
- [ ] Dor confirmada em 60%+ das entrevistas
- [ ] Meta do teste de interesse atingida
- [ ] Cenário provável cobre os custos em até 12 meses

**Recomendação para o P1:** Seguir / Reformular / Arquivar
