# CLAUDE.md: Hunger Games em Berlim

**Antes de trabalhar:** leia `PROGRESS.md` pra saber o que já foi feito e o que falta.

## O que é
Página única (`index.html`) com 11 locações de Hunger Games em Berlim e o roteiro de um Reels de ~1:30 (com falas extras pra cortar na edição). Publicada no GitHub Pages.

## Stack
- HTML + CSS + JS puro num arquivo só. Sem framework e sem biblioteca externa.
- Fotos e cenas embutidas em base64 (JPEG). Tudo funciona offline.
- Os dados (paradas, acesso, roteiro) ficam em `const STOPS`, `REELS` e `EXTRAS` dentro do HTML.

## Design
- Fundo `#0f0f11`, painéis `#18181c`, dourado `#d6a93c` (destaque), vermelho `#c8282f` (alerta/"não").
- Fonte do sistema (Segoe UI e similares). Sem emojis na interface, sem gradientes decorativos.
- **Regra do Rod: nunca resolver espaço com barra de rolagem.** O conteúdo tem que caber na janela:
  - tamanho do texto escala com a altura (`clamp(..vh..)`);
  - no celular (até 760 px) vira abas (Fotos, No filme, Acesso, Fatos) e seletor de trechos do Reels.
- Cor do ponto de acesso: verde = pode, dourado = parcial, vermelho = não.

## Convenções de conteúdo
- Texto em português do Brasil.
- Cada lugar tem: foto de hoje, cena, o que foi gravado, acesso (entrar / locação exata), 3 fatos, 1 curiosidade.
- Fato não confirmado é marcado como relato (ex.: curiosidade do Tempelhof).
- Kuppelsaal e Museumspark Rüdersdorf ficaram fora de propósito (ver `PROGRESS.md`).

## Fotos
- Lugares: Wikimedia Commons, com autoria e licença na legenda.
- Cenas: imagens de divulgação (© Leonine Studios, © Studiocanal). Se algum dia houver pedido de remoção, trocar por fotos próprias.
