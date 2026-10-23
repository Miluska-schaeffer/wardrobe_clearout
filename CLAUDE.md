# CLAUDE.md

## About this project
A feature inside a fictional secondhand clothing marketplace that makes listing a whole pile of clothes much faster (an unofficial concept, not connected to any real marketplace). The product name isn't decided yet.
The user sets a minimum price once, then photographs clothes item by item. AI drafts each listing (title, description, brand, size, colour, material, condition) and marks every field as: read from a photo, guessed, or not found. For judgment calls like condition, the AI explains its suggestion. Prices come from data on similar sold items, not from the AI. The user reviews each draft in a queue, most valuable first, and confirms or fixes it. Items likely to sell below the minimum price get a "donate instead" suggestion.
This is a portfolio prototype. Clarity and good UX matter more than scale.

## About me
I'm a product designer, not a developer. I learned some web development years ago and I'm rusty. I need to understand every change, because I will explain this code in job interviews.

## How to work with me
- Explain your plan in plain words before you change any code. Wait for my OK.
- Work in small steps: one change at a time, so each change fits into one commit.
- After each change, tell me which files you touched and why, in 2–3 sentences.
- If something is unclear, ask me. Don't guess what I want.
- Tell me whether you know something (you checked the code, the docs or ran it) or are guessing, and how sure you are.
- Don't add new libraries or packages without asking me first, and tell me why we need them.
- When you use a concept I may not know, explain it in one sentence.

## Stack
- Next.js (App Router) with TypeScript. This Next.js version may be newer than what you know. Follow AGENTS.md and check the docs in node_modules/next/dist/docs/ before writing Next.js code, and tell me when something works differently than you expected.
- Tailwind CSS, shadcn/ui components
- Deployed on Vercel from the main branch on GitHub
- Later: Claude API, called only from server-side routes

## Rules
- Mobile-first. Design for a phone screen first (about 390px wide), then larger screens.
- Accessibility basics on every screen: semantic HTML, labels on every input, visible focus states, keyboard navigation, enough colour contrast.
- Never put API keys or secrets in the code or in anything the browser can see. Keys live in environment variables (.env.local, never committed).
- Use mock data for now, kept in one clearly named file (for example lib/mock-data.ts), so it's easy to swap for real AI output later.
- Keep components small and named after what they are in the product (ListingDraft, FieldSourceBadge), not after how they look.
- Interface text: short, friendly and honest. Never claim the AI is sure when it isn't.

## Git
- I commit myself after reading the diff. Don't commit or push unless I ask.
- Suggest a short commit message in plain English after each change.
