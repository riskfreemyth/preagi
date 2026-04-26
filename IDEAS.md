# preagi.ai — Running Ideas

**Domains owned (Porkbun):** `preagi.ai` (primary, live), `preagi.dev` (parked — likely future home for a code/projects subsite or agent endpoint).

The working list of what should eventually live on the site, beyond the v1 landing page. Nothing here is committed; it's a parking lot for ideas Avinash drops in over time. Items get pulled into the site when they're ready, not when they're listed.

## Now (v1, shipping today)

- [x] Hero — name + role + one-line positioning
- [x] Socials — X/Twitter, IG (cooktochef + covathehova), Unfriendly Banter podcast, email
- [x] How I work — distilled operating principles
- [x] Views on AI — short essay

## Next up (v2)

- [ ] Blog/notes — MDX-powered, dated entries, work + life. The publishing engine.
- [ ] "Work with me" page — explicit corporate-facing pitch. What I ship, what I'm looking for next.
- [ ] Music
  - [ ] Spotify playlists: Pump / Mellow / Slow (mode-based)
  - [ ] Carnatic devotional shelf — MS Subbulakshmi, KGA Sudas, etc., with a note on why Carnatic puts the mind at peace
- [ ] Dark/light toggle (v1 respects system pref only)
- [ ] OG image with name + role for link unfurls
- [ ] Plausible or Vercel Analytics

## Eventually

- [ ] Soccer + Unfriendly Banter — podcast page with episodes, YouTube + IG embeds
- [ ] Kobe / Mamba mentality — essay on why and how I embraced it, what it's unlocked
- [ ] Stuttering — life lessons, framed for someone who might find it useful. Stutter is a fact, not a sensitivity.
- [ ] Cova page — Hovawart, turning 5, link to @covathehova
- [ ] Cooking — cross-post from @cooktochef
- [ ] Reading list / influences

## Long-term: the agent version (Parallel-AI-inspired)

The play here, modeled on Parallel AI's split between a human-facing site and an agent-facing site (a "web for agents"):

- [ ] `llms.txt` at the root with a structured bio + section index
- [ ] `/agent` (or `/a`) route serving a text-only/markdown rendering of the entire site
- [ ] `/api/me.json` endpoint with structured profile data (role, focus areas, links, contact)
- [ ] Edge-level user-agent routing so crawlers and agents land on the agent version automatically
- [ ] Schema.org Person structured data on every page

This is the long-term Parag (Parallel AI) hook. Not v2 — v3 or v4 — but the architecture from day one shouldn't close it off.

## How to use this file

When a new idea comes up, drop it in the right bucket. When something ships to the live site, move it under "Now" with a date. Don't delete things from "Eventually" just because they've been there a while — the soccer page might wait two years and that's fine.
