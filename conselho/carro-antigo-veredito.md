# Conselho — carro-antigo

> Arquivo avaliado: `carro-antigo.md` · Data: 2026-11-06

## Veredito: CORRIGIR ANTES

**Veredito: CORRIGIR ANTES**

**Por quê (3–5 frases):** A dor de dinheiro e agenda entre sócios de um mesmo carro existe, e os três conselheiros concordam nela, mas ninguém trouxe evidência concreta de que esses grupos existem em número suficiente nem de que pagariam para trocar Splitwise, Google Agenda e WhatsApp, que são gratuitos. O mercado estimado (5 mil a 15 mil garagens compartilhadas, R$ 3 a 5 milhões por ano no teto) não é fatal para um negócio bancado pelo próprio fundador, mas não deixa margem para errar: um CAC alto ou um cancelamento acima de 4% ao mês derrubam a conta. O rastreador próprio é o único risco que poderia matar a empresa (hardware, chip M2M, bateria, purista que rejeita mexer na elétrica), mas dá para eliminá-lo cortando o rastreador ou trocando por integração. Por isso há potencial, mas a disposição de pagar e o tamanho real do nicho precisam ser validados antes de investir R$ 100 a 150 mil em código.

**Pontos decisivos:**
- Os substitutos gratuitos são o risco mais concreto. O Splitwise e o Tricount já fazem rateio por percentual, então o diferencial precisa ser a combinação de reserva, rateio e dossiê do carro, e essa combinação ainda não foi provada.
- O tamanho do mercado limita o negócio, mas não o mata. Ele inviabiliza venture capital e impõe um modelo enxuto, de baixo custo, bancado pelo próprio fundador.
- Hardware próprio é a falha fatal que dá para evitar. Os três convergem em deixar o rastreador fora do MVP e não fabricar.
- Todos os números (CAC de R$ 40 a 80, churn de 3% a 4%, LTV/CAC de 6 a 10 vezes, 3.000 garagens) são suposições. Nenhum parecer traz uma entrevista ou um dado real.
- A receita lateral (seguradora de coleção, laudo de placa preta, relatório de procedência) provavelmente vale mais que a assinatura, e também não foi validada.

**Se CORRIGIR ANTES — o que corrigir (em ordem):**
1. Validar a dor e o nicho: entrevistar 20 a 30 grupos reais de sócios, via clubes, encontros e grupos de Facebook de modelos específicos. Medir quantos existem e testar sozinha a hipótese "quem deve a quem", contra a forma como eles se viram hoje com Splitwise, planilha e WhatsApp.
2. Provar a disposição de pagar antes de programar: conseguir garagens compartilhadas que pré-paguem, ou um compromisso firme, por cerca de R$ 19 por mês. A meta do investidor é 100. Se não passar de algumas dezenas, reavaliar.
3. Cortar o rastreador próprio da proposta. No máximo, integrar com AirTag e SmartTag ou revender aparelho de terceiros depois. Tratar a LGPD (consentimento de todos os sócios para a localização) antes de qualquer localizador.
4. Abrir conversa com uma seguradora de carro de coleção ou com um clube grande para testar o canal barato de aquisição e a receita lateral.
5. Só então construir o MVP enxuto (garagem compartilhada, percentuais, reserva, despesa com foto do recibo, saldo), com termos de uso que deixem claro que o app não resolve responsabilidade jurídica por multa, sinistro ou registro no DETRAN. Manter no radar a expansão para outros bens divididos entre sócios (barco, avião, casa de praia).

**Onde os conselheiros divergiram e quem tinha razão:**
- **Tamanho e crescimento.** O que acredita projeta 3.000 garagens com crescimento viral pelo convite entre sócios. O cético e o investidor estimam um universo de poucos milhares a 15 mil garagens compartilhadas. Os dois têm mais razão: o convite viral só funciona dentro das garagens compartilhadas, que são o nicho do nicho. Dos 30% compartilhados de 3.000, sobram cerca de 900 garagens, e a viralidade não escala além disso.
- **Força da dor.** O cético diz que o entusiasta gasta com prazer e não quer "gestão". Isso vale para o colecionador solo, mas não para os sócios, em que dinheiro e agenda geram briga de verdade. Nesse ponto o que acredita tem razão, e por isso o foco deve ser o carro com vários donos, não o solo.
- **Economia.** O investidor vê LTV/CAC saudável. O cético teme que o CAC supere o LTV. Ninguém tem dados, então a divergência só se resolve com a validação do item 2.
- **Rastreador.** O que acredita o trata como um upsell futuro. O cético o vê como risco capaz de afundar a empresa. O cético está mais certo sobre o hardware próprio. O investidor dá a saída sensata: integrar ou revender, nunca fabricar.
- **Nota.** A nota 7 do que acredita está otimista. As notas 3 e 4 refletem melhor a falta de evidência, mas o problema tem conserto, e nenhuma delas justifica desistir.

---

## A ideia

Um aplicativo para quem tem carro antigo. Ele acompanha os custos, onde o carro está e as fotos do carro.

Também serve para quem tem carro antigo dividido com outras pessoas — por exemplo, um carro com 3 donos. Cada dono usa o app e tem o seu percentual de participação. Há uma "garagem" com os carros. Os donos podem reservar o carro para sair no dia X, lançar todas as despesas e controlar quem pagou o quê, para ver quem está devendo a quem. A ideia é incluir também um localizador (rastreador) do carro.

## O que acredita

### Por que funciona

O carro antigo dividido entre sócios é um condomínio informal que hoje roda em grupo de WhatsApp com planilha. É aí que a coisa trava: "quem pagou a capota?", "você ia usar no sábado do encontro?", "a parte do Zé na restauração do motor foi 40% ou 33%?". Briga por dinheiro e por agenda é o que acaba com essas sociedades, e muitas vezes também com a amizade. O app junta tudo isso em três funções que ninguém oferece juntas: **reserva com calendário**, **rateio por percentual de participação** (não divisão igual) e um **saldo de quem deve a quem**, no estilo Splitwise, só que pensado para um bem. As fotos e o histórico de custos viram um **dossiê de procedência**, e procedência documentada faz o carro valer mais na venda e ajuda a tirar placa preta.

### Para quem

- **Grupos de 2 a 5 sócios** em um Fusca 1972, um Opala, um Maverick, um MP Lafer. Costumam ser amigos, irmãos ou herdeiros que receberam o carro do pai juntos (esse caso, herança dividida, é bem comum).
- **Colecionador solo** com 2 a 6 carros, que quer saber quanto já gastou em cada um e onde cada carro está: oficina de funilaria, garagem de terceiros, evento.
- Num segundo momento, **clubes de antigomobilismo** com carros do clube.

### Por que agora

O antigomobilismo no Brasil está aquecido: os encontros vivem cheios, a placa preta é valorizada e carros dos anos 80 e 90 (Gol GTI, Escort XR3, Kadett GSi) estão virando "antigos" para uma geração mais nova, acostumada a app, Pix e divisão de conta pelo celular. Rastreadores com chip e GPS baratos (alguns na faixa de R$ 100 a 200, com mensalidade baixa) tornam o localizador viável. E carro antigo é alvo de furto e quase nunca tem rastreador de fábrica.

### Melhor cenário (12 meses)

- 3.000 garagens ativas, com uns 30% sendo garagens compartilhadas. Esse é o núcleo viral: cada sócio convida os outros, então cada garagem traz em média 2,5 usuários sem custo de aquisição.
- Plano pago de R$ 19,90 por mês por garagem compartilhada, mais rastreador próprio em parceria com um fabricante nacional (receita de hardware e mensalidade).
- Parcerias com 20 clubes e 2 encontros grandes, além de seguradoras especializadas em carro de coleção, que ganham com o histórico documentado.
- A vantagem injusta: o **dado de custo real de manutenção por modelo** ("um Opala 6cc custa R$ X por ano para manter"), que ninguém tem e que vale ouro para comprador, seguradora e avaliador.

### Primeiro passo

Lançar um MVP **sem rastreador**: garagem compartilhada, percentuais, reserva por calendário, lançamento de despesas com foto do recibo e saldo entre sócios. Recrutar 30 grupos reais em 2 ou 3 clubes locais e em grupos de Facebook de modelos específicos. Validar se eles abandonam o WhatsApp e a planilha em 60 dias. O rastreador entra depois, como upsell.

Nota (0–10): 7 — Nicho apaixonado com uma dor real (dinheiro e agenda entre sócios), crescimento embutido pelo convite entre donos e um dado proprietário valioso, mas o mercado é pequeno e precisa ser provado com grupos reais antes do hardware.

## O cético

### Premissas frágeis
- **Que existam muitos carros antigos com vários donos formais.** Cotas de 3 donos existem, mas são raras e informais (amigos, irmãos, herança). É um nicho dentro de um nicho, e quem está nele costuma resolver tudo num grupo de WhatsApp.
- **Que o dono de carro antigo quer "gestão".** Quem tem carro antigo é colecionador e entusiasta. Gasta com prazer e quase não controla custo. A motivação é emocional, não financeira, então a dor que o app resolve é fraca.
- **Que o carro antigo aceita bem um rastreador.** Carro de coleção fica parado semanas na garagem. Um rastreador ligado direto drena a bateria. Instalar exige mexer na elétrica original, o que o purista rejeita porque desvaloriza o carro.

### Riscos principais (do mais grave ao menos grave)
1. **Produto sem foco: são três apps num só.** Controle de custos, divisão de despesas e rastreador são produtos diferentes, com custos e concorrentes diferentes. O rastreador traz hardware, chip M2M, logística, suporte e estoque, e isso pode afundar uma startup de software.
2. **Tamanho do mercado.** Placas pretas e carros com mais de 30 anos somam algumas centenas de milhares no Brasil. Os que têm mais de um dono e pagariam assinatura talvez sejam alguns milhares. Isso não vira negócio, vira hobby.
3. **Conflito jurídico entre os donos.** Com saldo devedor entre sócios, o app vira prova num litígio. Surgem perguntas difíceis: quem é responsável pela multa ou pelo sinistro do dia reservado? O carro está registrado em nome de um só no DETRAN, e o app não resolve isso. O risco de suporte e de responsabilidade é desproporcional à receita.
4. **LGPD e localização.** Rastrear um bem compartilhado expõe onde cada sócio esteve. É dado sensível e exige consentimento de todos, com risco de uso abusivo.
5. **Retenção.** O carro sai poucas vezes por mês e as despesas são esporádicas. Com uso tão baixo, o usuário cancela.

### Concorrência e substitutos
- **Divisão de despesas:** Splitwise e Tricount, gratuitos e já com percentuais por pessoa. Planilha Google compartilhada.
- **Reserva:** Google Agenda compartilhada, grupo de WhatsApp.
- **Rastreador:** Tag da Apple e Galaxy SmartTag por cerca de R$ 200, sem mensalidade. Rastreadores de seguradora e de empresas como Pósitron e Ituran.
- **Custos e histórico do carro:** Drivvo, Fuelio e apps de clube. Para histórico e fotos, Instagram e Google Fotos.

### O que mataria a ideia
- Se descobrirmos que donos em grupo usam Splitwise mais AirTag e ficam satisfeitos.
- Se o custo de aquisição de um usuário passar do valor que ele paga ao longo do tempo (LTV) num mercado de poucos milhares.
- Se o rastreador exigir hardware próprio.

### O que precisaria ser provado
- Quantos carros antigos têm mais de um dono de fato. Começar por entrevistas com 20 grupos reais, via clubes e encontros.
- Que esses grupos pagariam, e quanto (por exemplo R$ 20 por mês por carro), em vez de usar ferramentas gratuitas.
- Que existe um canal barato para chegar a eles: clubes, FBVA, seguradoras de antigos (Porto Clássicos), oficinas de restauro.
- Que o rastreador funciona sem desvalorizar o carro e sem descarregar a bateria, ou então cortá-lo da proposta.
- Qual problema dói de verdade. A hipótese é "quem deve a quem", e ela precisa ser testada sozinha antes de qualquer outra função.

Nota (0–10): 3 — Nicho minúsculo com substitutos gratuitos melhores para cada função, e um rastreador que acrescenta custo e risco sem criar diferencial.

## O investidor

### Tamanho de mercado
- **Carro antigo no Brasil:** a frota com mais de 30 anos passa de alguns milhões, mas quem gasta dinheiro com o carro como hobby é bem menos gente. Estimo de 50 mil a 150 mil entusiastas ativos, somando carros de placa preta, sócios de clubes (Veteran Car, clubes de Fusca, Opala e Puma) e frequentadores de encontros.
- **Carro com vários donos:** é um nicho dentro do nicho. Chuto de 5% a 10% desses carros, ou seja, de 5 mil a 15 mil "garagens" com mais de um dono.
- **Receita máxima realista:** de R$ 3 a 5 milhões por ano no Brasil, mesmo dominando o segmento. Isso não comporta venture capital. A saída seria ir para fora (EUA e Europa) ou ampliar para outros bens de hobby divididos entre sócios, como barcos, aviões experimentais e motos.

### Modelo de negócio
- **Assinatura por garagem, e não por usuário:** cerca de R$ 19 por mês para a garagem compartilhada (reserva, rateio, "quem deve a quem"). O registro pessoal de custos e fotos fica grátis e serve para atrair usuários.
- **Rastreador:** revenda de aparelho de terceiros (R$ 250) com mensalidade de R$ 25, ou integração com AirTag e similares. Fabricar hardware próprio não faz sentido.
- **Receita lateral, que é onde está o valor real:** indicação de seguro para carro de coleção (comissão de 10% a 20%), oficinas especializadas, peças e laudos para placa preta. O histórico de custos e manutenção também valoriza o carro na revenda, e isso pode render um relatório pago na hora de vender.

### Unit economics (estimativas)
- **Receita por garagem:** R$ 19 × 12 = R$ 228 por ano. Com rastreador em 30% delas, sobe para cerca de R$ 320 por ano.
- **Margem bruta:** cerca de 85% no software e 40% no rastreador.
- **Cancelamento:** de 3% a 4% ao mês. O uso é esporádico, o carro sai no fim de semana e às vezes fica meses parado. Com isso, cada garagem fica em média de 25 a 30 meses e gera de R$ 450 a 550 de margem no total.
- **Custo de aquisição:** de R$ 40 a 80 por garagem via clubes, encontros e grupos de WhatsApp. É baixo porque a comunidade é fechada e muito conectada. A relação margem total ÷ custo de aquisição fica entre 6 e 10 vezes, o que é saudável.
- **Gargalo:** o volume, não a margem.

### Capital e prazo até tração
- **Produto mínimo** (garagem, rateio de despesas, reservas, fotos, integração com rastreador já existente): de R$ 100 a 150 mil e de 4 a 6 meses.
- **Validação:** de 6 a 9 meses depois do lançamento. Meta de 500 garagens pagantes e 3 clubes parceiros.
- **Para escalar** com seguro e marketplace: de R$ 1 a 2 milhões, só depois de validar.

### Investiria? Em que condições
Não como aposta de venture capital neste formato. Colocaria um cheque pequeno (até R$ 150 mil) ou toparia como negócio bancado pelo próprio fundador, se estas condições forem cumpridas:
1. Antes de programar, provar disposição de pagar: 100 garagens com vários donos pré-pagando.
2. Fechar parceria com pelo menos uma seguradora de carro de coleção. É ela que paga a conta, não a assinatura.
3. Nada de hardware próprio.
4. Ter um plano para ampliar o rateio a outros bens de hobby (barco, avião, casa de praia) num prazo de 18 meses. É isso que transforma um app de nicho em plataforma.

Nota (0–10): 4 — A dor é real e bem resolvida, mas o mercado é pequeno demais para justificar capital, a menos que a ideia vire uma plataforma para qualquer bem de hobby dividido entre sócios, com receita de seguro.
