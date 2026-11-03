### Hi, I'm Aleksei

I'm a backend engineer and CS student at [York University](https://www.yorku.ca/) in Toronto. In 2026 I co-founded three startups: Tanish in April as its backend engineer, Arzan in May as its sole engineer, and Temir AI in August.

- Arzan is a pre-launch cross-border e-commerce startup (China to Kyrgyzstan). I built its FastAPI/PostgreSQL API (90+ endpoints, 2,300+ backend tests), a React/TypeScript operator console and an Expo app. [Read the case study](https://alekseilian.com/arzan).
- Tanish is a dating app for Central Asia: a FastAPI/PostgreSQL backend with 2,600+ tests, a React Native iOS app on TestFlight, AWS face-liveness checks and 4 languages. [Read the case study](https://alekseilian.com/tanish).
- Temir AI turns customer orders into priced quotes. At our pilot customer, a metal supplier, 4 sales managers at 2 warehouses made about 70 quotes with it from August to October, from orders that arrive as chat text, PDFs, spreadsheets or photos. The LLM parses each order into line items, and unit prices come from the catalog.

Over summer 2026 I also built Mendy, an advice app that remembers you: FastAPI, async SQLAlchemy and PostgreSQL, with long-term memory and a tiered safety pipeline.

#### Public code

| Project | What it does | Stack |
|---------|-------------|-------|
| [URL Shortener](https://github.com/alxlyn/alex-url-shortener) | Async link shortener with retry-on-conflict inserts, per-IP rate limiting and CI against a live Postgres | Python, FastAPI, asyncpg, PostgreSQL, Docker |
| [Chess Engine](https://github.com/alxlyn/alex-chess-engine) | UCI engine with negamax, alpha-beta, quiescence, a transposition table and clock management | Python |
| [Portfolio](https://github.com/alxlyn/personal-portfolio) | My site, [alekseilian.com](https://alekseilian.com) | React, Vite |

#### How I work

I wrote the chess engine and the first Flask version of the URL shortener in February 2026, with AI help. Since March I've built mostly with AI coding agents: Claude Code day to day, and Codex and Google Antigravity as well. I make the design calls, like the data model and what a job should do if it crashes halfway, then review what the agent writes and test it before it goes in. Agents are confidently wrong often enough that I check every review finding against the source before fixing anything, and I don't trust a change until a test covers it. On Arzan I ran 17 review passes, each aimed at the fixes from the pass before, and several of them caught bugs that the previous round of fixes had introduced.

The shortener's FastAPI rewrite, its tests, the READMEs and my site were built that way. On Nov 2, 2026 I re-uploaded the repos and dropped the Claude co-author lines and AI tool files from their history. Then an AI code review found bugs in both public repos, like a move for the wrong side on a short clock and missed mates in one. I made every change and fix by hand, one small commit at a time.

The startup code stays private, so next I'm rebuilding two of its harder parts as small public repos, without an agent: Arzan's order claim, with a test that races two Postgres sessions, and then Tanish's rotating refresh tokens. I'll link them here when they're up.

#### What I use

```
Languages:      Python, TypeScript, JavaScript, SQL, Java, C
Backend:        FastAPI, SQLAlchemy 2.0 (async), Pydantic, WebSockets, PostgreSQL, Redis, Supabase
Frontend:       React, React Native (Expo)
Infrastructure: Docker, GitHub Actions, Railway, Vercel, GCP, AWS (Rekognition), Linux
AI:             OpenAI and Anthropic APIs, eval rubrics and golden sets, Claude Code, Codex, Antigravity, AI code review
```

#### Links

[alekseilian.com](https://alekseilian.com) · [LinkedIn](https://linkedin.com/in/aleksei-lian) · [X @_alxlyn](https://x.com/_alxlyn)
