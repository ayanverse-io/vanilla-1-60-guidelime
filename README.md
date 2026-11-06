# vanilla-1-60-guidelime

Open-source 1–60 leveling guides for **WoW Classic Era / Forever**, in
[Guidelime](https://github.com/max-ri/Guidelime) format. Two addons, both factions,
one in-game UX: step list with auto check-off, map waypoints, and a navigation arrow.

## Status

| Pack | Coverage | State |
|---|---|---|
| `Guidelime_Alliance_1_60` | 12–60 (40 blocks) | ✅ usable now |
| | 1–12 (starting zones) | 🚧 planned |
| `Guidelime_Horde_1_60` | 1–60 | 🚧 planned |

## Install

1. Install **Guidelime** (CurseForge/Wago). It is required and *not* bundled.
2. Copy (or junction) `Guidelime_Alliance_1_60` and/or `Guidelime_Horde_1_60` into
   `World of Warcraft\_<flavor>_\Interface\AddOns\`.
3. Restart the game fully, enable both addons, then `/guidelime` and pick a guide
   from the **"Alliance 1-60 (Custom)"** / **"Horde 1-60 (Custom)"** group.
4. If the addon shows as out of date on your client, tick "Load out of date AddOns".

```powershell
# Windows: link instead of copy (keeps the repo as source of truth)
New-Item -ItemType Junction -Path "C:\...\Interface\AddOns\Guidelime_Alliance_1_60" `
  -Target "C:\path\to\vanilla-1-60-guidelime\Guidelime_Alliance_1_60"
```

## What's inside

Each guide block covers one zone visit of the classic speed-leveling route:

- **Alliance 12–30**: Darkshore → Loch Modan → Redridge → Darkshore → Ashenvale →
  Stonetalon → Darkshore → Ashenvale → Wetlands → Redridge → Duskwood
- **Alliance 30–40**: Wetlands → Ashenvale → Hillsbrad → Arathi → STV →
  Shimmering Flats → Desolace → STV → Alterac → Arathi → Dustwallow → STV
- **Alliance 40–50**: Badlands → Swamp of Sorrows → STV → Desolace → Tanaris →
  Feralas → Azshara → Hinterlands → STV → Searing Gorge → Feralas → Dustwallow → Tanaris
- **Alliance 50–60**: Hinterlands → Blasted Lands → Un'Goro → Azshara → Felwood →
  Winterspring → Felwood → Burning Steppes → WPL → EPL → WPL → Kalimdor mop-up →
  Silithus → EPL → Winterspring

Blocks chain automatically via `[NX]` tags. Steps carry real vanilla quest IDs, so
accept/complete/turn-in auto-tracks. Hub-level waypoints only — this is a
"where to be and which chains to run" guide, not a per-mob coordinate guide.
`[O]` marks group/escort/tough-solo steps.

## Content policy

- All routing text is **original** to this project.
- Quest names/IDs and zone layout are **Blizzard game data** (facts), the same data
  any quest database exposes. This project contains **no** content from commercial
  guide products (no text, files, or decrypted data).
- The zone sequence follows publicly available route information cross-checked
  against public guides.

## Roadmap

- [ ] Alliance 1–12 (Elwynn / Dun Morogh / Teldrassil)
- [ ] Horde 1–30 and 30–60
- [ ] Quest-name labels audited against in-game DB display
- [ ] Per-step coordinates for elite/escort targets
- [ ] Dungeon quest-callout blocks (ZF, ST, BRD)

## Contributing

Guides are plain text with Guidelime tags — see any `Guides*.lua` for the pattern.
Fix wrong quest IDs/coords, add missing chains, or port a Horde block.
Please keep the content policy: original text + game facts only.

## License

[MIT](LICENSE)
