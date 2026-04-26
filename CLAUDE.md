# preagi — Project Context

This file auto-loads when Claude Code starts in `~/code/preagi/`. It's the project's long-lived memory. For "what's the current state of play," see `HANDOFF.md` instead.

## What this is

Personal website for **Avinash Gopinathan** at `preagi.ai`. Three jobs: (1) public home for thoughts and views, (2) about-me page (short and long), (3) sales page strong enough that a corporate reader walks away wanting to hire or work with him. Specific reader on the radar: **Parag (CEO/founder, Parallel AI)** — long-term ambition is to mirror Parallel AI's split between a human-facing site and an agent-facing site.

## Domains

- **`preagi.ai`** — primary, live (or about to be). Bought on Porkbun.
- **`preagi.dev`** — defensive, parked on Porkbun. Future home for code/projects subsite or the agent endpoint.
- **`preagi.com`** — was unavailable at registration time.

Email: `hello@preagi.ai` → forwards to `avinashgopinathan6@gmail.com` (set up in Porkbun).

## Stack

- **Astro 6** + Tailwind CSS v4 + TypeScript (strict)
- Static-first build, deployed to **Vercel** via GitHub auto-deploy
- Fonts: Fraunces (display/serif), Inter (body), JetBrains Mono (accents) — loaded from Google Fonts
- Color theme: warm off-white / near-black, single burnt-orange accent (`#b8472d` light, `#e07a5f` dark). Respects system dark/light pref. No toggle in v1.
- Layout: single-column, `max-w-2xl` (672px) reading column

## File map

```
~/code/preagi/
  CLAUDE.md             # this file — project context
  HANDOFF.md            # current session state, blockers, next actions
  IDEAS.md              # running roadmap (Now / Next up / Eventually / Long-term agent)
  README.md             # default Astro readme (low signal)
  astro.config.mjs      # Astro + Tailwind vite plugin
  package.json
  src/
    pages/
      index.astro       # composes the four sections
    layouts/
      Base.astro        # html shell, meta tags, OG, fonts, max-w container
    components/
      Hero.astro        # name + role + one-liner
      Socials.astro     # X, IG (cooktochef + covathehova), podcast, email
      HowIWork.astro    # 7 distilled operating principles
      ViewsOnAI.astro   # 5-paragraph essay
    styles/
      global.css        # @import tailwindcss + @theme tokens + small custom layer
  public/
    favicon.svg         # black square, "ag" in burnt orange
```

## Voice and copy

- **Direct, blunt, no sycophancy.** Avinash's CLAUDE.md spells this out. Skip warmth-buffers and praise-padding in any copy we write for the site.
- **Operator's voice, not marketer's voice.** Sales-page energy without smelling like a marketing page.
- **First-person.** "I" not "we" — this is a personal site.
- **Editorial pacing.** Short paragraphs, white space, no headers stacking on headers.
- **Don't re-explain things.** Audience is fluent in fintech, AI, startup tech. Calibrate up.

## Development workflow

```bash
npm run dev      # http://localhost:4321
npm run build    # static build to ./dist
npm run preview  # serve the build locally
```

When making changes:
1. Edit components in `src/components/` (one section per component).
2. `npm run build` to catch issues early; build is fast (<1s).
3. Commit on `main`. Vercel auto-deploys on push.
4. Update `HANDOFF.md` if you're stopping mid-task.
5. Update `IDEAS.md` when ideas land or items ship.

## Reference

- **Parag / Parallel AI** — long-term inspiration for the human/agent split. Not the audience for v1; the audience for v2+ is.
- **Patrick Collison's site, Brian Lovin's site, Sam Lambert's site** — design references. Editorial, fast, text-led.
- **Avinash's global CLAUDE.md** at `~/.claude/CLAUDE.md` — has the full persona (operating principles, energizers, drainers, working preferences). Read it for tone calibration.
