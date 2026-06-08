# Multiplayer Structure — Shared World, Personal Story

> Status: **Direction locked** (Phase 0). Exact unlock pacing, technical
> implementation (server architecture, instancing mechanism), and systemic
> content design are deferred to Phase 1+ — this doc captures the *shape*
> the rest of the design builds on.

## Why this doc exists

Multiplayer was the founding vision for this project — but building the
narrative around a KHR-inspired structure naturally pulled in KHR's own DNA:
a single chosen protagonist, a personal mentor bond, a found family that
orbits one specific person. That's a Persona-shaped story wearing a
Roblox-shaped engine, and the two don't reconcile on their own.

This doc is the reconciliation: **keep the personal story exactly as
designed, and build the multiplayer experience as a layer that runs alongside
it rather than fighting it.**

## The two layers

### Layer 1 — the shared world (multiplayer from minute one)

Slateburgh's everyday districts — school, downtown, residential blocks,
parks — are the persistent, shared social space. Other players are
*physically present* here: you see them, cross paths with them, party up,
hang out. This is where the "even mix, swings both ways" tone lives day to
day (slice-of-life, side content, casual social play), and it doubles as a
quiet thematic payoff: you're sharing the same ordinary streets with dozens
of other players, and — per the "hidden world" framing — most of them read as
just townsfolk... except some of them are wielders living through their *own*
version of this same story, same as you.

### Layer 2 — the personal story (instanced)

Your awakening, your bond with Salvatore, your found-family arc with Raphael
and Wren — these phase you into a private instance where *you* are the one
whose Resonance just cracked open, the one Salvatore made a promise about,
the one drawing faction attention. This is where the emotional intimacy of
everything in [[character-roster]] and [[setting-and-factions]] survives
completely untouched — no other player's presence dilutes "this is happening
to *you*."

### How players move between them

You start in the shared layer (everyday Slateburgh, established friendships
with Raphael and Wren already in place), then **phase into instanced story
beats as they trigger** — the awakening, Salvatore's entrance, key
found-family moments — before being handed back to the shared world, now
carrying your power, to keep adventuring alongside other players who are each
living their own version of the same arc.

## NPC visibility — fully authored, but not invisible to the world

Raphael, Wren, and Salvatore stay **fully authored NPCs** — their
personalities, arcs, and relationships to you are exactly as designed in
[[character-roster]], not randomized or player-driven. But they're not
locked away in your instance either:

- **They appear as recognizable figures in the shared world** — you might
  spot Salvatore across the street in downtown Slateburgh, or run into
  Raphael causing a scene at school, even outside your own instanced story
  beats. This makes Slateburgh feel *lived-in* and cohesive rather than like
  a hub full of strangers, while your *personal* relationship with each of
  them still plays out privately, instanced, on your own terms.
- **Friends can "guest" in each other's personal-story instances** — a
  real-life friend can tag along during your awakening scene, your first
  meeting with Salvatore, or a found-family beat, as a participant rather
  than a spectator. This is the single biggest lever for making the personal
  story *feel* multiplayer without compromising its "this is happening to
  you" core — you get to share the most important moments of your story with
  the people you actually play with.

## Shared end-game content — light gate, systemic design

Rather than story-locking shared content behind personal-arc completion (which
fragments friend groups who progress at different paces) or fully decoupling
it (which raises the question of why an unawakened Suzu would be exploring
hidden-world content they have no in-fiction reason to access), the plan is a
**middle path**:

- **Gate on a single, early, near-universal milestone: the awakening itself**
  — not full personal-arc completion. Once you've awakened, you've "earned"
  a place in the hidden world, and that's enough justification to belong in
  shared adventure content regardless of how far you've gotten with Salvatore
  or the found-family arc.
- **Design shared content to be systemic, not plot-driven** — combat, faction
  operations, resonant-site exploration, loot/progression. Built this way, it
  runs *alongside* personal stories instead of requiring them to be at any
  particular point, and carries zero risk of spoiling or stepping on anyone's
  personal-story beats. The split becomes clean: personal story = "how you
  got your power and who it made you," shared world = "what you do with it."

### The resonant site & Carthage — the natural shared end-game space

[[setting-and-factions]] already frames the resonant site as a
"hidden/late-game-unlocked area" and Carthage's ruins as "the central mystery
The Conclave chases" — which makes it tailor-made to *be* this shared
end-game space. Every awakened wielder, regardless of where they are in their
personal arc, can converge here to explore the same buried civilization
together — and personal-story discoveries can feed pieces of the Carthage
mystery into what the shared space gradually reveals, so solo narrative
discovery and group exploration reinforce each other instead of living in
separate boxes.

## Decisions still open (track in Phase 1+)

- [ ] Exact unlock pacing/requirements for "the awakening" milestone (how
      early, how much setup before a player reaches it)
- [ ] How guesting works mechanically — can a guest actively participate in
      your instanced story beats, or are they limited to certain kinds of
      involvement (combat support vs. dialogue/cutscene presence, etc.)?
- [ ] Which parts of Slateburgh's everyday spaces are fully shared vs.
      lightly instanced (e.g., is the school itself a shared space, or do
      certain interior/story-relevant areas phase per-player?)
- [ ] How faction systems manifest in the shared layer (reputation, territory
      control, PvP, faction-vs-faction content?)
- [ ] Pacing/safeguards for how the Carthage mystery unfolds across both
      layers without players spoiling discoveries for each other
