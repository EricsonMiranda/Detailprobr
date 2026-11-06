# Conselho — orcamento-empreiteiro

> Arquivo avaliado: `orcamento-empreiteiro.md` · Data: 2026-11-06

## Veredito: CORRIGIR ANTES

**Veredito: CORRIGIR ANTES**

**Por quê (3–5 frases):** Os três conselheiros concordam que a dor existe e é concreta: cobrar é constrangedor, o cliente some sem sinal e o orçamento solto no WhatsApp parece amador. O cético, porém, mostra riscos que podem matar a ideia e que ninguém respondeu com evidência. São eles: retenção e disposição de pagar num público de renda irregular, com substitutos gratuitos (caderno + WhatsApp + Pix do banco + Canva); erro de preço que destrói a confiança no primeiro uso; e dependência da API do WhatsApp para a função que mais segura a assinatura. O próprio investidor admite que a assinatura sozinha não paga o investimento: o LTV/CAC de 2,5–3,5 só fica confortável com receita de lojas e de pagamentos, que hoje é só hipótese. Há potencial, mas a tese de receita está de pé sobre suposições, e a métrica de validação proposta por quem acredita ("emitir 4 orçamentos/mês") mede uso de graça, não pagamento.

**Pontos decisivos:**
- **Pagamento e retenção reais não foram provados.** Churn estimado em 7–10% ao mês contra o limite de 6% que o próprio investidor exige. Esse é o risco nº 1 do cético e os outros dois não o desmontaram.
- **O orçamento automático é ao mesmo tempo o ponto de venda e o ponto de ruptura.** Os três citam o erro de preço como risco central. A solução precisa ser estimativa editável, que aprende os preços do profissional, e não "orçamento correto em 2 minutos".
- **O valor de verdade (lojas e pagamentos) não tem evidência.** Nenhuma loja pagando, e a loja já recebe o pedido de graça pelo WhatsApp do pedreiro. Grandes redes podem dar o mesmo de graça.
- **O WhatsApp é dependência crítica.** Custo por conversa, templates aprovados pela Meta e risco de bloqueio do número por denúncia de mensagem de cobrança atingem justamente a função de maior retenção.
- **O escopo está largo demais.** São seis funcionalidades. O MVP proposto (só pintores, uma cidade) já corta parte delas, e esse foco é correto.

**Se CORRIGIR ANTES — o que corrigir (em ordem):**
1. **Trocar a métrica de validação por dinheiro real.** Piloto com cobrança desde o primeiro mês, com meta de pelo menos 100 pagantes por mais de 3 meses e churn abaixo de 6% ao mês após o terceiro mês. Antes do código, dá para testar com um MVP "concierge" (orçamento PDF + Pix + lembrete feitos semi-manualmente) com 30–50 pintores.
2. **Medir a precisão e o efeito do orçamento.** Comparar o preço gerado com o preço que o pintor fecha de fato (meta: dentro de ±15%). Tornar a estimativa editável desde o início e medir se o PDF aumenta a taxa de aceite em relação ao orçamento feito à mão.
3. **Validar o canal de cobrança antes de depender dele.** Calcular o custo real por conversa na API oficial, aprovar os templates de cobrança na Meta e testar a taxa de denúncia e de bloqueio. Medir se os lembretes reduzem a inadimplência de forma mensurável.
4. **Conseguir uma loja pagando de fato**, por lead ou por comissão, sem ficar só em carta de intenção, e medir a conversão. Sem isso, o negócio é um SaaS de R$ 12 milhões por ano de teto, e o investidor já disse que não segue.
5. **Testar a tese de pagamentos e a objeção fiscal.** Ver se mais de 30% das etapas passam pelo Pix do app e se o medo de deixar rastro de renda (teto do MEI) trava a adoção. Definir o PSP/BaaS e o tratamento de MED e fraude antes de mexer com o dinheiro de terceiros.

**Onde os conselheiros divergiram e quem tinha razão:** Quem acredita aposta que o lembrete automático segura a assinatura e que a loja vai até subsidiar o profissional. O cético diz que o público paga pouco, larga rápido e já resolve quase tudo de graça. Sobre retenção e disposição de pagar, o cético tem mais razão. As metas de quem acredita (2.500 pagantes, R$ 100 mil por mês em 12 meses) não têm evidência, e a validação que ele propõe não mede pagamento. Sobre a lista de compras, quem acredita e o investidor têm razão em que ali está o ativo de maior valor, mas o cético acerta que hoje ela é genérica e que a loja já recebe o pedido de graça. O investidor faz a melhor síntese: a assinatura não sustenta o negócio, e é preciso provar a receita de lojas e pagamentos com marcos objetivos. Os critérios dele, junto com os critérios de morte do cético, são o melhor roteiro para decidir depois do piloto entre CONSTRUIR e DESISTIR.

---

## A ideia

App para o profissional autônomo da construção (pedreiro, pintor, eletricista, encanador, pequeno empreiteiro). Ele mede o cômodo e digita as medidas ou manda um áudio, escolhe o padrão de acabamento, e em 2 minutos o app gera:
- orçamento bonito em PDF, com o nome dele, para mandar ao cliente;
- lista de material;
- prazo estimado;
- link de pagamento por Pix, com sinal.

Durante a obra, o app manda ao cliente fotos do andamento e cobra cada etapa.

Também inclui:
- **Controle financeiro básico:** quanto entrou, quanto saiu (material, ajudante), quanto tem a receber e o lucro de cada obra.
- **Lembretes de cobrança automáticos:** pelo WhatsApp, avisando o cliente antes e depois do vencimento de cada etapa, para o profissional não ter o constrangimento de cobrar.

Modelo de receita: assinatura de R$ 29 a 49 por mês para o profissional, mais comissão ou leads com lojas de material, que recebem a lista de compras pronta.

## O que acredita

### Por que funciona

O autônomo da construção perde dinheiro em três lugares, e o app fecha os três num fluxo só.
1. **Orçamento.** Hoje ele faz a conta de cabeça, manda o preço por WhatsApp numa mensagem solta e parece amador perto do concorrente que mandou um PDF. Um orçamento com nome, logo, lista de material e prazo eleva a taxa de fechamento e justifica cobrar mais.
2. **Sinal.** Sem sinal, o cliente some depois que o material foi comprado. O link Pix com sinal já no orçamento transforma o "vou pensar" em compromisso.
3. **Cobrança.** O pedreiro não cobra porque tem vergonha e medo de perder indicação. Quando o lembrete automático parte do "sistema", o constrangimento sai das costas dele. É a função que ele mais vai valorizar, e a que mais segura a assinatura.

O financeiro por obra resolve uma dor que ele nem percebe: muitos não sabem se a última obra deu lucro depois de pagar o ajudante e voltar três vezes à loja.

### Para quem

Começar pelo **pintor e pelo pequeno empreiteiro de reforma**. São orçamentos por m², com padrão repetível, fáceis de automatizar com precisão. Têm ticket de R$ 3 mil a R$ 30 mil, de 3 a 8 obras por mês, e já usam WhatsApp e Pix o dia inteiro. O eletricista e o encanador vêm depois, porque orçar por ponto é mais difícil de padronizar.

### Por que agora

- O Pix com cobrança e link é universal, inclusive no Pix Automático.
- A transcrição de áudio por IA ficou boa e barata, e esse público prefere falar a digitar.
- A API oficial do WhatsApp Business ficou mais acessível.
- O MEI virou norma, e o profissional quer parecer empresa.

Há cinco anos, essa combinação seria cara e travada.

### Melhor cenário

A vantagem injusta é o **lado da loja de material**. Cada orçamento gera uma lista de compras com CEP, prazo e intenção de compra. Para o home center ou o depósito do bairro, isso é o lead mais quente que existe, e vale muito mais que R$ 29. Com escala, a loja chega a subsidiar a assinatura.

Em 12 meses, num cenário realista:
- 8 mil profissionais ativos em 2 ou 3 capitais, com 2.500 pagantes, perto de R$ 100 mil de receita recorrente por mês;
- R$ 15 a 20 milhões por mês em orçamentos emitidos;
- parceria com 30 a 50 depósitos regionais pagando por lista entregue;
- crescimento orgânico, porque cada PDF enviado ao cliente leva a marca do app e é visto por quem também conhece outros pintores.

### Primeiro passo

Montar um MVP só para pintores em uma cidade, com áudio, orçamento em PDF, Pix com sinal e lembrete de cobrança. O financeiro e as lojas ficam para depois. A ideia é recrutar 50 pintores em grupos de WhatsApp e lojas de tinta e medir duas coisas em 60 dias: quantos orçamentos cada um emite e quantos sinais são pagos pelo link. Se mais de 40% emitirem 4 ou mais orçamentos por mês, a tese está validada.

Nota (0–10): 8 — Resolve uma dor de dinheiro diária e constrangedora, e o lado das lojas de material dá um caminho de monetização que vai além da assinatura.

## O cético

### Premissas frágeis
- **"Em 2 minutos sai um orçamento correto."** O preço de obra pequena depende do que não dá para medir com trena: parede fora de prumo, reboco podre, fiação antiga, retrabalho, acesso, região e o próprio cliente. Se o app errar para baixo, o profissional perde dinheiro e larga o app. Se errar para cima, perde a obra. A confiança morre no primeiro erro.
- **"O autônomo quer formalizar."** Boa parte trabalha de boca, com preço "de cabeça", e cobra informalmente justamente para fugir de rastro fiscal. Pix com sinal e controle financeiro criam histórico de renda (Receita, MEI estourando o teto) que muitos querem evitar.
- **"Ele vai alimentar o app durante a obra."** Fotos por etapa e lançamento de gastos exigem disciplina diária de quem está com a mão suja de massa. O padrão desse público é usar e largar.
- **"A loja paga pela lista."** A lista sai genérica, sem marca e sem quantidade confiável. A loja já recebe o pedido de graça pelo WhatsApp do próprio pedreiro.

### Riscos principais (do mais grave ao menos grave)
1. **Retenção e disposição de pagar.** R$ 29–49/mês para quem fecha de 2 a 4 obras por mês e tem renda irregular. O churn deve ser altíssimo nos meses fracos.
2. **WhatsApp.** Cobrança automática exige a API oficial, com custo por conversa e templates aprovados pela Meta. Mensagens de cobrança denunciadas derrubam o número. A ideia depende de uma plataforma que você não controla.
3. **Responsabilidade.** O cliente contesta o orçamento ou o prazo ("o app disse 10 dias"). Pix com sinal envolvendo terceiro traz exigências de PSP/BaaS, chargeback via MED e fraude. Sem ART, o eletricista que usar o app para "padrão de acabamento" pode virar alvo.
4. **Base de preços.** Manter custos regionais de material e mão de obra atualizados (SINAPI é defasado e voltado a obra pública) é caro e contínuo.
5. **CAC.** Esse público se alcança em loja física e no boca a boca, e não converte bem em mídia paga.

### Concorrência/substitutos
- O substituto real: **caderno + WhatsApp + Pix do banco + modelo no Canva/Word**. Custa zero e já funciona.
- Apps de orçamento já existentes: Orçamento Fácil, Meu Orçamento, Obra Prima, além de Gestor de Obras e Diário de Obra para empreiteiros.
- Bancos e maquininhas (InfinitePay, PagBank, Mercado Pago) já oferecem link de Pix e cobrança recorrente de graça.
- Leroy Merlin, Telha Norte e as casas de material locais têm apps e programas de fidelidade para profissionais, com cashback. Elas podem oferecer o orçamento grátis para capturar o pedido.
- GetNinjas e Habitissimo disputam a relação com o cliente final.

### O que mataria a ideia
- Retenção abaixo de 30% no terceiro mês.
- Uma loja grande lançando o mesmo app de graça.
- Bloqueio de números ou custo por conversa no WhatsApp que torne os lembretes inviáveis.
- Orçamentos sistematicamente fora de ±15% do preço que o profissional fecha de verdade.

### O que precisaria ser provado
- Que pelo menos 100 profissionais pagam por mais de 3 meses, em pagamento real e não por intenção declarada.
- Que o orçamento gerado fecha mais obras do que o feito à mão (taxa de aceite).
- Que os lembretes reduzem a inadimplência de forma mensurável.
- Que alguma loja paga por lead ou comissão e com que conversão.
- Qual é a única funcionalidade indispensável. Hoje são seis, e isso cheira a produto sem foco.

Nota (0–10): 4 — A dor de cobrar é real, mas o público paga pouco, larga rápido e já resolve quase tudo com WhatsApp e Pix de graça.

## O investidor

### Tamanho de mercado
O Brasil tem cerca de 7 milhões de ocupados na construção. Desses, uns 4 milhões trabalham por conta própria ou na informalidade. Quem tem perfil de pagar é bem menos gente: o profissional com smartphone, que fecha várias obras de reforma por mês e já manda orçamento pelo WhatsApp. Estimo entre 600 mil e 1 milhão. Com 3% desse grupo pagando R$ 39 (uns 25 mil assinantes), a assinatura dá cerca de R$ 12 milhões por ano de receita recorrente. É um bom negócio, mas não um negócio grande. O dinheiro maior está na outra ponta: cada obra de reforma pequena gira de R$ 5 mil a 20 mil, e de 40% a 50% disso é material.

### Modelo de negócio
- **Assinatura:** paga os custos, mas sozinha não paga o investimento.
- **Lista de material indo para a loja:** é o ativo de verdade, porque é intenção de compra qualificada, com quantidade e endereço. Uma comissão de 2% a 3% sobre R$ 3 mil a 6 mil de material dá R$ 60 a 180 por obra, mais que um mês de assinatura.
- **Pagamentos (o que está escondido na ideia):** o sinal e as etapas passam pelo app. Isso abre espaço para cobrar uma taxa pequena, antecipar recebíveis e oferecer crédito para material. É aqui que o negócio pode virar uma fintech vertical, em vez de um SaaS barato.

### Unit economics (estimativas)
- **Preço médio:** R$ 39 por mês.
- **Margem bruta:** cerca de 80%. A API do WhatsApp custa uns R$ 0,05 por mensagem de utilidade, com 60 a 100 mensagens por profissional por mês. Somando transcrição de áudio, IA e PDF, o custo fica em R$ 6 a 8 por usuário.
- **Custo de aquisição (CAC):** R$ 100 a 150 com anúncio pago no Meta e no YouTube e influenciadores de obra. Pode cair para menos de R$ 50 se o laço viral funcionar: todo PDF e todo link de cobrança chegam ao cliente final com a marca do app, e o cliente de hoje indica outros profissionais.
- **Cancelamento:** alto, de 7% a 10% ao mês, por causa da sazonalidade, da renda instável e do pagamento por cartão que falha.
- **Valor por cliente (LTV), só com assinatura:** cerca de R$ 31 de margem ÷ 0,085 ≈ R$ 365, o que dá LTV/CAC de 2,5 a 3,5. Com a receita das lojas e dos pagamentos (R$ 15 a 30 por mês a mais), o LTV vai para R$ 600 a 900 e a conta passa a ficar confortável.

### Capital e prazo até tração
- **Rodada seed:** R$ 2 a 3 milhões para 18 meses.
- **Meses 0 a 6:** produto com tabela de preços regional baseada no SINAPI e ajustável pelo próprio profissional, piloto em uma ou duas capitais e uma loja ou rede regional parceira.
- **Meta de 18 meses:** de 5 a 8 mil pagantes e de R$ 1 a 2 milhões por mês de material repassado às lojas.

**Risco central:** se o orçamento automático errar o preço, o profissional perde dinheiro uma vez e abandona o app. A estimativa tem que ser editável e "aprender" com os preços dele.

**Risco secundário:** as grandes redes de material de construção podem fazer algo parecido de graça para capturar o pedreiro.

### Investiria? Em que condições
Sim, com cheque pequeno e ligado a marcos, condicionado a quatro coisas:
1. Piloto com 200 profissionais em que pelo menos 40% ainda fazem 3 ou mais orçamentos por mês no segundo mês.
2. Cancelamento abaixo de 6% ao mês nos pagantes depois do terceiro mês.
3. Pelo menos uma loja ou rede pagando de fato por lista ou venda, não só uma carta de intenção.
4. Mais de 30% das etapas recebidas pelo Pix do app, o que prova a tese de pagamentos.

Se a assinatura for a única receita depois de 12 meses, eu não acompanharia a rodada seguinte.

Nota (0–10): 6 — dor real e um laço viral embutido, mas o negócio só passa a valer o investimento se a receita das lojas e dos pagamentos se provar; a assinatura sozinha não sustenta.
