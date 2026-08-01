# OD9 Labs — Claude Onboarding

You are working in **od9-labs**, the collaboration sandbox for the OD9 community.
This file is written for *any* contributor's Claude — read it fully before your
first change; it replaces weeks of context.

## What OD9 is (60 seconds)

OD9 ("Off Da Nine") is a community and framework for advancing humanity toward
Type I civilization status by solving **coordination failures** — founded by
The Ultimate Rage (Chicago). The public surface is **offda9.com** + a Discord
community running the **ASCEND Protocol**: a five-tier progression system
(Observer → Theorist → Architect → Pioneer → Benefactor) where members earn
credits through presence and **dimensions only through verified work** —
completed lessons, reviewed contributions, shipped projects.

That last part matters here: **work merged from this repo is exactly the kind
of verified contribution the ladder counts.** A contributor pairing with their
Claude to ship something real is the mission working as designed — human-AI
collaboration is the HOW of the whole project.

## What this repo is — and is not

**IS:** community-built tooling — Game Night helpers, scoreboard pages, small
CLIs, web components, art/QA scripts. Self-contained things a member and their
Claude can design, build, and PR.

**IS NOT:** the OD9 Discord bot, the offda9.com deploy tree, or anything with
credentials. Those live elsewhere and nothing here connects to them. This
boundary is absolute:

- **No secrets, keys, tokens, or `.env` values — ever.** Not in code, not in
  commits, not in issue text. If a project seems to need one, it needs a
  redesign instead: emit files/JSON that a maintainer imports on their side.
- **No member data.** No Discord IDs, usernames, emails, or scraped content.
  Test data is invented data.
- **Nothing here talks to production.** No webhooks at offda9.com, no bot
  endpoints, no databases. Deliverables are static pages, scripts, and data
  files a maintainer reviews and wires up on the other side of the wall.

## How work flows

1. **Pick an issue** (or open one proposing an idea and wait for a 👍 from a
   maintainer before building big).
2. **Branch** from `main`: `yourname/short-slug`.
3. **Build small and self-contained.** Prefer zero dependencies: plain Python
   3.12 stdlib, or a single static HTML file with inline CSS/JS. If you need a
   dependency, name it in the PR description and keep it pip-installable.
4. **PR with a real description**: what it does, how you tested it, one
   screenshot if it renders anything. Your Claude wrote it? Great — say so,
   that's the point. You still reviewed it before pushing.
5. A maintainer (the founder or their Claude) reviews and merges.

## Conventions

- **Python**: 3.12, stdlib-first, `pathlib` over `os.path`, every file opens
  with `encoding="utf-8"`. Scripts get a `--dry-run` flag if they write
  anything and a docstring saying what they do and why.
- **Web**: single-file static HTML unless agreed otherwise. Must look right on
  a phone. OD9 brand feel: near-black backgrounds (`#0A0A0A`), electric blue
  `#00BFFF`, cyan `#00FFF7`, gold `#FFD700`, crimson `#FF1744` as accent —
  dark, high-contrast, a little cinematic.
- **Docs**: every project directory carries a `README.md` — what it is, how to
  run it, what's unfinished. Write the WHY into comments, not just the what.
- **Honesty over polish**: a PR that says "X works, Y is stubbed, Z is untested"
  is a good PR. Claiming done what isn't done is the one unforgivable sin here —
  OD9's whole epistemics are built on verified claims.

## Tone

Direct, warm, zero corporate voice. The community says "pull up," means it,
and reads receipts. Have fun with it — this repo exists because building
things together IS the community.
