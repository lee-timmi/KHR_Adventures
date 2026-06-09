# Anamnesis

A multiplayer Roblox RPG about **Strata Resonance** — power born from
*feeling*, not measured force — set in **Slateburgh**, an unassuming town
sitting on a resonant geological site that's quietly drawn an unusual
concentration of wielders into the hidden world built around it.

> **Naming note**: The repo folder is still named `KHR_Adventures` — the
> placeholder carried over from the project's KHR-inspired origins. Renaming
> the folder/repo is a harder-to-reverse step; it stays until we're ready
> to do it properly.

## Design docs

Phase 0 (concept direction) is locked. Start here for the full picture:

- [`docs/design/power-system.md`](docs/design/power-system.md) — Strata
  Resonance: attribute types, Resonant Echoes, Keepsakes, Harmonic
- [`docs/design/setting-and-factions.md`](docs/design/setting-and-factions.md)
  — Slateburgh, Carthage, the four factions, tone
- [`docs/design/character-roster.md`](docs/design/character-roster.md) — the
  core cast (Suzu, Raphael, Wren, Salvatore)
- [`docs/design/multiplayer-structure.md`](docs/design/multiplayer-structure.md)
  — how the shared world and instanced personal story fit together

See [`WORKING_WITH_CLAUDE.md`](WORKING_WITH_CLAUDE.md) for how this project is
built, reviewed, and tracked.

## Getting Started

This is a [Rojo](https://github.com/rojo-rbx/rojo) place project.

To build the place from scratch:

```bash
rojo build -o "KHR_Adventures.rbxlx"
```

Then open `KHR_Adventures.rbxlx` in Roblox Studio and start the Rojo server:

```bash
rojo serve
```

For more help, check out [the Rojo documentation](https://rojo.space/docs).
