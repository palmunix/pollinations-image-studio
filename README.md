# ✦ Pollinations Image Studio

Um gerador de imagens com IA que usa a API da [Pollinations](https://pollinations.ai). O usuário conecta sua própria conta Pollinations com o botão **Connect** e gera imagens usando o **próprio saldo** — o app nunca pede para colar chaves de API.

[![Made with pollinations.ai](https://raw.githubusercontent.com/pollinations/pollinations/main/packages/ui/src/brand/badge-made-with.svg)](https://pollinations.ai/?ref=badge)

## Funcionalidades

- 🔐 **Sign-in com Pollinations** via drop-in `<polli-connect>` (OAuth, sem App Key)
- 🎨 **4 modelos de imagem** para escolher (Flux 1 Schnell, Z-Image Turbo, Qwen Image, Flux 2 Klein)
- 📐 **4 proporções** (1:1, 4:3, 3:4, 16:9)
- ⬇️ **Download** da imagem gerada
- 💰 Usa o saldo do próprio usuário (sem custo para o desenvolvedor)

## Como usar

1. Abra o app
2. Clique em **Connect** no canto superior direito e autorize sua conta Pollinations
3. Descreva a imagem, escolha modelo e proporção
4. Clique em **Gerar imagem**
5. Baixe ou abra a imagem em nova aba

## Detalhes técnicos

- Sem build step: HTML + CSS + JS puro
- `<polli-connect>` do `@pollinations/ui@0.1.0-alpha.20` via CDN
- A chave do usuário é lida de `connect.apiKey` e mantida em `sessionStorage`
- Imagens geradas via `GET https://gen.pollinations.ai/image/{prompt}` com `Authorization` embutido na query

## Submissão

App criado para a quest `app_listed` do Pollinations.
