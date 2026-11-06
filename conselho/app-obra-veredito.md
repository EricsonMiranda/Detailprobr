# Conselho — app-obra

> Arquivo avaliado: `app-obra.md` · Data: 2026-11-06

## Veredito: CORRIGIR ANTES

**Veredito: CORRIGIR ANTES**

**Por quê (3–5 frases):** A dor é real e os três conselheiros concordam nisso: o dono da obra paga sem saber se o orçamento é justo. Mas a ideia depende de duas coisas que ninguém provou e que podem matá-la. A primeira é que o público-alvo tenha planta em PDF utilizável, com escala e cotas. A segunda é que a extração automática chegue a uma precisão de ±15–20%. Além disso, o próprio investidor mostra que, como B2C de compra única, a conta não fecha: LTV/CAC entre 1,5 e 3x, sem recorrência. Ainda não é caso de desistir, porque os três chegam ao mesmo teste barato de validação (20–30 plantas reais comparadas com orçamentos reais). Construir antes desse teste seria gastar entre R$ 400 e 700 mil numa premissa que não foi verificada.

**Pontos decisivos:**
- **A entrada pode não existir.** Quem reforma apartamento costuma ter só a planta de vendas, humanizada e sem cotas. Quem tem projeto completo geralmente já tem arquiteto. Se isso se confirmar, o mercado endereçável encolhe muito. O cético levanta o ponto e o investidor reforça com o SAM.
- **A precisão não está provada.** Um erro acima de ±20% leva a reclamação no CDC, pedido de reembolso e perda de confiança. Neste produto, a precisão é a proposta de valor inteira.
- **A planta não define o custo.** O padrão de acabamento, a mão de obra (40–50% do total) e os problemas ocultos da reforma não aparecem no PDF. Para o produto ser honesto, o usuário precisa informar a especificação, e o escopo inicial precisa ser restrito.
- **A economia só fecha com distribuição B2B2C ou afiliação.** A taxa por projeto sozinha não paga um CAC de R$ 250–600 numa compra feita uma vez a cada 5–20 anos.
- **Há risco regulatório.** Falta confirmar que o produto não exige responsável técnico (CREA/CAU, ART/RRT). O enquadramento como "estimativa de referência" precisa ser validado juridicamente.

**Se CORRIGIR ANTES — o que corrigir (em ordem):**
1. **Medir quem tem a entrada.** Levantar com 50–100 pessoas que estão reformando ou construindo que fração tem PDF com escala e cotas. Se for pequena, redefinir a entrada: medidas digitadas, croqui ou foto com trena, em vez de depender do PDF.
2. **Medir a precisão num escopo estreito.** Reforma de apartamento com só três itens (piso, revestimento, pintura), em 20–30 obras reais. O critério de aprovação é erro ≤ ±20% em pelo menos 75% delas, comparado com orçamentos profissionais e, se possível, com o custo realizado. A especificação de acabamento deve ser coletada do usuário, não deduzida da planta.
3. **Validar a disposição de pagar de forma manual.** Receber a planta por WhatsApp e entregar o relatório em 24h, cobrando R$ 100–250, para ver se as pessoas pagam por algo que o empreiteiro faz "de graça".
4. **Testar o canal B2B2C.** Conversar com 2–3 varejistas regionais ou construtoras de reforma sobre bancar o CAC ou pagar por afiliação. É isso que faz a conta fechar.
5. **Fazer o parecer jurídico.** Confirmar que não há exigência de ART/RRT e definir o texto de isenção de responsabilidade, além de incluir no time um engenheiro de orçamento.

**Onde os conselheiros divergiram e quem tinha razão:** O otimista dá como certo que "a pessoa já tem a planta" e que modelos multimodais já leem planta bem o suficiente. Nisso o cético tem razão, e o investidor também quando estima o SAM: essa é a premissa mais frágil e precisa ser medida antes de tudo. Por outro lado, o otimista acerta ao propor o primeiro passo certo (escopo estreito, 20 plantas, venda manual), e esse passo coincide quase exatamente com o que o cético e o investidor exigem como prova. Na monetização, o investidor tem razão contra o otimista: a meta de 8–10% de conversão com taxa avulsa não sustenta o negócio, e a receita precisa vir de afiliação ou de distribuição B2B2C. A nota 3 do cético exagera a ameaça do "ChatGPT de graça". Um modelo genérico não entrega quantitativo calibrado por região, nem o acompanhamento do previsto contra o realizado. A diferenciação existe, mas só vale se a precisão for comprovada.

---

## A ideia

Um aplicativo onde você sobe as plantas em PDF de uma casa ou apartamento — para construir ou para reformar — e o app gera uma estimativa de compras, uma estimativa de prazo, uma estimativa de custo e a lista de itens que precisam ser comprados. Tudo pensado para uma pessoa comum, que não é engenheira, conseguir acompanhar a obra.

## O que acredita

### Por que funciona

Quem reforma ou constrói pela primeira vez assina um contrato sem saber se o orçamento do empreiteiro é justo, compra material três vezes porque errou a quantidade e descobre no meio da obra que "faltou o contrapiso". A dor não é técnica, é **assimetria de informação**: o mestre de obras sabe, o dono da obra paga. O app converte a planta, que a pessoa já tem porque o arquiteto entregou ou a prefeitura exigiu, num **referencial independente**: quantos m² de piso, quantos sacos de argamassa, quantos pontos elétricos, quantas semanas, quantos reais. A pessoa não precisa virar engenheira. Basta conseguir perguntar "por que seu orçamento tem 40% a mais de porcelanato do que o meu?".

O valor está no **quantitativo**, que é a parte mais chata e cara do orçamento profissional. Com áreas e perímetros extraídos da planta e composições públicas do SINAPI (Caixa), dá para chegar a uma estimativa de ±15–20%. Isso já basta para pegar sobrepreço grosseiro e planejar o fluxo de caixa.

### Para quem

- **Família classe média reformando apartamento** (R$ 60–300 mil): o público principal, que sente o medo de ser enganado no próprio bolso.
- **Autoconstrução em lote próprio**, muito comum no interior e nas periferias, com a compra de material feita aos poucos pelo próprio dono.
- **Compradores de imóvel na planta** que querem saber quanto custa personalizar antes da entrega das chaves.
- Em segundo plano, **pequenos empreiteiros e arquitetos autônomos** que hoje montam orçamento no Excel.

### Por que agora

Até 2023, ler uma planta em PDF (cotas, legendas, ambientes) exigia CAD vetorial ou trabalho manual. Modelos multimodais atuais conseguem interpretar uma planta rasterizada e extrair ambientes e medidas com qualidade suficiente para um orçamento preliminar. Ao mesmo tempo, o SINAPI é gratuito e atualizado todo mês por estado, e o custo da construção subiu bem acima da inflação depois da pandemia, então errar a compra pesa mais no bolso.

### Melhor cenário (12 meses)

- 30 mil plantas processadas, com 8–10% de conversão para um plano pago (R$ 49–149 por obra, ou assinatura durante a obra).
- O **acompanhamento** vira o motor de retenção: o usuário marca o que já comprou e o que foi executado, e compara o previsto com o realizado.
- **Vantagem injusta:** cada obra acompanhada gera dado real de custo e prazo por região e tipologia. Nem o SINAPI tem isso. Em 12 meses, esse banco calibra as estimativas melhor que a referência pública.
- A lista de compras abre receita de **afiliação com home centers** (Leroy, C&C, lojas regionais), com cotação de cada item em um clique.

### Primeiro passo

Recortar o escopo para **reforma de apartamento com planta de layout simples** e só três disciplinas: piso, revestimento e pintura. Pegar 20 plantas reais, gerar os quantitativos e comparar com orçamentos de verdade feitos por profissionais. Se o erro ficar abaixo de 20% em 15 das 20, há produto. Depois disso, vender manualmente (planta por WhatsApp, relatório em 24h) para validar a disposição de pagar antes de automatizar tudo.

Nota (0–10): 7,5 — A dor é real e o dinheiro em jogo é grande; o sucesso depende de provar que a extração da planta chega a uma precisão de orçamento aceitável.

## O cético

### Premissas frágeis
- **"A pessoa comum tem plantas em PDF utilizáveis."** Quem reforma apartamento raramente tem projeto. Tem, no máximo, a planta de vendas da incorporadora, que é humanizada, fora de escala e sem cotas. Sem projetos estrutural, elétrico e hidrossanitário, não existe quantitativo confiável.
- **"Dá para extrair quantitativos de um PDF de forma automática."** PDF de planta é vetor sem semântica, muitas vezes escaneado. Separar parede de cota, reconhecer escala, pé-direito, espessura e especificação de acabamento é um problema que nem os softwares BIM caros resolvem de forma confiável sem um modelo nativo.
- **"A planta define o custo."** Não define. Quem define o custo é a especificação (porcelanato de R$ 40 ou de R$ 400), o estado real do imóvel na reforma (o que só aparece depois da demolição), a região e a mão de obra, que pode chegar a 40–50% do total. A planta mostra a geometria, mas o padrão de acabamento não está nela.
- **"O leigo vai usar a estimativa para acompanhar a obra."** Quem acompanha uma obra precisa de medição física e de controle de pagamento ao empreiteiro. Um orçamento inicial não faz esse papel.

### Riscos principais (por gravidade)
1. **Precisão e responsabilidade.** Uma estimativa com erro de 30% induz o cliente a contratar mal ou a ficar sem dinheiro no meio da obra. O app passa a ser apontado como culpado, com risco de reclamação no CDC. Orçamento e cronograma técnicos se aproximam de atribuição profissional (CREA/CAU, ART/RRT).
2. **Reforma é a maior parte do mercado e o pior caso técnico.** Patologias ocultas, instalações antigas e regras de condomínio (NBR 16280) não aparecem em planta nenhuma.
3. **Preço desatualizado e regional.** Manter base de preços de insumos por cidade custa caro e é trabalho contínuo. O SINAPI existe, é gratuito e mesmo assim erra para o varejo pessoa física.
4. **Prazo é ficção.** Depende de equipe, chuva, entregas e do pedreiro que some. Uma estimativa de prazo gerada pelo app dá ao usuário uma confiança que os números não sustentam.
5. **Frequência de uso baixíssima.** A pessoa faz uma obra a cada 10–20 anos, o que deixa o LTV quase nulo e o CAC alto.

### Concorrência/substitutos
- O arquiteto ou engenheiro que já entrega orçamento e cronograma, e o empreiteiro que orça de graça.
- Calculadoras gratuitas de Leroy Merlin, Telhanorte e fabricantes (Quartzolit, Tigre), que pagam pela lead.
- ChatGPT/Claude com o PDF anexado, hoje, de graça.
- Apps de gestão de obra (Obra Prima, Sienge, Construct, Diário de Obra) e o regra-de-bolso de custo por m² (CUB).

### O que mataria a ideia
- Erro médio acima de ±20% contra o custo real de obras concluídas.
- A maioria dos usuários-alvo não ter PDF com escala e cotas.
- Um varejista de material de construção lançar a mesma ferramenta de graça, como isca de venda.

### O que precisaria ser provado
- Precisão, medida em 20 ou mais obras reais já concluídas e auditadas, separando construção de reforma.
- Uma fatia mensurável de leigos que têm planta utilizável e pagariam R$ 100 ou mais por um relatório que um empreiteiro faz de graça.
- Um modelo de receita viável (B2C avulso, afiliação com varejo, venda para arquitetos) que não dependa de uso recorrente.
- Validação jurídica de que o produto não exige responsável técnico.

Nota (0–10): 3 — O problema é real, mas a entrada é ruim, a precisão não está provada e o substituto gratuito está a um clique.

## O investidor

### Tamanho de mercado
O mercado é grande, mas o comprador é difícil de alcançar. A construção e reforma residencial no Brasil movimenta centenas de bilhões de reais por ano. Grande parte é autoconstrução ou reforma tocada pelo próprio dono (estimo mais de 50% das obras residenciais). Por isso o mercado endereçável real é bem menor:
- **SAM:** pessoas que têm planta em PDF. Na reforma, a maioria não tem planta nenhuma, e quem tem planta costuma já ter arquiteto ou engenheiro. Estimo de 300 a 600 mil obras por ano com PDF utilizável e dono leigo envolvido.
- **SOM realista em 5 anos:** de 15 a 30 mil projetos pagos por ano.

### Modelo de negócio
- **Taxa por projeto:** de R$ 149 a R$ 399 pela estimativa completa, mais acompanhamento da obra.
- **Receita principal possível: afiliação ou marketplace de materiais.** Uma obra de R$ 80 a 300 mil gasta de 40% a 50% em material. Com comissão de 2% a 4%, isso dá de R$ 600 a R$ 6.000 por obra convertida.
- **Venda de leads** para empreiteiros, arquitetos e financiamento (home equity, crédito para material).

### Unit economics (estimativas)
- **CAC pago (Meta/Google, nicho "reforma"):** de R$ 60 a 150 por cadastro e de R$ 250 a 600 por cliente pagante (conversão de 15% a 25%).
- **Receita por cliente:**
  - Taxa: R$ 250
  - Afiliação: 30% compram pelo app × R$ 2.000 = R$ 600
  - Total: cerca de R$ 850
- **Margem bruta:** de 60% a 75%. O custo de IA e processamento é baixo (menos de R$ 20 por projeto). O que pesa é a revisão humana, que vai ser necessária no começo para a precisão não destruir a confiança.
- **LTV/CAC:** de 1,5 a 3x. Não há recorrência: a pessoa reforma uma vez a cada 5 a 10 anos. O LTV é praticamente igual à primeira transação.
- **Risco técnico central:** ler planta em PDF (vetorial, escaneada, sem cotas) e tirar dela quantitativos confiáveis. Errar 20% no custo vira reclamação e pedido de reembolso.

### Capital e prazo até tração
- **MVP** com arquitetônico simples (apartamento padrão, reforma de banheiro e cozinha) e revisão humana: de R$ 400 a 700 mil, de 6 a 9 meses.
- **Seed** para provar a monetização por afiliação e um CAC sustentável: de R$ 3 a 5 milhões, mais 18 meses.
- **Tração mínima convincente:** 1.000 obras pagas por mês e mais de 25% de compra de material via app.

### Investiria? Em que condições
Como app B2C puro, com receita só da taxa, não investiria. A compra é única, o CAC é alto e a precisão é difícil de garantir. Investiria um cheque pré-seed se:
1. Houver parceria de distribuição com um varejista de material de construção ou uma construtora de reformas que banque o CAC. O app vira a ferramenta de venda deles (B2B2C).
2. O foco inicial for estreito: reforma de apartamento padrão em uma capital, com uma base de preços local (SINAPI ajustado mais preços do varejista).
3. Houver prova de precisão de ±15% em 30 obras reais antes de escalar.
4. O time tiver um engenheiro de orçamento como cofundador, além de tecnologia.

Nota (0–10): 4 — O mercado é real e a dor é clara, mas sem distribuição via varejo e sem precisão comprovada, a economia de uma compra única não fecha.
