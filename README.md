# FH6 DynoLab v1.0

A dyno & tuning workbench for Forza Horizon 6 car data.

DynoLab does no decryption or rencrytion, Decrypt `gamedbRC.slt` with this tool -> https://github.com/DVS-code/Forza-Crypto-Tool
## How to use
1. Download `FH6 DynoLab.exe` below
2. Click **Load decrypted gamedb…** and pick your decrypted `gamedbRC.slt`.
3. Pick a car, choose an option, edit, and hit **Confirm Edit** to save.
4. Re-encrypt the database with your crypto tool.
5. Wait for patcher

Edits only save when you press Confirm. Leaving a card without confirming discards the changes.

## Cards
- **Tuning** — engine build with per-part tiers, power multiplier, live dyno graph
- **Engine Swapper** — swap in any of 647 engines (presets or any car's engine) with exhaust sound preview
- **Suspension** — ride height, springs, damping, camber, anti-roll bars (with m→in)
- **Transmission** — gear ratios, final drive, shift time, live speed-per-gear + shift points
- **Tires** — width, aspect, wheel size, compound, pressure, traction (mm↔in)
- **Weight & Balance** — curb weight, front/rear bias, live power-to-weight
- **Brakes** — front/rear brake strength & balance
- **Aero / Downforce** — downforce & drag scale with top-speed tradeoff
- **Drivetrain** — convert FWD / RWD / AWD
- **Engine Character** — backfire, fuel tank, rotary/diesel flags, sound preview

## Notes
- All dyno math is derived from real game data and cross-checked against the game's own stats.
- Edits are non-destructive and written only to the database file you load.
- Some engines are shared between cars — editing engine character affects every car using that engine (shown in-app).
