# Tuitionless: scholarship matcher

**Repo:** https://github.com/tadiwachirambamhanda-cyber/tuitionless · **Live:** https://tuitionless.vercel.app · **Stack:** Next.js 16 (App Router), TypeScript, Supabase, Vitest, Vercel

## What it does
A student answers a short step-by-step profile (nationality, university country and city, level, field, yearly budget in any currency) and sees scholarships grouped as **Best fit, Worth a try and Stretch**, each with the reason it matched, and a link to the official application page. Phone first.

## What I built
- Matching engine and currency conversion, results screens, scholarship detail pages.
- A researched dataset of **169 scholarships** across 9 destination countries plus global awards, and a country cost-of-living table.
- Built as a **parallel team workflow:** a chief-architect foundation, then 3 lanes (matching, screens, research) with separate file ownership and ports, merged through gated pull requests. 19 commits in 4 days.
- `npm run check` (typecheck, lint, test, build) must pass; a daily health cron keeps the free-tier database awake.

## Skills shown
Product scoping, data research and modelling, parallel delivery, CI discipline.
