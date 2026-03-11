# Epubly

**Converta PDFs escaneados em EPUBs limpos, direto no navegador.**

Envie um PDF escaneado — torto, manchado, antigo, em página dupla. A IA extrai o texto, reconhece tabelas e identifica figuras, entregando tudo limpo para o seu e-reader.

![OCR](https://img.shields.io/badge/OCR-Qwen2.5--VL-blueviolet?style=flat-square) ![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square) [![Ko-fi](https://img.shields.io/badge/Apoie-Ko--fi-FF5E5B?style=flat-square&logo=ko-fi&logoColor=white)](https://ko-fi.com/epubly)

---

## Como funciona

1. Arraste ou selecione um PDF escaneado
2. Ajuste as configurações — título, autor, idioma, páginas
3. Clique em **Converter para EPUB**
4. Baixe o `.epub` pronto para Kindle, Kobo ou Apple Books

O processamento acontece no seu navegador. As imagens das páginas vão direto para a API de IA — nenhum arquivo passa por servidores do Epubly.

---

## Funcionalidades

- **OCR via Qwen2.5-VL** — modelo de visão de última geração; lê texto de páginas tortas, manchadas ou de baixa qualidade
- **Separação de páginas duplas** — detecta spreads automaticamente, encontra o gutter da encadernação e divide cada metade com precisão
- **Seleção de páginas** — converta só o intervalo que quiser (`1-5`, `1,3,7`, `1-5,8,12`). Páginas fora da seleção não são nem renderizadas
- **Reconhecimento de tabelas** — converte tabelas do PDF em HTML `<table>` válido no EPUB
- **Reconhecimento de figuras** — detecta ilustrações, gravuras e fotografias e as embute como imagem no EPUB
- **Correção de hifenização** — une palavras quebradas no fim de linha
- **EPUB 2.0 válido** — compatível com Kindle, Kobo, Apple Books e outros leitores
- **Detecção automática de capítulos** — identifica e estrutura o sumário (TOC) do EPUB

---

## Tecnologias

- [PDF.js](https://mozilla.github.io/pdf.js/) — renderização de PDF no navegador
- [Qwen2.5-VL](https://huggingface.co/Qwen/Qwen2.5-VL-72B-Instruct) via [OpenRouter](https://openrouter.ai) — OCR multimodal
- [Cloudflare Workers](https://workers.cloudflare.com/) — proxy serverless para proteger a chave de API
- [QRCode.js](https://davidshimjs.github.io/qrcodejs/) — geração do QR code PIX
- EPUB 2.0 gerado em JavaScript puro, sem dependências

---

## Apoie o projeto

O Epubly é gratuito, mas cada conversão tem um custo real de processamento de IA. Se ele foi útil para você, considere uma contribuição:

- 🇧🇷 **PIX** — disponível diretamente no app, clique em *♡ Apoie-nos*
- 🌍 **Ko-fi** — [ko-fi.com/epubly](https://ko-fi.com/epubly) · aceita PayPal e cartão de qualquer país

Qualquer valor ajuda a manter o servidor e as chamadas de IA. Obrigado ♡

---

## Licença

MIT — use, modifique e distribua livremente.
