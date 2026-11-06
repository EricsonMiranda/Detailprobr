---
name: conselho
description: Conselho de avaliação de ideias. Lê a ideia de um arquivo, lança 3 subagentes em paralelo (o que acredita, o cético e o investidor) e depois um 4º, o juiz, que dá um veredito único — CONSTRUIR, CORRIGIR ANTES ou DESISTIR. Grava tudo em conselho/<ideia>-veredito.md. Use quando o usuário digitar /conselho <arquivo> ou pedir para "passar uma ideia pelo conselho".
argument-hint: <arquivo-da-ideia.md>
---

# Conselho

Avalia uma ideia com quatro perspectivas independentes e entrega um veredito único.

## Entrada

`$ARGUMENTS` é o caminho do arquivo com a ideia (ex.: `minha-ideia.md`).

1. Se `$ARGUMENTS` estiver vazio, peça o caminho do arquivo e pare.
2. Leia o arquivo inteiro com Read. Se não existir ou estiver vazio, avise o usuário e pare — não invente a ideia.
3. Defina `<ideia>` = nome do arquivo sem diretório e sem extensão (ex.: `minha-ideia.md` → `minha-ideia`).

## Fase 1 — Três conselheiros em paralelo

Lance **os três subagentes na MESMA mensagem** (três chamadas da ferramenta Agent, `subagent_type: general-purpose`, `run_in_background: false`) para que rodem em paralelo. Cada um recebe o texto completo da ideia (cole-o no prompt; não mande só o caminho) e **não** vê a resposta dos outros.

Prompt base para cada um (troque `<PAPEL>` e `<INSTRUÇÕES DO PAPEL>`):

```
Você é <PAPEL> num conselho que avalia uma ideia. Avalie apenas a ideia abaixo, sem consultar outras opiniões.
<INSTRUÇÕES DO PAPEL>
Seja concreto e específico para ESTA ideia; nada genérico. Máximo ~400 palavras.
Responda em português, em Markdown, com as seções pedidas e termine com a linha:
"Nota (0–10): X — <uma frase>".

=== IDEIA ===
<texto completo do arquivo>
```

Papéis:

- **O que acredita** — "Você é o defensor convicto. Mostre o melhor caso realista: o problema que resolve, quem sofre com ele, por que agora, a vantagem injusta, e como seria o sucesso em 12 meses. Seções: Por que funciona · Para quem · Por que agora · Melhor cenário · Primeiro passo."
- **O cético** — "Você é o cético implacável. Procure as razões pelas quais isso falha: premissas não comprovadas, concorrentes e substitutos, riscos técnicos/legais/operacionais, por que clientes não pagariam. Seções: Premissas frágeis · Riscos principais (ordenados por gravidade) · Concorrência/substitutos · O que mataria a ideia · O que precisaria ser provado."
- **O investidor** — "Você é um investidor pragmático decidindo se coloca dinheiro e tempo nisso. Avalie mercado, modelo de receita, custo de aquisição, margem, escalabilidade, capital necessário e retorno. Seções: Tamanho de mercado · Modelo de negócio · Unit economics (estimativas explícitas) · Capital e prazo até tração · Investiria? Em que condições."

## Fase 2 — O juiz

Depois que os três retornarem, lance **um 4º subagente** (`general-purpose`) com a ideia e as três respostas na íntegra:

```
Você é o juiz de um conselho. Abaixo estão a ideia e três pareceres independentes (o que acredita, o cético, o investidor).
Pese os argumentos — não faça média das notas; dê mais peso a riscos fatais e a evidências concretas.
Dê UM único veredito, exatamente um destes: CONSTRUIR, CORRIGIR ANTES ou DESISTIR.
- CONSTRUIR: os riscos são administráveis; vale começar já.
- CORRIGIR ANTES: há potencial, mas existe(m) problema(s) que precisam ser resolvidos/validados antes de investir.
- DESISTIR: falhas fatais ou retorno que não compensa.
Responda em português, em Markdown, exatamente neste formato:

**Veredito: <CONSTRUIR | CORRIGIR ANTES | DESISTIR>**

**Por quê (3–5 frases):** ...

**Pontos decisivos:**
- ...

**Se CORRIGIR ANTES — o que corrigir (em ordem):** / **Se CONSTRUIR — primeiros 3 passos:** / **Se DESISTIR — o que aproveitar:**
1. ...

**Onde os conselheiros divergiram e quem tinha razão:** ...

=== IDEIA ===
<texto>
=== O QUE ACREDITA ===
<resposta>
=== O CÉTICO ===
<resposta>
=== O INVESTIDOR ===
<resposta>
```

Se a resposta do juiz não contiver exatamente um dos três vereditos, peça a ele (SendMessage) que corrija.

## Saída

Crie a pasta `conselho/` se não existir e grave `conselho/<ideia>-veredito.md` (sobrescreve se já existir) com:

```markdown
# Conselho — <ideia>

> Arquivo avaliado: `<caminho>` · Data: <AAAA-MM-DD>

## Veredito: <CONSTRUIR | CORRIGIR ANTES | DESISTIR>

<resposta completa do juiz>

---

## A ideia

<texto original>

## O que acredita

<resposta>

## O cético

<resposta>

## O investidor

<resposta>
```

No chat, mostre só: o veredito, o "por quê" em 1–2 frases e o caminho do arquivo gerado. Não repita os pareceres inteiros.
