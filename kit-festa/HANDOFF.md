# 🤝 HANDOFF — Kit Festa (o que falta finalizar)

Documento pra quem vai terminar o produto. O app **já funciona**. Aqui está o que está pronto,
o que falta, e os avisos que não podem ser esquecidos.

---

## ✅ O que JÁ está pronto (funcional)

- App completo em `index.html` (arquivo único, sem build).
- **10 kits prontos** (Aniversário, Só Docinhos, Só Salgados, Bolo no Pote, Kids, Chá da Tarde,
  Gourmet, Mini, Reunião, Completo) — cada um com itens, preço sugerido, custo e lucro calculado.
- **Calculadora de lucro** — a usuária ajusta preço e custo (da cidade dela) e o lucro recalcula na hora,
  com margem % e aviso (vermelho / margem apertada / saudável).
- **11 receitas** (brigadeiro, beijinho, surpresa de uva, cajuzinho, ninho, bolo de pote, coxinha,
  kibe, enroladinho, pastel, empadinha).
- **Foto por kit** — a usuária tira/sobe a foto do kit dela (galeria ou câmera). Comprimida e salva no aparelho.
- **Criar kit próprio** — nome, foto, itens, preço, custo. Vira o catálogo dela. Edita e exclui.
- **Tela "Minha meta"** — ela digita quanto quer ganhar e o app diz quantos kits/mês e /dia.
- Termo de aceite + rodapé legal + tema claro/escuro + compartilhar kit.

## 🔧 O que FALTA finalizar (pendências)

1. **Fotos-modelo dos 10 kits.** Hoje o slot de foto é da usuária — o app **não vem com uma foto de
   como cada kit fica montado**. A copy de venda promete "a foto de como o kit fica", então, pra a
   promessa ser verdadeira, gerar/adicionar **10 imagens** (uma por kit) numa pasta `img/` e referenciá-las
   como foto padrão do kit (com a foto da usuária sobrepondo quando ela subir a dela).
   *Sugestão: gerar com IA (fotos de mesa de doces/salgados montada) ou usar fotos próprias com direito de uso.*

2. **O número da promessa na copy.** A copy usa "mais de R$1.000/mês (vendendo 1 kit/dia)". Definir o
   número final **e mantê-lo sempre como potencial** ("dá pra fazer"), NUNCA como garantia (ver Legal).

3. **Link de checkout.** O app não tem pagamento (nem precisa). O fluxo é: página de vendas →
   checkout (Hotmart/Kiwify) → entrega do link do app. Falta criar o produto no checkout e ligar a
   página de vendas a ele.

4. **Página de vendas.** A copy pronta está em `copy-pagina-vendas.md`. Falta montar a página
   (design + código) e publicar. *(Pode ser feita com a skill `pagina-de-vendas-completa`.)*

5. **CONFIG.** Trocar `autora` (o @) no bloco CONFIG do `index.html`.

## ⚠️ AVISOS TÉCNICOS

- **Fotos e dados ficam só no aparelho** da usuária (localStorage). Se ela trocar de celular, não vão
  junto. É o preço de um app sem login/servidor. Pra sincronizar entre aparelhos, precisaria de conta +
  backend (outro nível de projeto).
- **Sem login** — a proteção é entregar o link só a quem paga (checkout com robots.txt bloqueando indexação).
- **Nome de domínio `.vercel.app` é global** — `kit-festa.vercel.app` já está ocupado por outra pessoa.
  Este projeto foi publicado em `kit-festa-pink.vercel.app`. Use um nome livre ou um domínio próprio.

## ⚖️ ZONA PROIBIDA (legal — não pode esquecer)

- **NÃO prometer renda garantida.** CDC art. 37 proíbe. Use "dá pra fazer", "com base na conta",
  "vendendo 1 kit por dia" — nunca "você vai ganhar R$X garantido".
- **Custos são estimativa** — o app já avisa isso; manter o aviso, porque preço de ingrediente varia por cidade.
- **Vender comida caseira** pode exigir MEI + boas práticas sanitárias (varia por município). O app
  orienta como conteúdo educativo, sem se responsabilizar pela regularização da usuária.
- **Não fabricar depoimento falso** — usar só prova real de clientes.

## Pesquisa que embasa o produto (por que vende)

- Confeitaria é o setor com **maior índice de precificação errada** do food service. [Nuvemshop]
- **10,4 milhões de mulheres** à frente de negócios no Brasil (Sebrae).
- Curso concorrente do nicho com **1.850 avaliações** = prova de venda real (Hotmart).
- Relatório completo (interno): `criacao/analises/2026-09-02-renda-extra-doces.md`.
