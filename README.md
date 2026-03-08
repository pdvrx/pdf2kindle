[README (1).md](https://github.com/user-attachments/files/25829139/README.1.md)
# Epubly

**Converta PDFs escaneados em EPUBs limpos, direto no navegador.**

Envie um PDF escaneado — torto, manchado, antigo, em página dupla. A IA extrai o texto e entrega ele limpo para o seu e-reader.

![Epubly](https://img.shields.io/badge/OCR-Google%20Gemini-orange?style=flat-square) ![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)

---

## Como funciona

1. Arraste ou selecione um PDF escaneado
2. Insira sua chave de API do Google Gemini (gratuita)
3. Ajuste as configurações — título, autor, idioma, páginas
4. Clique em **Converter para EPUB**
5. Baixe o `.epub` pronto para Kindle, Kobo ou Apple Books

O processamento acontece inteiramente no seu navegador. Nenhum arquivo é enviado a servidores do Epubly.

---

## Funcionalidades

- **OCR via Gemini Vision** — lê texto de páginas tortas, manchadas ou de baixa qualidade
- **Separação de páginas duplas** — detecta spreads automaticamente e divide cada metade
- **Seleção de páginas** — converta só o intervalo que quiser (`1-5`, `1,3,7`, `1-5,8,12`)
- **Correção de hifenização** — une palavras quebradas no fim de linha
- **EPUB 2.0 válido** — compatível com Kindle, Kobo, Apple Books e outros leitores
- **Processamento em lotes** — 3 páginas por chamada à API, reduzindo uso de cota em ~65%
- **Rate limit inteligente** — backoff exponencial e detecção de cota diária esgotada
- **Chave armazenada localmente** — nunca sai do seu navegador

---

## Como obter a chave de API

1. Acesse [aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey)
2. Clique em **Create API key**
3. Copie a chave (começa com `AIza...`)
4. Cole no campo da chave no Epubly e clique em **Salvar**

O plano gratuito permite ~1.500 requisições/dia — suficiente para dezenas de livros.

---

## Uso local

O Epubly é um único arquivo HTML. Para rodar localmente sem problemas de CORS:

```bash
python3 iniciar_servidor.py
```

Acesse `http://localhost:8000` no navegador.

> **Não abra o `index.html` diretamente via `file://`** — o PDF.js exige um servidor HTTP para funcionar corretamente.

---

## Licença

MIT — use, modifique e distribua livremente.
