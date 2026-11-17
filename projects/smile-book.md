# Smile Book: bilingual braces-reminder agent

**Repo:** https://github.com/tadiwachirambamhanda-cyber/braces-reminders · **Stack:** Next.js 16, TypeScript, Zod, Claude (Anthropic SDK), Jev classifier, Vitest · **Data:** synthetic only

## Problem
A Dubai dental clinic treats about 50 braces patients a month. About 20 of them miss their monthly visit, which delays treatment, and reminding people by hand is slow.

## What I built
- A weekly run that picks the braces patients due that Friday with no booking and sends a warm **English and Arabic** reminder in one message.
- Hard rules in code: at most two reminders per visit, none outside 17:00 to 22:00 clinic time (UTC+4), then the patient goes on a call list for a person.
- A receptionist screen to approve wording, book 20-minute slots (a taken slot cannot be booked twice) and work the call list. A booking triggers an automatic confirmation with the exact day and time from the booking record.
- Replies to patients: visit window, a fixed AED 300 price answer, and a caring reply to pain or damage that goes first on the call list as urgent. The AI never writes a time, date or price and never claims anything is booked.

## Numbers
- **193 automated tests** in 12 files, all passing.
- **14 features**, 5 acceptance criteria, each with a checkable done-test (for example: Monday run creates exactly 12 reminders from 60 synthetic patients).
- 3 rounds of independent AI code review, findings checked against the running app.
- About 2,260 lines of TypeScript. Built and merged in 2 days through 8 pull requests.

## Skills shown
Agent design, rules-in-code architecture, bilingual copy, scheduling logic, testing, code review discipline.
