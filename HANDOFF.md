# preagi — Handoff

The "where did we leave off" doc. Update at the end of every working session. Last updated: **2026-04-26** (initial v1 build session).

## Status: v1 built locally, not yet deployed

Site builds cleanly. Dev server confirmed working at http://localhost:4321/ (will be killed on machine restart — restart with `npm run dev`).

## Done

- [x] Bought `preagi.ai` and `preagi.dev` on Porkbun (`preagi.com` wasn't available)
- [x] Email forwarding set up: `hello@preagi.ai` → `avinashgopinathan6@gmail.com`
- [x] Node 25 installed via Homebrew
- [x] Astro + Tailwind scaffold at `~/code/preagi/`
- [x] Four v1 sections built (Hero, Socials, HowIWork, ViewsOnAI)
- [x] Editorial design system (Fraunces + Inter + JetBrains Mono, warm bg, burnt-orange accent, system dark/light)
- [x] `IDEAS.md` seeded with v2+ roadmap
- [x] Local git: 2 commits on `main`, no remote yet
- [x] Build verified: `npm run build` clean

## Blocked / open

- [ ] **Vercel login** — Avinash hit a login issue. Suspects: popup blocker on GitHub OAuth, or magic-link email not arriving. Backup options if Vercel keeps fighting: Cloudflare Pages, Netlify (both free, both auto-deploy from GitHub).
- [ ] **GitHub push** — Avinash said "GitHub done" but local repo has no remote configured (`git remote -v` is empty). Either the remote command wasn't run, or it ran in a different shell. Need GitHub username to set up `git remote add origin` and push.

## Next actions (in order)

1. **Verify GitHub state** — confirm the repo exists on GitHub (likely `github.com/<username>/preagi`), then locally:
   ```
   cd ~/code/preagi
   git remote add origin git@github.com:<username>/preagi.git
   git push -u origin main
   ```
2. **Resolve Vercel login** — diagnose specific error and unblock. Or pivot to Cloudflare Pages / Netlify.
3. **Deploy** — connect repo on Vercel, accept Astro auto-detect, deploy.
4. **Wire DNS at Porkbun** — A record (`76.76.21.21`) and CNAME (`cname.vercel-dns.com`) for `preagi.ai` and `www.preagi.ai`.
5. **Mobile + desktop check on live URL.**
6. **Lighthouse audit** — target ≥ 90 on all four categories.

## Open copy edits Avinash hasn't reviewed yet

These were drafted from the persona file. Worth a careful read before publish:

- **`src/components/Hero.astro`** — current one-liner: *"Director of Underwriting Strategy at Ramp. I own the credit policy and lead the push to automate underwriting decisions. Operator who sees systems and brings out the best in people."*
- **`src/components/HowIWork.astro`** — 7 principles with title + body. Titles I wrote are mine; some may want edits ("Optimize for myself, sober about institutions" is the most editorial).
- **`src/components/ViewsOnAI.astro`** — 5-paragraph essay with the "We are pre-AGI" hook. This is the section Parag would actually read. Spend the most time here.

## Decisions banked (don't relitigate)

- Domain: `preagi.ai` primary, `preagi.dev` parked.
- Stack: Astro + Tailwind + Vercel (no Next.js, no Framer).
- v1 = single landing page, four sections. Everything else lives in `IDEAS.md` until we build it.
- No photo on hero (text-only is on-brand).
- No dark/light toggle in v1 (system pref only).
- Email: `hello@preagi.ai`.

## How to recover after a machine restart

```bash
cd ~/code/preagi
claude --resume      # or: claude (CLAUDE.md auto-loads, then read this file)
npm run dev          # bring back the dev server
```

Tell Claude: *"Read HANDOFF.md and pick up from there."*
