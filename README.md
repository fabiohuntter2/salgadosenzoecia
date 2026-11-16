# Salgados Enzo e Cia

Ferramentas para vender salgados em grupos de WhatsApp, com pagamento por Pix.

## Arquivos

| Arquivo | O que é |
|---|---|
| `loja.html` | Página de pedidos para o cliente. Ele escolhe os combos e os sabores, informa nome e endereço, paga no Pix com o valor exato do pedido e envia o pedido pelo WhatsApp. Tem **Modo ADM** (rascunho e prévia antes de publicar) e **Modo cliente**. |
| `index.html` | Gerador de banner com Pix para abrir direto no computador. Junta o banner da loja com uma faixa com QR Code e chave Pix, e monta a mensagem pronta para o grupo. |
| `artifact.html` | O mesmo gerador de banner, na versão publicada no Claude. |
| `banner-loja.jpg` | Banner original da loja. |

## Como funciona o Pix

O QR Code e o Pix Copia e Cola são gerados na própria página, no padrão BR Code do Banco Central (EMV com CRC16). Quando o pedido tem valor, o código já cobra o total. Não há servidor nem cobrança automática: a loja confere o comprovante enviado pelo WhatsApp.

## Onde está no ar

- Página de pedidos: publicada como artifact no Claude.
- Para editar produtos e preços, abra o link do artifact com `#adm` no final, logado na conta dona. As alterações ficam como rascunho até você tocar em **Publicar agora**.

> Os arquivos `.html` trazem as imagens embutidas (data URI), por isso são grandes.
