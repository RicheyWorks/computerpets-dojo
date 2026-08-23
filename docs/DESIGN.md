# Dojo design

Implement against this file, not folklore.

## Identity

- Product: **Dojo**
- Repo: `computerpets-dojo`
- Idea: Pet Dojo Training
- Genre: Idle clicker
- Engine: Svelte
- Surface: `5173`

## Loop

Without a cap this becomes pay-or-click-forever. Dojo is the honest grind: small, capped, visible on the overlay as 'trained today'. Arena, Siege, Horde all read these numbers.

## Play beats

- Park a pet on a dummy.
- Click for burst XP, idle for drip.
- Daily cap per stat (shown).
- Overcap XP converts to flavor steam, not power.

## Neighbors

- computerpets (base stats)
- computerpets-arena
- computerpets-siege
- computerpets-horde
- computerpets-quests

## Failure doctrine

Bot clicks → exponential decay. Cap bypass attempt → reject write. Overlay offline → queue the day's remaining cap, apply on sync.

## Hard rules

1. Minigames cannot mint or burn NFTs by themselves (Minter is the write path).
2. Stats come from lived overlay care + Dojo caps, not cash shop.
3. Species kits stay inside Lore. Illegal hybrids never spawn.
4. Fail soft: the desktop overlay process is not this process.
