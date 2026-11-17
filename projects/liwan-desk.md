# Liwan Desk: WhatsApp front-desk agent for a dental clinic

**Repo:** https://github.com/tadiwachirambamhanda-cyber/liwan-desk · **Live:** https://liwan-desk.vercel.app · **Stack:** Next.js 16, React 19, TypeScript, Zod, Supabase, Claude (Anthropic SDK), Jev classifier, Vercel · **Data:** synthetic only

## What it does
Answers a Dubai dental clinic's WhatsApp messages in English and Arabic: prices, opening hours, free appointment times, greetings and thanks. Anything it should not answer (emergencies, complaints, cancellations, unlisted treatments, medical advice) goes to a person, with a kind holding reply that matches the situation.

## How it is built
- **Jev sorts the message** (with a Claude fallback); **about 570 lines of plain-code clinic rules** decide; Claude writes only a warm opening and closing around lists that code builds; **a reply checker** (an allow-list of prices, times and claims) approves every reply before it is sent.
- **Memory (built, in an open pull request, not yet on `main`):** every message, step, cost and hand-over is saved in Supabase through atomic database functions; reloading restores the whole chat and the staff "what the agent did" panel.
- **Hardening:** webhook signature check, rate limiting, duplicate-message protection, agent stays quiet while a person has the conversation (except emergencies), a templates-only fallback mode, row-level security on all tables, secrets server-side only.
- Runs on Vercel in Mumbai next to the Supabase database; a phone-style simulator page for demos; CI on pull requests.

## Numbers
About 2,700 lines of TypeScript on `main`, 22 commits, 3 database migrations, 11 merged pull requests (memory is a 12th, still open).

## Skills shown
Agent architecture, guardrails, Supabase, serverless deployment, security hardening.
