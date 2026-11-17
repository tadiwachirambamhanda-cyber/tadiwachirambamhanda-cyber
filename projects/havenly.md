# Havenly: student community and housing app for Dubai

**Live web build:** https://havenly-app-zeta.vercel.app · **Repo:** https://github.com/tadiwachirambamhanda-cyber/havenly · **Stack:** React Native, Expo, TypeScript, Supabase (Postgres, Auth, Storage, Realtime), React Navigation, Vercel (web)

![Havenly screens: feed, post detail, Discover, profile](images/havenly-screens.png)

*Feed, post detail, Discover and profile from the web build running locally. The posts shown are clearly labelled sample posts; no real members' content appears.*

## Try it without an account
The login screen has an **Explore without signing up** button that opens a read-only demo of the app with sample content. It is built so a visitor can never touch the real database: a switch sends every call to an in-memory demo client, every write (post, like, message, upload, profile edit) is refused with a clear message, and nothing is stored on the device. 19 automated tests cover this, including one that fails if the real database is ever reached. Open the [live web build](https://havenly-app-zeta.vercel.app) and tap the button.

## What it is
A visual-first community app for students and young adults in Dubai: a card feed with editorial picks, Discover (spots and events), interest and campus communities, real-time direct messages, profiles, and a student housing section with listings, enquiries and a referral-fee pipeline.

## What I built
I am the founder and sole builder: product, design, code and database.
- iOS, Android and web from one codebase, with the web build live on Vercel.
- 35 screens: masonry feed with editorial picks, Discover, interest and campus communities, real-time messages with message requests, group chats, a map, events, notifications and student perks that unlock as a daily streak grows.
- Student housing: listings, enquiries, admin review and a referral-fee pipeline.
- Supabase back end with 28 tables and 122 row-level security policies. Blocking and message requests are enforced in the database, not only on screen. Account deletion removes chat traces and uploads.
- Trust and safety: an adversarial review closed five security holes; draft privacy policy and terms; crash reporting. After Supabase's security scan flagged functions callable by signed-out visitors, I locked them down with reviewed, tested database migrations (dry-run in a rolled-back transaction first) without breaking the row-level security policies that depend on them.
- Design and UX: Phosphor icons, dark mode, skeleton loaders, UX-law fixes (Fitts, Doherty, Miller, Jakob).

## Numbers
**162 commits** over 2 months, about **13,900 lines of TypeScript**, 60 SQL files, CI checks, launch PRD and technical requirements documents.

## Skills shown
Mobile development, relational schema design, row-level security, real-time features, product thinking for the UAE student market.
