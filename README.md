# TOWER — $TOWER holder city

Single-file website: `index.html`. No build step. Upload to GitHub Pages / Netlify / Vercel, or open it directly.

Every $TOWER holder gets a building. Height = $TOWER held (1 floor per `tokensPerFloor`). Fee stake = holdings ÷ eligible supply.

## Launch-day setup (CONFIG at the top of the script)
- `tokenCA`  → the $TOWER mint. Switches the city from PREVIEW (demo data) to LIVE on-chain data.
- `feeWallet` → the public wallet that receives creator fees. Its SOL balance is shown as the fee vault.
- `excludeOwners` → IMPORTANT: add the pump.fun bonding curve (and later the LP / AMM pool), plus team/fee wallets,
  otherwise the bonding curve shows up as the tallest "holder" and stakes are diluted.
- `rpcUrl` → use your own RPC (Helius, QuickNode…). The public endpoint rate-limits.
- `tokensPerFloor`, `maxFloors`, `holderSharePct`, `creatorFeePct`, `distribution` text.
- `buyUrl`, `chartUrl` (xUrl is set to https://x.com/Towerprojectsol).

## What the site does / doesn't do
- Reads balances, top holders, supply and the fee wallet balance from Solana (read-only).
- Never holds or sends funds. Distributions must be sent by you from the fee wallet, on the schedule you post on X.

`game-version.html` is the earlier stacking-game version, kept in case you want it on a /play page.
