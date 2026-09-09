# 🎉 Kit Festa

App de **renda extra com kits de festa** (doces + salgados). A usuária escolhe entre 10 kits prontos
— ou cria os dela —, vê a **receita**, a **foto**, o **preço sugerido**, o **custo** e **quanto lucra**
em cada kit. Tem calculadora de custos, catálogo com foto e uma tela de meta.

Produto digital de ticket baixo (R$29,90), vendido para mulheres que querem ganhar dinheiro em casa.

---

## Como rodar (local)

É um **arquivo único, sem build e sem dependências**. Basta abrir:

```
index.html   →   dois cliques (abre em qualquer navegador)
```

Não precisa de Node, npm, servidor nem instalação. Funciona offline.

## Como publicar

**Vercel (recomendado)** — conecte este repositório no [vercel.com](https://vercel.com):
- Framework preset: **Other** (é HTML estático)
- Build command: *(vazio)* · Output directory: *(vazio / raiz)*
- A cada `git push`, a Vercel republica sozinha.

**Ou GitHub Pages:** Settings → Pages → Branch `main` / `root`. O `index.html` já é a home.

> Dica: mantenha o `robots.txt` (bloqueia indexação no Google) até o lançamento oficial.

## Como personalizar (sem saber programar)

No topo do `index.html`, dentro de `<script>`, tem o bloco **`CONFIG`**:

```js
const CONFIG = {
  produto:   "Kit Festa",
  titulo:    "Renda extra com <em>kit festa</em> — a partir de R$50.",
  subtitulo: "...",
  autora:    "@seu_arroba",   // ← troque pelo @ da dona do produto
};
```

Troque `autora` e, se quiser, `titulo`/`subtitulo`. Nada mais precisa ser mexido pra publicar.

## Como funciona por dentro

- **HTML + CSS + JS puro**, tudo num arquivo. Zero biblioteca externa, zero CDN.
- Os dados da usuária (kits que ela cria, ajustes de preço, meta) ficam no **`localStorage`** do
  aparelho dela. As **fotos** ficam num `localStorage` separado (`kitfesta_fotos_v2`), comprimidas
  em JPEG ~760px pra não estourar a memória.
- **Sem login e sem servidor** — a "proteção" do produto é entregar o link só a quem compra
  (o checkout entrega). Isso é o padrão pra produto de ticket baixo.
- Tema claro/escuro automático + botão de trocar.

## Estrutura

```
kit-festa/
├── index.html               → o app (é o que publica)
├── README.md                → este arquivo
├── HANDOFF.md               → o que falta finalizar (LEIA)
├── copy-pagina-vendas.md    → a copy de venda pronta
├── robots.txt               → bloqueia indexação até o lançamento
└── .deploy/                 → cópia usada em testes (pode ignorar)
```

## ⚠️ Antes de vender

Leia o **HANDOFF.md** — tem as pendências (fotos-modelo dos kits, o número da promessa, link de
checkout) e os avisos legais (não prometer renda garantida; custos são estimativa).
