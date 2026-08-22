# MMK Wallet Addon — v1.5.0 Changelog

Main file: `MMK_Wallet_Addon_v1.5.0.mcaddon` (update of v1.4.0).
Requires Minecraft Bedrock 26.30+ (@minecraft/server 2.8.0).

## Bug fixes
1. **Wallet item looked like a gold ingot** — the item used the vanilla
   `gold_ingot` icon. It now uses its own wallet texture
   (`items/wallet.json` -> `"minecraft:icon": "wallet"`).
2. **Sneak + use wallet got stuck in Creative** — sneak + use now TOGGLES:
   once = real creative menu, sneak + use again = back to Survival.
3. **Sell Items button/menu reworked** — the old dropdown flow is replaced
   by a full menu (see below).

## New features
### Sell Items — new rarity menu
- Shows everything sellable in your inventory, grouped and colored by
  rarity: **Common (white) -> Uncommon (green) -> Rare (aqua) ->
  Epic (pink) -> Legendary (gold) -> Mythical (purple)**.
- **Search bar** to find items by name.
- Sell any amount of one item, or **Sell EVERYTHING** in one tap.
- New top prices / rarest items: **Dragon Egg = 10,000,000 MMK** (highest
  price in the bank), plus Beacon, Conduit, Dragon Head, Sniffer Egg,
  Netherite Upgrade Template and more.

### Leaderboard + titles
- `/mmktop` and the wallet menu now show the richest players (online AND
  offline), ranked.
- Money titles with custom icons: Villager -> Hustler -> Wealthy ->
  **Millionaire** -> Multi-Millionaire -> Tycoon -> **Billionaire**.
- Each player's title is displayed **above their head** (name tag).

### Item Price Check (on/off switch)
- Toggle in the main menu. While ON, holding any item shows its bank price
  and rarity state (common white -> mythical purple) on the action bar.

### GUI modes (main menu + all sub menus)
- **Dark**, **Light** and **20% Transparent (Glass)** looks. Bedrock forms
  cannot change their real window background, so each mode re-skins titles,
  colors, dividers and buttons across every menu. Saved per player.

### About
- Telegram account text is now **yellow**.

### Creator features (MaouKhatana only)
- **Disco name tag** — the creator's name tag cycles through moving
  rainbow colors, with a ★ CREATOR ★ title.
- **Instant Structures item** (`mmk:structures`) — use it to browse all
  141 structures (Houses, Castles, Farms, Trees, Platforms, Statues...)
  and place them instantly where you look (rotation/mirror options).
  - No crafting recipe.
  - Hidden from the creative menu (no menu category).
  - Only MaouKhatana ever receives it; anyone else holding it gets it
    confiscated.
- **"Always on you" guardian** — if the wallet or the structures item is
  dropped, the ground copy is deleted and a fresh one returns to the
  owner's inventory. The structures item can never be lost.

## Notes
- `/give` command autocomplete is controlled by the game engine, so the
  structures item id can still be typed there — but there is no recipe, no
  creative-menu entry, and the script confiscates it from everyone except
  MaouKhatana.
- Structure files come from the Instant Structures reference pack and load
  under the `mystructure:` namespace inside `MMKWallet_BP/structures/`.
