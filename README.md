# Dojo

**Pet Dojo Training** — Clicker / idle gym: pets hit dummies to raise base stats under a daily cap.

Part of the [ComputerPets](https://github.com/RicheyWorks/computerpets) universe. Map: [computerpets-ecosystem](https://github.com/RicheyWorks/computerpets-ecosystem).

> Status: **design scaffold**. Gameplay contract is frozen. Engine choice is the one in the brief. Implementation comes next.

## Loop

Without a cap this becomes pay-or-click-forever. Dojo is the honest grind: small, capped, visible on the overlay as 'trained today'. Arena, Siege, Horde all read these numbers.

## Genre & engine

- Genre: **Idle clicker**
- Engine: **Svelte**
- Stack: Svelte 5 · idle tick · dummy targets · writes into overlay base stats with daily caps
- Default surface: `5173`

## How you play

1. Park a pet on a dummy.
2. Click for burst XP, idle for drip.
3. Daily cap per stat (shown).
4. Overcap XP converts to flavor steam, not power.

## Talks to

- computerpets (base stats)
- computerpets-arena
- computerpets-siege
- computerpets-horde
- computerpets-quests

## Failure doctrine

Bot clicks → exponential decay. Cap bypass attempt → reject write. Overlay offline → queue the day's remaining cap, apply on sync.

Canon rules that never yield:

- 210 living kinds. No illegal hybrids.
- Overlay pets can get tired, sick, or hide. Tokens are not burned by a minigame.
- Desktop walk stays the main quest. Closing Dojo must leave Rui walking.

## Layout

```
computerpets-dojo/
  README.md
  LICENSE
  docs/DESIGN.md
  src/                implementation lands here
```

## Run (Windows)

```powershell
cd app; npm install; npm run dev
```

Meet Rui first via the [flagship start-here](https://github.com/RicheyWorks/computerpets/blob/main/docs/START-HERE.md). This game is optional.

## License

MIT. See [LICENSE](LICENSE).

---

*Two hundred ten living kinds. Keep them so a line does not go quiet.*
