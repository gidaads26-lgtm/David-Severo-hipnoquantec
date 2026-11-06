# HipnoQuantec® – site institucional

Site de uma página do método HipnoQuantec®, de David Severo: acompanhamento para ansiedade que integra Hipnose Clínica, Par Biomagnético e Quantec® Pro.

## Como ver

Abra o `index.html` no navegador. É um arquivo único, com estilos, scripts e imagens embutidos, sem etapa de build.

- Os vídeos de depoimento tocam dentro da página quando o site está publicado (endereço `https://`). Abrindo o arquivo direto do computador, eles abrem no YouTube.
- As fontes (Source Serif 4 e Plus Jakarta Sans) carregam pelo Google Fonts.

## Onde mudar as coisas

- **WhatsApp dos botões de agendamento:** constante `WHATSAPP` no fim do `index.html` (os links `wa.me` também estão escritos direto nos botões).
- **Endereço:** seção `#local` e rodapé.
- **Redes sociais:** rodapé (`.foot-social`).

## Pendências antes de publicar

Os trechos marcados em amarelo no site (classe `pending`) ainda dependem de dados do cliente:

- foto, nome, função e formação do segundo profissional;
- formação e registros profissionais.

## Arquivos

- `index.html`: o site.
- `paleta-azul-dourado.html`: versão de teste do site com a paleta azul-marinho e dourado (não aparece no Google). Acesse em `/paleta-azul-dourado.html`.
- `og-image.jpg`: imagem que aparece quando o link do site é compartilhado (WhatsApp, Instagram, Facebook).
- `docs/prompt-claude-code.md`: prompt usado para gerar a copy.no Claude Code.
