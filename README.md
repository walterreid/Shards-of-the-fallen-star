## Shards of the Fallen Star (v0.7)

Arcade roguelite micro-platformer built with Phaser 3. Collect shards, defeat the boss, and escape before the world collapses.

### Play
- Open `index.html` in a modern desktop browser, or serve the folder locally to enable clipboard features.
  - Recommended: `python3 -m http.server 8080` then visit `http://localhost:8080`
  - Or: `npx serve --single --listen 8080` then visit `http://localhost:8080`

### Controls
- Movement: WASD / Arrow Keys
- Jump: Space (traits can grant extra jumps)
- Sprint: Shift
- Shoot: Left‑Click (hold to charge if you find the charging trait)
- Blink: Right‑Click (if you get the blink trait)
- Pause: P
- Restart Run: R

### Game Loop
1. Crash on the islands and collect 3 shards.
2. Fight the boss that spawns after the final shard.
3. When the collapse begins, reach the ship before the timer hits zero.

### Menu & Options
- Seed: Enter a custom seed or leave blank for a random run.
- Continue Last Seed: Re-run with your last seed.
- Daily Challenge: Uses the current New York date for a shared daily seed.
- Options (P → Options panel): toggle SFX, screen shake, and difficulty (Normal/Hard).

### Traits (v0.7)
There are 30 traits plus the unlockable Starlight Veil; each run grants random traits from the pool as you collect shards. Examples:
- Movement: Pulsebound, GravityFavor, AuroraStep, ZephyrChain, Magnetstride, VoidSkater
- Offense: StarforgedEdge, CometFury (charge shots), Shatterwake, EchoAncients, Flarefang, Blightbite
- Defense: Prismheart, IronBloom, SpecterBreath, AegisLoop, SolarHunger, LamentCore
- Utility: OrreryWhisper, TemporalVeil, WraithDebt, EclipserEye, AuricKey, ChronoDrift
- Risk–Reward: BloodBloom, HungerEngine, ShardEater, StormPact, FrostVein, GlassSoul

Unlocks tracked in localStorage:
- Starlight Veil: Gain brief i‑frames on shard pickup (unlocks at 6 lifetime shards).
- Crystal Biome: Added to biome rotation after 3 wins.

### Run Codes
At the end of a run, a Base64 run code appears in the summary. Copy to share your run data (seed, mode, biome, boss, difficulty, time, traits, result). Import is not implemented; codes are for sharing only.

### Tech
- Phaser `3.60.0` via CDN.
- Single‑file implementation in `index.html` using Phaser Arcade Physics.
- Local storage keys: `sfs_meta_v07`, `sfs_last_seed_v07`, `sfs_options_v07`.

### Troubleshooting
- Clipboard buttons (Copy Seed / Copy Run Code) may require a secure context (HTTPS) or `http://localhost`. If opened via `file://`, clipboard APIs can be blocked; serve with a local web server.
- If performance is low, try disabling screen shake and SFX in the Options panel.

### License
No license specified. Phaser is © Photon Storm Ltd. See Phaser’s license for details.


