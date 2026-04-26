# preagi — Handoff

The "where did we leave off" doc. Update at the end of every working session. Last updated: **2026-04-26** (deploy day).

## Status: v1 LIVE at https://preagi.ai

- Apex `preagi.ai` → Vercel production (Valid)
- `www.preagi.ai` → 308 → `preagi.ai` (Valid)
- `preagi.vercel.app` → Vercel production (Valid)
- GitHub: `github.com/riskfreemyth/preagi` (public, auto-deploy from `main`)
- Verified externally: 200 on apex, 308 on www, HTML and OG meta render

## Done

- [x] Domains registered on Porkbun: `preagi.ai` (primary), `preagi.dev` (parked)
- [x] Email forwarding: `hello@preagi.ai` → `avinashgopinathan6@gmail.com`
- [x] Astro 6 + Tailwind v4 scaffold at `~/code/preagi/`
- [x] v1 sections: Hero, Socials, HowIWork (4 principles after trim), ViewsOnAI
- [x] Editorial design system (Fraunces + Inter + JetBrains Mono, warm bg, burnt-orange accent, system dark/light)
- [x] `gh` CLI installed + authenticated as `riskfreemyth`
- [x] Pushed to GitHub on `main`
- [x] Vercel project connected to GitHub, auto-deploy on `main` push
- [x] DNS at Porkbun:
  - `A @ → 216.198.79.1` (apex to Vercel)
  - `CNAME www → 1d4b65179256b230.vercel-dns-017.com` (www to Vercel)
  - Deleted Porkbun's parking `CNAME *.preagi.ai → pixie.porkbun.com`
  - Kept email records (MX fwd1/fwd2.porkbun.com, SPF TXT)

## Open / next session

- [ ] **Copy review on Hero.astro and ViewsOnAI.astro** — both still in v1 form, drafted from persona file. ViewsOnAI is the high-leverage one (the section Parag would actually read). Hero is a one-liner; quick.
- [ ] **Mobile + desktop eyeball pass** on live URL
- [ ] **Lighthouse audit** — target ≥ 90 across all four categories. Run via Chrome DevTools or `npx lighthouse https://preagi.ai --view`
- [ ] **Git author config** — current commits show `Cova Benu <covabenu@Covas-Mac-mini.local>`. Run:
  ```
  git config --global user.name "Avinash Gopinathan"
  git config --global user.email "<github-noreply or real email>"
  ```
- [ ] **OG image** — currently no `og:image` meta. Worth adding for link previews on Twitter/LinkedIn/iMessage.

## Decisions banked (don't relitigate)

- Domain: `preagi.ai` primary (apex canonical), `preagi.dev` parked.
- Stack: Astro + Tailwind + Vercel (no Next.js, no Framer).
- v1 = single landing page, four sections. Everything else lives in `IDEAS.md` until built.
- No photo on hero (text-only is on-brand).
- No dark/light toggle in v1 (system pref only).
- Email: `hello@preagi.ai`.
- Deploy flow: push to `main` on GitHub → Vercel auto-deploys. No manual deploy step needed.

## How to recover after a machine restart

```bash
cd ~/code/preagi
claude --resume      # or: claude (CLAUDE.md auto-loads, then read this file)
npm run dev          # local preview at localhost:4321
```

Tell Claude: *"Read HANDOFF.md and pick up from there."*
