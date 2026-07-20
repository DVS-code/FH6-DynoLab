# FH6 DynoLab

A dyno & tuning workbench for Forza Horizon 6 car data.

DynoLab can work two ways: edit a **decrypted database file** offline, or read and write the **live running game** directly. In offline mode DynoLab does no decryption or re-encryption — decrypt and re-encrypt `gamedbRC.slt` with this tool -> https://github.com/DVS-code/Forza-Crypto-Tool

## How to use

Pick a mode on the launch screen:

### 📄 Offline (file)
1. Download `FH6 DynoLab.exe` from the latest release (or run the installer).
2. Click **Offline (file)** and pick your decrypted `gamedbRC.slt`.
3. Pick a car, choose a card, edit, and hit **Confirm Edit** to save.
4. Re-encrypt the database with your crypto tool.
5. Wait for patcher.

### ⚡ Runtime (live game)
1. Start Forza Horizon 6.
2. Launch DynoLab and click **Runtime (live game)** — it reads the database straight out of the running game (no decrypt/encrypt needed).
3. Edit as normal, then hit **⬆ Push to game** to apply your changes to the live game instantly.

Edits only save when you press Confirm. Leaving a card without confirming discards the changes.

## Cards
- **Tuning** — engine build with per-part tiers, power multiplier, live dyno graph, and a **+ tier** button to add a brand-new upgrade level to any engine part
- **Engine Swapper** — swap in any of 647 engines (presets or any car's engine) with exhaust sound preview
- **Transmission** — edit gear ratios, final drive, shift time, live speed-per-gear + shift points, **or swap in any gearbox** (Swap tab) by DrivetrainID
- **Differential** — LSD accel/decel lock (front/rear/center) and AWD power split
- **Clutch** — friction and engage/release timing
- **Boost Tuning** — turbo/supercharger peak-boost scale, off-boost floor, and high-RPM taper
- **Electric Motor** — EV power multiplier, redline and battery, with a live motor dyno
- **Suspension** — ride height, springs, damping, camber, anti-roll bars (with m→in)
- **Tires** — width, aspect, wheel size, compound, pressure, traction (mm↔in)
- **Weight & Balance** — curb weight, front/rear bias, live power-to-weight
- **Brakes** — front/rear brake strength & balance
- **Aero / Downforce** — downforce & drag scale with top-speed tradeoff
- **Drivetrain** — convert FWD / RWD / AWD
- **Grip & Assists** — surface traction and lateral/longitudinal grip scalars
- **PI & Class** — set performance index and car class
- **Catalog & Rarity** — cost, rarity, autoshow visibility, speed limiter
- **Engine Character** — backfire, fuel tank, rotary/diesel flags, sound preview

## Notes
- All dyno math is derived from real game data and cross-checked against the game's own stats.
- Offline edits are non-destructive and written only to the database file you load. **Back up your database before editing.**
- Engine exhaust sounds are **bundled in the app**, so the ▶ preview works with no game files present. When a decrypted DB sits next to the real game audio, the exact per-car clip is used.
- Swaps are self-consistent: an engine or transmission swap automatically brings that engine/gearbox's upgrade tiers and dyno with it — nothing to migrate.
- Some engines are shared between cars — editing engine character affects every car using that engine (shown in-app). All other edits are scoped to per-car / per-engine / per-drivetrain rows so they don't bleed between cars.
- **Runtime (live game) mode is Windows-only and version-specific.** It finds the game's live database by memory signature for the current FH6 build; if the game updates it fails cleanly rather than corrupting anything. May require running as administrator, and injects into the game process (avoid on online / anti-cheat-sensitive play).

