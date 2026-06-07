# Working with Claude on KHR_Adventures

A reference for how you and Claude collaborate on this project — workflow, code
review process, and the originality guardrails that keep this "inspired by KHR,
not a clone."

## Project shape (from the scaffold)

This is a Rojo place project (`default.project.json`):

- `src/client` — client-side scripts (`init.client.luau`)
- `src/server` — server-side scripts (`init.server.luau`)
- `src/shared` — modules shared between client and server (`Hello.luau`)
- `stylua.toml` / `selene.toml` — formatting and linting config (run before
  committing; Claude will run these as part of review)
- Build with `rojo build -o "KHR_Adventures.rbxlx"`, live-sync with `rojo serve`

As systems get designed (Phase 1+), this is where their code will land — combat
in a shared module consumed by both sides, hub interactions split across
client/server, etc.

## Workflow

- **Naming convention — `<ticket_number>-<short_feature_description>`**:
  applies to branches, PR titles, and commit subject lines alike, e.g.
  `4-map-slateburgh-districts`, `7-script-suzu-awakening-scene`. Keeps every
  piece of work traceable straight back to its tracking issue on the project
  board (issue #4 in the example above is "Map Slateburgh's districts and
  design the resonant site").
- **Branches**: one feature branch per ticket, named per the convention above.
  Branch off `master`.
- **Commits**: small and focused — one logical change per commit, subject line
  follows the naming convention, body explains *why* not just *what*.
- **Pull requests**: open a PR before merging anything into `master`. Title
  follows the naming convention; link it to its tracking issue (`Closes #N`).
- **Merging**: nothing lands in `master` without going through review first.

## Code review — "teach me as we go"

You're still building your review instincts, so for each PR Claude will:

1. **Summarize** what changed and why, in plain language first.
2. **Walk the diff** section by section rather than dumping a verdict.
3. **Explain the reasoning** behind any suggestion — not just "change this to
   that," but *why* it matters (so the lesson transfers to the next PR).
4. **Call out Roblox/Luau-specific things to watch for**, e.g.:
   - Client-server trust boundaries (never trust client input on the server;
     validate everything that comes through a RemoteEvent/RemoteFunction)
   - Connection cleanup (disconnecting `RBXScriptConnection`s to avoid leaks,
     especially in things that get created/destroyed repeatedly)
   - Performance hot paths (avoid heavy work in `RenderStepped`/`Heartbeat`
     loops, expensive operations inside loops over players/parts)
   - DataStore practices (retries, throttling, not saving on every small change)
5. **Flag anything risky** explicitly (security, performance, data loss) so it
   doesn't get lost in a sea of style nits.

Over time the goal is for you to start spotting these things yourself —
Claude will name the *pattern*, not just the instance, so it's recognizable
next time.

## Project board & tasks

- Tracked via GitHub Issues + a Project board (columns: **Backlog → To Do →
  In Progress → In Review → Done**).
- Each phase from the roadmap becomes a milestone/epic; concrete work becomes
  individual issues underneath it.
- Suggested labels: `phase:0-concept`, `phase:1-gdd`, `phase:2-foundation`, …,
  `area:client`, `area:server`, `area:shared`, `area:design`, `type:bug`.
- PRs reference the issue they close so the board stays in sync automatically.

## Originality guardrails (run this checklist for any new character, power, or
piece of lore before it gets built)

- [ ] Name is distinct from any KHR character, group, item, or named technique
- [ ] Visual design (silhouette, color palette, signature prop) reads as its
      own thing next to the show's equivalent
- [ ] Backstory/motivation is original, even where the *role* in the story
      rhymes with a KHR character's role
- [ ] No direct quotes, catchphrases, or unique terminology lifted from the show
- [ ] If a mechanic is structurally similar (e.g. "typed power + companion +
      gear"), the *presentation* — naming, lore, visual theme — is built from
      scratch (see the power-system brainstorm in the planning notes)

Keep a running list of "things that are too close, don't reuse" as they come up
— it's easier to course-correct early than to redesign something the team has
already built around.

## Session conventions

- Claude won't write game code until the relevant design is settled (GDD before
  building). If a request jumps ahead of where the design stands, Claude will
  flag the gap rather than guess.
- For anything that touches shared/external state — pushing branches, opening
  PRs, creating/editing the GitHub Project board — Claude will confirm with you
  first.
