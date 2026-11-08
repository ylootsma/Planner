# Planner

Planning app and website: a self-adjusting planner that covers all 24 hours, with day, week and month views, to-dos, goals, events and automatic planning around your calendar.

## Stack

Next.js + Supabase (database and login), first as an installable web app (PWA), later as a store app (Expo). Hosted on Vercel.

## How work is done

Work is organised in **epics** (main features) and **features** (sub features). Every feature passes four sign-offs:

1. **Stories**: user stories and acceptance criteria, reviewed and signed off.
2. **Mockup**: clickable mockup in phone, tablet and PC size, signed off.
3. **Build**: on its own branch, with a preview link.
4. **Check**: every story tested against its acceptance criteria and signed off before merging.

## Branches

- `main` is the live app. Only signed-off work lands here.
- One branch per feature: `feature/<epic>-<feature>`, e.g. `feature/entries-todo`. Each has one pull request with the preview link and the sign-off.
- Each story is an issue, with its acceptance criteria as tick boxes. Each epic is a milestone.

## Epics

| # | Epic | Features |
| --- | --- | --- |
| 1 | Foundation | Project setup · Data model · Design system |
| 2 | Users | Sign-up and login (web) · Profile and settings · Landing page · Sign-up in the app |
| 3 | Layout / UX | App shell and navigation · Mobile · Tablet · PC |
| 4 | Entries | To-do · Event · Goal · Repeat rules · "To plan" list |
| 5 | Planning engine | Auto-plan · Travel time · Clash detection · Replan · Learn my pace |
| 6 | Calendar | Day · Week · Month · Tick off and drag · Filter by |
| 7 | Overview | Tracking to-dos · Tracking goals · Visual representation · Mini overviews · Done log |
| 8 | External input | Google Calendar sync · Email · File uploads · Evening check |
| 9 | Notifications | Reminders · Evening summary · Goal sign-off prompt |

Build order: 1 → 2 → 3 → 4, then 5 and 8 in parallel, then 6 and 7 in parallel, then 9.

## Folders

- `docs/stories/` signed-off stories per epic
- `docs/mockups/` signed-off mockups per epic
- `docs/reference/` the earlier single-page planner (v3), kept for reference only. The new app starts with empty data.
