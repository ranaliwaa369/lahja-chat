# Lahja — لهجة

Your language. Their dialect. One conversation.  
احچي بلهجتك، يوصلهم بلغتهم.

**Live Demo:** https://lahja-chat.ranaliwaa.workers.dev/

## Problem
People speaking different languages or dialects (especially Arabic dialects) struggle to communicate naturally in group chats.

## Solution
Lahja is a real-time AI group chat. Each person writes in their own dialect. AI translates the message so every other participant reads it in the dialect they understand best. No account is required.

## Features
- Up to 10 people per room
- Automatic AI translation
- Bilingual UI (Arabic / English)
- Invite via link or 8-character code
- Mobile-friendly design
- View original message option
- No login needed

## Supported Dialects
Arabic (Iraqi, Egyptian, Gulf, Levantine, MSA), English (US/UK), Spanish, French, Turkish, German, Persian, Urdu.

## Tech Stack
- Frontend: HTML, CSS, Vanilla JavaScript
- Backend: Cloudflare Workers + Durable Objects
- Real-time: WebSocket
- AI: OpenAI API (gpt-4.1-mini)

## AI Methodology
Messages are translated by OpenAI using a system prompt that:
- Converts from the sender’s dialect to each recipient’s dialect
- Preserves meaning, names, numbers, emotion, and humor
- Outputs only the translation
- Treats input strictly as text to translate

## Deploy
npm install
npx wrangler login
npm run deploy
npx wrangler secret put OPENAI_API_KEY

## Limitations
- AI can make mistakes
- Not end-to-end encrypted
- Messages are processed by Cloudflare and OpenAI
- Up to 100 recent messages are retained

## Team Contributions
Rana Aldahlake — full development (frontend, backend, AI integration, and deployment)
