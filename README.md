[README.md](https://github.com/user-attachments/files/26327353/README.md)
# Epubly

**Converta PDFs escaneados em EPUBs limpos, direto no navegador — sem instalar nada, sem criar conta.**

Envie um PDF escaneado — torto, manchado, antigo, em página dupla. A IA extrai o texto, reconhece tabelas e identifica figuras, entregando tudo limpo para o seu e-reader.

![OCR](https://img.shields.io/badge/OCR-Qwen2.5--VL-blueviolet?style=flat-square) ![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square) [![Ko-fi](https://img.shields.io/badge/Apoie-Ko--fi-FF5E5B?style=flat-square&logo=ko-fi&logoColor=white)](https://ko-fi.com/epubly)

**→ [epubly.github.io](https://pdvrx.github.io/epubly/)**

---

## Como funciona

1. Arraste ou selecione um PDF escaneado
2. Ajuste título, autor, idioma e intervalo de páginas
3. Clique em **Converter para EPUB**
4. Baixe o `.epub` ou acesse direto no KOReader via catálogo OPDS pessoal

O processamento acontece no seu navegador. As imagens das páginas vão direto para a API de IA — nenhum arquivo passa por servidores do Epubly.

---

## Funcionalidades

**Conversão**
- **OCR via Qwen2.5-VL** — modelo de visão de última geração; lê texto de páginas tortas, manchadas ou de baixa qualidade
- **PDFs digitais** — detecta automaticamente se o PDF já tem texto selecionável e extrai sem OCR, de graça e instantâneo
- **Separação de páginas duplas** — detecta spreads, encontra o gutter da encadernação e divide com precisão
- **Negrito e itálico preservados** — tanto em PDFs digitais quanto no OCR
- **Seleção de páginas** — converta só o intervalo que quiser (`1-5`, `1,3,7`, `1-5,8,12`)
- **Reconhecimento de tabelas** — converte tabelas em HTML `<table>` válido no EPUB
- **Reconhecimento de figuras** — detecta ilustrações e as embute como imagem
- **Correção de hifenização** — une palavras quebradas no fim de linha
- **Limpeza automática** — remove cabeçalhos e rodapés repetidos, números de página inline
- **Notas de rodapé** — detectadas e colocadas no final de cada página
- **OCR paralelo** — 3 lotes simultâneos, ~3× mais rápido que serial

**EPUB gerado**
- **EPUB 2.0 válido** — compatível com Kindle, Kobo, Apple Books, KOReader
- **Sumário (TOC)** com detecção automática de capítulos e número de página
- **Capa** gerada a partir da primeira página do PDF

**Envio para e-reader**
- **Catálogo OPDS pessoal** — após cada conversão o livro fica disponível por 24h no seu catálogo privado; configure uma vez no KOReader e esqueça
- Código pessoal de 6 caracteres garante que você veja apenas seus livros

**Interface**
- Internacionalização em português, inglês e espanhol
- Contador público de livros convertidos
- Tema escuro, responsivo, sem anúncios

**Infraestrutura**
- Chave de API protegida via Cloudflare Worker — nunca exposta no cliente
- Armazenamento temporário de EPUBs via Cloudflare KV (24h, até 15MB por livro)

---

## KOReader + OPDS — envio sem fio

A integração mais prática para quem usa KOReader (inclusive em Kindle com jailbreak):

1. Clique em **KOReader** no header do site
2. Copie sua URL pessoal (ex: `https://.../opds?code=Ab3kX9`)
3. No KOReader: **Busca de livros → Catálogos OPDS → +** → cole a URL
4. Pronto. Cada conversão aparece automaticamente no catálogo, sem cabo, sem app extra

## Apoie o projeto

O Epubly é gratuito, mas cada conversão tem um custo real de processamento de IA.

- 🇧🇷 **PIX** — disponível no app, clique em *Apoie-nos*
- 🌍 **Ko-fi** — [ko-fi.com/epubly](https://ko-fi.com/epubly) · PayPal e cartão internacional

---

## Licença

MIT — use, modifique e distribua livremente.
