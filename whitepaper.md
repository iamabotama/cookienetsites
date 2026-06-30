# Cookie Chain ($COOK) Tokenomics White Paper

**Version 2.0**
**Date:** June 5, 2026
**Last Updated:** June 5, 2026 (balances as of June 5, 2026, 10:53 AM PT)

## Official Links
- Website: https://cookiechain.wtf
- Explorer: https://cookiescan.io
- Bridge: https://bridge.cookiescan.io
- Ecosystem: https://cookiechain.wtf/ecosystem
- Docs: https://docs.cookiechain.wtf
- DAS API: https://api.cookiescan.io
- Community Multi-Sig (Cookie Chain side): https://sig.cookiechain.wtf
- Community Multi-Sig (Solana Side): https://app.squads.so/squads/DoYYCtcG2vfrE3HtxBBXiNVieMutvWBXsgbF3SKtYCyx/treasury
- Solana CA (sCOOK): 36ZrtQoab5MhhySaP1YSTwUahSk6GRVUTtZ6cuVfm9e1
- Twitter: @TheCookieChain
- Telegram: t.me/TheCookieNetChain

## Executive Summary

Cookie Chain is a high-performance, community-operated Solana Virtual Machine (SVM) Layer 1 blockchain with nine months of on-chain history and 22,000 wallets. Launched May 26, 2026, the project marked its public debut by simultaneously releasing $COOK and a live two-way bridge — opening the ecosystem to Solana and beyond, and inviting the world to move freely in and out for the first time.

$COOK has a fixed total supply of 1,000,000,000 tokens. Holders on the legacy chain received cCOOK (the native Cookie Chain $COOK token) at genesis through a snapshot distribution, and their exits are guaranteed by an equity reserve of sCOOK (the Solana-side SPL $COOK token) that the project purchased and locked in a community multi-sig on Solana. As of June 5, 2026, user exit claims are backed at approximately 100% by locked reserves. All bridge movement in both directions is 1:1, multi-sig governed, and publicly auditable.

The structure is transitional, with a planned migration to a Hyperlane bridge for native burn/mint mechanics.

## 1. Background & Genesis

### 1.1 The Cookie Chain Origin

Cookie Chain has been a functioning SVM ecosystem for nine months, with 22,000 wallets actively participating on-chain. The community built the chain, the infrastructure, and the identity from the ground up — and on May 26, 2026, made it official: $COOK launched alongside a live two-way bridge, giving every wallet holder the ability to move value freely between Cookie Chain and Solana for the first time.

### 1.2 Honoring the Founding Community

On May 3, 2026, a snapshot was taken of all on-chain wallet balances (snapshot ID: genesis-snapshot-20260503). Cookie Chain launched on May 26, 2026 with this snapshot as its genesis state, recognizing every wallet that had been part of the ecosystem:

1. The full supply of 1,000,000,000 cCOOK was minted at genesis into the Community Controlled Wallet (Vault 0).
2. Every wallet in the snapshot was credited cCOOK proportionally, distributed out of Vault 0. This genesis distribution totaled approximately 279,862,165.78 cCOOK (~27.9% of supply) — a direct acknowledgment of the community that built this ecosystem.
3. Project operational wallets (LST Staking Rewards, Bridge Reserve) were funded from Vault 2 at Cookie Chain Multisig Treasury.
4. The remainder stays in Vault 0 as the bridge distribution reserve.

**Key point: the community supply on Cookie Chain did not arrive through the bridge. It was a genesis distribution honoring legacy holders.** The bridge governs all movement between chains after genesis.

### 1.3 Backing the Genesis Holders

Because genesis holders received cCOOK without ever depositing anything on Solana, the project created an equity reserve to guarantee their exit path:

- $COOK was launched on Solana (sCOOK) via Pump.fun with a supply of 1,000,000,000.
- The project acquired approximately 28% of the sCOOK supply (~279M) on the open market and via developer allocation, and deposited it into the community multi-sig lock wallet on Solana. This reserve alone covers the ~279.9M genesis distribution at roughly 100%.
- The team additionally acquired and deposited 10% of sCOOK supply (~100M), reserved for marketing, rewards, and future operational fees. This allocation moves only by 6 of 11 multi-sig approval and is never used for bridge settlement. This supply is now at Cookie Chain Multisig with Vault number of 2.

This 28% equity reserve is what makes the bridge an **equity bridge**: exits by genesis holders are paid from reserves the project purchased and locked, not from newly minted tokens.

## 2. Token Overview

| Property | Value |
|---|---|
| Name / Ticker | Cookie ($COOK) |
| Total Supply | 1,000,000,000 (fixed, no further minting) |
| Decimals | 9 |
| Native form | cCOOK on Cookie Chain (SVM L1) |
| Solana form | sCOOK, SPL token, CA: 36ZrtQoab5MhhySaP1YSTwUahSk6GRVUTtZ6cuVfm9e1 |
| Canonical listing asset | sCOOK on Solana |
| Utility | Gas, staking and LST rewards, bridging, dApp ecosystem |

### 2.1 One Asset, Two Representations

$COOK exists as two mirrored representations: cCOOK native to Cookie Chain and sCOOK on Solana. They are not two separate 1B supplies. The bridge and its reserves keep the user-accessible supply anchored at 1,000,000,000, as reconciled in Section 3.4. cCOOK held in Vault 0 is the undistributed mirror of sCOOK circulating on Solana; sCOOK held in the Solana lock wallet is the reserve backing cCOOK circulating on Cookie Chain.

## 3. Token Allocation, Bridge Mechanics & Supply Reconciliation

### 3.1 Wallet Allocation (as of June 5, 2026)

| Wallet | Side | Address | Balance | % of Supply | Role |
|---|---|---|---|---|---|
| Community Controlled Wallet (Vault 0) | Cookie Chain | `G3mm95M4ns7mk8oseWGJnirvgyMahMz3vZEUhdJn8oGX` | 590,222,436 cCOOK | 59.02% | Undistributed reserve; source of cCOOK for bridge entries; destination for cCOOK on exits |
| LST / Staking Rewards | Cookie Chain | `HXV5qzn7fezEifX7BYx13Z8Yi5wZvpUcgm5fQ1gfE5m3` | 100,879,769 cCOOK | 10.09% | Staking reward distribution |
| Bridge Reserve Wallet | Cookie Chain | `BTUTiNcsrYFCsmAxQN4diwp7JT8cobthygR4vV5bnr2D` | 17,221,221 cCOOK | 1.72% | Bridge liquidity and claims support |
| Genesis & community holders | Cookie Chain | distributed (22,000 wallets) | 279,862,165.78 cCOOK | 27.98% | Genesis distribution to founding community wallets plus post-genesis bridge entries |
| Community Multi-Sig Lock Wallet | Solana | `DoYYCtcG2vfrE3HtxBBXiNVieMutvWBXsgbF3SKtYCyx` | ~392.8M sCOOK | 39.28% | Equity reserve, team allocation, and user bridge deposits (see 3.2) |
| DEX Liquidity Pool | Solana | `DRaD...Ezx` | ~126M sCOOK | ~12.6% | Liquidity pool backing sCOOK trading on Solana DEXs |
| Public sCOOK holders | Solana | distributed | ~481.2M sCOOK | ~48.12% | Freely circulating on Solana |

### 3.2 Composition of the Solana Lock Wallet (39.28%)

The lock wallet balance is not a single category. It consists of:

| Component | Amount | % of Supply | Purpose |
|---|---|---|---|
| Equity reserve | ~270M sCOOK | ~27% | Purchased by the project to back exits by genesis holders. Never used for any other purpose. |
| Team operations allocation | ~100M sCOOK | ~10% | Marketing, rewards, future fees. Locked; moves only by 6-of-11 multi-sig. Bridged into the Cookie Chain and locked in Multi Sig Vault number 2. |
| User bridge deposits | ~22.8M sCOOK | ~2.28% | sCOOK deposited by users entering Cookie Chain since launch |

### 3.3 How the Bridge Works

![Cookie Chain Equity Bridge flow diagram](bridge-flow.svg)

**Entering Cookie Chain (Solana → Cookie Chain)**
1. User deposits sCOOK into the Solana multi-sig lock wallet.
2. An equal amount of cCOOK is released from Vault 0 to the user's Cookie Chain address.

**Exiting Cookie Chain (Cookie Chain → Solana)**
1. User's cCOOK is returned to Vault 0.
2. An equal amount of sCOOK is released from the Solana lock wallet to the user's Solana address.

Every movement in either direction is 1:1 and executed under 6-of-11 community multi-sig control on both sides. No tokens are minted or burned in bridge operation; the fixed genesis supply simply changes custody.

### 3.4 Supply Reconciliation (as of June 5, 2026)

The test of the equity bridge is whether every user-held token has a guaranteed redemption path.

- User-held cCOOK on Cookie Chain (exit claims): **291,676,574** (~268.9M genesis distribution + ~22.8M bridged in)
- sCOOK in the Solana lock wallet available against exits: ~270M equity reserve + ~22.8M user deposits = **~292.8M**
- **Exit backing ratio: ~100.4%**, with the 17.2M cCOOK Bridge Reserve Wallet as additional buffer
- The team operations allocation (~100M sCOOK) and Vault 0 are excluded from user claims and from backing calculations.

Whole-system check: 607.2M circulating sCOOK + 291.7M user-held cCOOK + 100M locked team allocation ≈ 998.9M, reconciling to the 1B fixed supply within the over-collateralization buffer.

All balances are publicly auditable in real time at cookiescan.io/top-holders and on Solana explorers at the addresses above.

### 3.5 Circulating Supply Methodology

The canonical listed asset is sCOOK on Solana. For market data aggregators:

> **Circulating Supply = 1,000,000,000 − Solana Multi-Sig Lock Wallet balance**

Excluded address:
- `DoYYCtcG2vfrE3HtxBBXiNVieMutvWBXsgbF3SKtYCyx` (Solana lock wallet: equity reserve, team operations allocation, and bridge deposits)

Resulting circulating supply: approximately **607,200,000 $COOK** (as of June 5, 2026). This figure includes the ~126M sCOOK held in the DEX liquidity pool, consistent with standard aggregator treatment of open market liquidity.

Chain-side wallets (Vault 0, Bridge Reserve, LST Rewards) are cCOOK reserves that mirror the Solana-side supply and are not part of the sCOOK circulating calculation; they are disclosed in Section 3.1 for full transparency. Because cCOOK in user hands is backed by sCOOK locked in the excluded wallet, supply is counted once across both chains.

## 4. Governance & Security

- Cookie Chain side: 6-of-11 multi-sig
- Solana side: Squads multi-sig with matching members
- Future: Broader DAO

**Precedents**: Equity/reserve models like WBTC, stablecoin bridges, and early chain migrations.

**Transition Plan**: Phased move to Hyperlane Warp Routes for native burn/mint, reducing reserve dependency.

## 5. Token Utility & Economics

- Gas fees on Cookie Chain
- Staking & LST rewards
- Bridge operations
- dApp ecosystem (Cookoven, CookieSwap, BakedBazaar, etc.)

## 6. Risk Factors

Holding or bridging $COOK involves significant risk. The following factors are disclosed so that holders can evaluate the system on complete information. This section will be expanded as the project evolves.

### 6.1 Bridge Custody Risk

The Cookie Chain bridge is operated by community multi-signature wallets rather than autonomous smart contracts. All bridge releases require approval from 6 of 11 signers on coordinated multi-sigs (Cookiequads on Cookie Chain; Squads on Solana). The security of bridged and reserve funds therefore depends on the integrity, independence, and key security of the signer group. Compromise or collusion of six signers could result in unauthorized movement of reserve funds.

**Mitigations and context:**

- Every custodied wallet is publicly identified in Section 3.1 and auditable in real time. Any unauthorized movement would be immediately visible to all holders.
- Each reserve wallet has a single defined purpose. The equity reserve is used exclusively for user exits and the team operations allocation is never used for bridge settlement.
- All 11 signers are long-standing community members with eight to eleven months of continuous involvement predating Cookie Chain's public launch. They are the people who built this ecosystem from the ground up — present since before the token existed, before the bridge was live, before the doors were open. Their tenure is the strongest signal of alignment and accountability the project can offer.
- As the project matures, the signer pool is expected to expand. Any change will maintain the approval threshold above 50% of the pool, so that security scales with the group without increasing the risk of quorum failure. Expanded signer transparency, up to and including verified identities, is under consideration for later phases; specific commitments and timelines will be published as they are made.
- The planned migration to Hyperlane Warp Routes (Section 4) replaces custodial settlement with native burn/mint mechanics, removing this dependency entirely.

## Glossary

- **$COOK**: The native utility token of Cookie Chain. Used for gas fees, staking, bridging, and ecosystem activity.
- **sCOOK**: Solana-side representation of $COOK (Pump.fun launched SPL token).
- **cCOOK**: Native Cookie Chain-side representation of $COOK.
- **Genesis Snapshot Distribution**: The launch-day crediting of cCOOK to all wallets holding $GOR on the legacy chain, in proportion to their snapshot balances (~268.9M cCOOK).
- **Equity Bridge**: The current 1:1 community multi-sig bridge, backed by a purchased sCOOK reserve rather than mint/burn. sCOOK is locked on Solana to enter; cCOOK returns to Vault 0 and sCOOK is released to exit.
- **Equity Reserve**: The ~27% of sCOOK supply purchased by the project and locked in the Solana multi-sig to guarantee exits for genesis holders.
- **Community Controlled Wallet / Vault 0**: Main pre-minted reserve on Cookie Chain (`G3mm95M4ns7mk8oseWGJnirvgyMahMz3vZEUhdJn8oGX`).
- **Bridge Reserve Wallet**: Dedicated Cookie Chain wallet for bridge liquidity (`BTUTiNcsrYFCsmAxQN4diwp7JT8cobthygR4vV5bnr2D`).
- **Solana Multisig / Lock Wallet**: Holds the equity reserve, team operations allocation, and user bridge deposits on Solana (`DoYYCtcG2vfrE3HtxBBXiNVieMutvWBXsgbF3SKtYCyx`).
- **Multi-Sig**: Community governance system (6-of-11 threshold) using Cookiequads and Squads for transparent control of key wallets and bridge operations.
- **Hyperlane Bridge**: Planned upgrade for native burn/mint mechanics, reducing reliance on equity reserves.
- **LST**: Liquid Staking Token for staking rewards on Cookie Chain.
- **Founding Supply**: The cCOOK distributed at genesis to wallets that had been active on Cookie Chain prior to the public launch. Recognized through the genesis snapshot and redeemable 1:1 via the two-way equity bridge.

## Conclusion

Cookie Chain's genesis snapshot honored every legacy holder, and the purchased equity reserve guarantees their path out, backed at over 100% as of this writing. Combined with 6-of-11 multi-sig governance on both chains and fully public wallet addresses, the model provides verifiable user protection during migration while building toward a Hyperlane-based native bridge and broader decentralization.

**This is not financial advice. DYOR and verify on cookiescan.io.**
