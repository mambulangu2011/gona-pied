# GonaAI Jigawa - gona-pied

Live Demo: https://gona-pied.vercel.app/
Hausa AI Extension Officer for Jigawa Farmers

## Architecture (A)
- Frontend: Next.js 14 on Vercel (https://gona-pied.vercel.app/)
- Backend: Vercel AI SDK + Groq Llama3 for reasoning
- Voice: Web Speech API (Hausa) + Whisper
- Tools: 3 MCP Servers integrated

## MCP Implementation (B)
1. Weather MCP - getWeather(location) -> returns forecast, rain probability for Jigawa LGA
2. Market MCP - getMarketPrice(crop, market) -> Gumel/Hadejia market prices
3. Pest MCP - diagnosePest(image/description) -> identifies pest & treatment
Built with MCP SDK - tools/mcp/weather.ts, market.ts, pest.ts - agent decides when to call

## How Agentic Behavior Achieved (C)
User speaks in Hausa -> Agent transcribes -> LLM reasons -> Decides which MCP to call (multi-step) -> Calls tools -> Synthesizes cited answer in Hausa -> Returns with source citation. Not just chatbot, it acts via tools.

## Capabilities Used (D)
[x] Agentic Behavior (multi-step tool calling)
[x] Vercel AI SDK (useChat, streamText)
[x] MCP - 3 custom tools integrated
[x] Hausa Voice Interface

## Tech Stack
Next.js, TypeScript, Tailwind, Groq, Vercel AI SDK, MCP

## Team
Abubakar Muhammad - mambulangu2011
