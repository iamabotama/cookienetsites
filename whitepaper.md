# Cookie Chain ($COOK) Tokenomics White Paper

**Version 3.0**
**Date:** July 3, 2026
**Last Updated:** July 3, 2026 (all balances as of July 3, 2026 UTC; sources: cookiescan.io, Solscan, Squads dashboard, Cookiequads dashboard)

## Official Links
- Website: https://cookiechain.wtf
- Investor site: https://invest.cookiechain.wtf
- Explorer: https://cookiescan.io
- Bridge (Hyperlane, instant): https://hyperlane.cookiescan.io
- Legacy escrow bridge: deprecated July 10, 2026 (do not send funds)
- Ecosystem: https://cookiechain.wtf/ecosystem
- Docs: https://docs.cookiechain.wtf
- DAS API: https://api.cookiescan.io
- Community Multi-Sig (Cookie Chain side): https://sig.cookiechain.wtf (Cookiequads, Squads v4 protocol)
- Community Multi-Sig (Solana side): https://app.squads.so/squads/DoYYCtcG2vfrE3HtxBBXiNVieMutvWBXsgbF3SKtYCyx/home
- Solana CA (sCOOK): 36ZrtQoab5MhhySaP1YSTwUahSk6GRVUTtZ6cuVfm9e1
- Official email: community@cookiechain.wtf
- Twitter/X: @TheCookieChain
- Telegram: t.me/TheCookieNetChain

## Executive Summary

Cookie Chain is a high-performance, community-operated Solana Virtual Machine (SVM) Layer 1 blockchain. The chain has been producing blocks since well before its public debut; as of July 12, 2026 it has processed over 35 million transactions across more than 12.2 million slots, secured by a validator set of 7 (4 currently active, all running Agave 3.1.13), with 12,528 wallets holding COOK on-chain. The public debut on May 26, 2026 launched $COOK together with a live two-way bridge to Solana.

$COOK was minted with a supply of 1,000,000,000 and can never be minted again (mint authority permanently revoked at creation). Holders on the legacy chain received cCOOK (the native Cookie Chain representation) at genesis through a snapshot distribution. Their exits are guaranteed by an equity reserve of sCOOK (the Solana-side SPL representation) that the project purchased and locked in a community multi-sig on Solana. As of July 3, 2026, user exit claims are backed at approximately 110% by locked reserves.

Cookie Chain's bridge is the **Hyperlane Warp Route**: instant, automated, collateral-type transfers, live since July 3, 2026 and out of beta since July 6, 2026. The original community-operated escrow bridge served from launch (May 26) until it was **deprecated on July 10, 2026**; all transfers now run through Hyperlane. The equity reserve backing genesis holders remains locked under multi-sig custody and is unaffected by the deprecation.

$COOK is listed on CoinGecko as both a token (coingecko.com/en/coins/cookie-2) and a chain ecosystem.

## 1. Background & Genesis

### 1.1 Origin

Cookie Chain is a community-led hard fork of the Gorbagana chain, built from a surviving backup snapshot after the original chain was halted under single-operator control. The community that built the ecosystem chose continuity: same chain history, new community-controlled future.

### 1.2 Genesis Snapshot Distribution

On May 3, 2026, a snapshot was taken of all on-chain wallet balances (snapshot ID: genesis-snapshot-20260503). Cookie Chain's May 26, 2026 launch used this snapshot as its genesis state:

1. The full supply of 1,000,000,000 cCOOK was minted at genesis into the Community Controlled Wallet (Vault 0). No further minting is possible.
2. Every wallet in the snapshot was credited cCOOK proportionally out of Vault 0. This genesis distribution totaled exactly **279,862,165.78 cCOOK** (~27.99% of supply).
3. Operational vaults were funded under multi-sig control as described in Section 3.

**Key point: the community supply on Cookie Chain did not arrive through the bridge. It was a genesis distribution honoring legacy holders.** All post-genesis movement between chains occurs via the bridges described in Section 3.3.

### 1.3 Backing the Genesis Holders

Genesis holders received cCOOK without depositing anything on Solana, so the project created an equity reserve to guarantee their exit path:

- $COOK launched on Solana (sCOOK) on May 26, 2026 via Pump.fun (Token-2022 program) with an initial mint of 1,000,000,000. Mint authority and freeze authority were set to null in the creation transaction; the supply can only decrease. Current on-chain total supply is 999,960,246.09 after small burns associated with bonding-curve mechanics.
- The project acquired sCOOK on the open market and via developer allocation and deposited it into the Solana community multi-sig lock vault, sized to back the full 279,862,165.78 genesis claim base.
- The team additionally acquired 100,000,000 sCOOK (10%) and deposited it into the same lock vault. That deposit was bridged: 100,000,000 cCOOK was released chain-side into Vault 2 ("Baked Reserve"), reserved for LST/validator staking rewards. The corresponding 100M sCOOK remains locked on Solana as the bridge deposit backing Vault 2. It moves only by multi-sig approval and is never used for bridge settlement.

This purchased-and-locked reserve is what makes the legacy bridge an **equity bridge**: genesis-holder exits are paid from reserves the project bought, not from newly minted tokens.

## 2. Token Overview

| Property | Value |
|---|---|
| Name / Ticker | Cookie Chain ($COOK) |
| Initial mint | 1,000,000,000 (no further minting possible; mint & freeze authority null) |
| Current total supply (Solana) | 999,960,246.09 |
| Decimals (sCOOK) | 6 (Token-2022) |
| Native form | cCOOK on Cookie Chain (SVM L1) |
| Solana form | sCOOK, SPL Token-2022, CA: 36ZrtQoab5MhhySaP1YSTwUahSk6GRVUTtZ6cuVfm9e1 |
| Canonical listing asset | sCOOK on Solana |
| Utility | Gas, staking and LST rewards, bridging, dApp ecosystem |
| Listings | CoinGecko (token + chain ecosystem) |

### 2.1 One Asset, Two Representations

$COOK exists as two mirrored representations: cCOOK native to Cookie Chain and sCOOK on Solana. They are not two separate supplies. Bridge reserves keep the user-accessible supply anchored, as reconciled in Section 3.4. cCOOK held in Vault 0 is the undistributed mirror of sCOOK circulating on Solana; sCOOK held in the Solana lock vault is the reserve backing cCOOK circulating on Cookie Chain.

## 3. Token Allocation, Bridge Mechanics & Supply Reconciliation

### 3.1 Wallet Allocation (as of July 3, 2026)

**Cookie Chain side (cCOOK) — vaults under 6-of-10 community multi-sig (Cookiequads):**

| Wallet | Address | Balance (cCOOK) | % | Role |
|---|---|---|---|---|
| Vault 0 "Bridge Vault" | `G3mm95M4ns7mk8oseWGJnirvgyMahMz3vZEUhdJn8oGX` | 577,222,435.93 | 57.72% | Undistributed reserve; source of cCOOK for bridge entries; destination on exits |
| Vault 1 "Cookie Jar" | `568tU9FMksJDxjkLBjWisSA4J4C5uPH87NCCkyREwrxe` | 30,900,000.80 | 3.09% | Community treasury: donations from community app protocol fees; funds builder incentives, dev support, hackathon rewards |
| Vault 2 "Baked Reserve" | `HXV5qzn7fezEifX7BYx13Z8Yi5wZvpUcgm5fQ1gfE5m3` | 100,879,769.20 | 10.09% | LST/validator staking rewards; backed 1:1 by the 100M sCOOK team deposit locked on Solana |
| Vault 3 (reserved) | `AEMq4AZiGU2smZJX4Y3hqrSmAocGJzBAyvNDWSQeQ4Xe` | 0 | 0% | Unused |
| Bridge operations wallet (legacy, deprecated Jul 10) | `BTUTiNcsrYFCsmAxQN4diwp7JT8cobthygR4vV5bnr2D` | 1,088,035.49 | 0.11% | Working wallet of the deprecated escrow flow; residual float pending wind-down |
| Hyperlane collateral (Cookie Chain side) | `CL2JoQ5jdTpRNKshWhaTihuooT4qrKdLUiPsqKj3yAKz` | 2,543,348.53 | 0.25% | Warp route collateral pool |
| Genesis & community holders | distributed (12,528 wallets hold COOK) | 287,366,410.05 | 28.74% | Genesis distribution (279,862,165.78) plus net post-genesis bridge entries |

Chain-side total: **1,000,000,000.00 ✓**

**Solana side (sCOOK) — total on-chain supply 999,960,246.09:**

| Wallet | Address | Balance (sCOOK) | Role |
|---|---|---|---|
| Community Multi-Sig Lock Vault (Squads "Cookie Community") | `DoYYCtcG2vfrE3HtxBBXiNVieMutvWBXsgbF3SKtYCyx` | 415,697,219.14 | Equity reserve + team deposit backing Vault 2 + user bridge deposits. **Excluded from circulating supply** |
| Hyperlane collateral (Solana side) | `88q7zoKctwAQRsoTxkMJy95sNE3tntuyEhSrhvR1eZwq` | 1,484,476.47 | Warp route collateral escrow (counted as circulating; operational) |
| Legacy bridge working wallet (deprecated Jul 10) | `BTUTiNcsrYFCsmAxQN4diwp7JT8cobthygR4vV5bnr2D` | 2,077,140.49 | Residual float of the deprecated escrow flow (counted as circulating) |
| DEX Liquidity Pool (PumpSwap) | `DRaDjBfCtCCD2Kb1rzMtom3oDiGnwTu9LBgA7WA4LEzx` | ~117.4M (live: dexscreener.com/solana/DRaDjBfCtCCD2Kb1rzMtom3oDiGnwTu9LBgA7WA4LEzx) | Open-market liquidity; counted as circulating |
| Public sCOOK holders | distributed (315 holders) | remainder | Freely circulating |

### 3.2 Composition of the Solana Lock Vault (415,697,219.14 sCOOK)

| Component | Purpose |
|---|---|
| Equity reserve | Purchased by the project to back the 279,862,165.78 genesis claim base; used exclusively for exit settlement |
| Team deposit backing Vault 2 | 100,000,000 sCOOK: the bridge deposit corresponding to the 100M cCOOK in Vault 2. Never used for bridge settlement |
| User bridge deposits | sCOOK deposited by users entering Cookie Chain via the legacy bridge |

Note on the 100M: this allocation exists once, represented on both chains. The sCOOK sits locked on Solana; the corresponding cCOOK sits in Vault 2 chain-side. It is excluded from circulating supply (inside the lock vault) and counted once.

### 3.3 How the Bridge Works

The bridge system has two remaining layers, both publicly auditable, plus one retired flow:

**Hyperlane Warp Route (the bridge):** instant, automated, collateral-type transfers, live July 3, 2026 and out of beta July 6, 2026. COOK is locked in the collateral pool on the sending chain and a relayer delivers 1:1 COOK from the destination pool within seconds. Collateral addresses: `CL2JoQ5j...yAKz` (Cookie Chain) and `88q7zoKc...eZwq` (Solana). Bridge UI: https://hyperlane.cookiescan.io

**Custody layer:** identical 10-member community multi-sigs on both chains (Squads on Solana, Cookiequads on Cookie Chain) hold the reserves: the Solana lock vault and Vault 0. The equity reserve continues to back user-held cCOOK exactly as before; the bridge transition changed the transfer path, not the backing.

**Legacy escrow bridge (deprecated July 10, 2026):** the original flow — deposit to the working wallet (`BTUT...nr2D`) with a destination memo, manual multi-sig-governed settlement in 12-24 hours — operated from launch on May 26, 2026 until its deprecation on July 10, 2026. It has been retired in favor of the instant Hyperlane route; funds should not be sent to it. Residual operational float in the working wallet is being wound down.

No tokens are minted or burned in bridge operation; the fixed supply changes custody.

### 3.4 Supply Reconciliation (as of July 3, 2026)

Every token is in a named bucket at a single timestamp:

**Cookie Chain side:** 577,222,435.93 (Vault 0) + 30,900,000.80 (Vault 1) + 100,879,769.20 (Vault 2) + 0 (Vault 3) + 1,088,035.49 (bridge ops) + 2,543,348.53 (Hyperlane collateral) + 287,366,410.05 (user-held) = **1,000,000,000.00**

**Exit backing test:** user-held cCOOK claims of 287,366,410.05 vs. available backing of 315,697,219.14 (lock vault 415,697,219.14 minus the 100M Vault-2 deposit) = **~109.9% backed**, with a further ~3.6M sCOOK of bridge operational float as buffer.

Note: the Solana-side total supply (999,960,246.09) is marginally below the 1B cCOOK mirror due to ~39,754 sCOOK burned in launch bonding-curve mechanics; the difference is absorbed by the over-collateralization margin.

### 3.5 Circulating Supply Methodology

The canonical listed asset is sCOOK on Solana. For market data aggregators:

> **Circulating Supply = Solana total supply − Community Multi-Sig Lock Vault balance**
> **= 999,960,246.09 − 415,697,219.14 = 584,263,026.95** (as of July 3, 2026)

Excluded address:
- `DoYYCtcG2vfrE3HtxBBXiNVieMutvWBXsgbF3SKtYCyx` (Squads lock vault: equity reserve, team deposit backing Vault 2, legacy-bridge user deposits)

This is the same methodology CoinGecko independently applies to $COOK. The figure includes sCOOK in the open-market DEX pool, consistent with standard aggregator treatment, and conservatively counts the small operational balances (Hyperlane escrow ~1.5M, legacy bridge float ~2.1M) as circulating. The excluded balance is readable in real time on any Solana explorer, making the figure reproducible by any third party at any moment. Chain-side vaults are cCOOK reserves that mirror Solana-side supply and are not part of the sCOOK calculation; they are disclosed in Section 3.1 for full transparency. Because cCOOK in user hands is backed by sCOOK locked in the excluded vault, supply is counted once across both chains.

## 4. Governance & Security

- **Structure:** identical 10-member community multi-sig on both chains (same signer public keys), threshold 6 approvals. Solana side runs on Squads Protocol; Cookie Chain side runs Cookiequads, a deployment of the Squads v4 protocol on Cookie Chain.
- **Permissions:** all 10 signers propose, vote, and execute on the Solana side. On the Cookie Chain side all 10 vote; proposal initiation and execution are held by a subset of signers as an operational safeguard.
- **Membership is dynamic by design.** Signers are added and removed by on-chain proposal; the current member set and threshold are always visible live at the multi-sig links above, which are the source of truth. This document states the configuration as of July 3, 2026: 6-of-10.
- **Track record:** a full on-chain proposal and config history on both chains, including a member-removal proposal rejected by vote — evidence that approvals are not automatic.
- **Future:** phased transition toward broader DAO governance.

**Precedents:** equity/reserve models like WBTC, stablecoin bridges, and early chain migrations.

## 5. Token Utility & Economics

- Gas fees on Cookie Chain
- Staking & LST rewards (funded from Vault 2 "Baked Reserve"; validator set of 7, 4 active, as of July 12, 2026)
- Bridging (Hyperlane, instant)
- dApp ecosystem: Cookoven, CandyShop, CookieSwap, CookieBox, BakedBazaar, gorboy, and community programs funded via Vault 1 "Cookie Jar"

## 6. Risk Factors

Holding or bridging $COOK involves significant risk. The following factors are disclosed so holders can evaluate the system on complete information.

### 6.1 Bridge & Custody Risk

**Reserve custody:** reserves are held by community multi-signature wallets rather than autonomous smart contracts. All releases require 6-of-10 signer approval on coordinated multi-sigs. Security of custodied funds depends on the integrity, independence, and key security of the signer group; compromise or collusion of six signers could move reserve funds without authorization.

**Hyperlane route:** live since July 3, 2026 (out of beta July 6). Hyperlane protocol security assumptions (validator set / relayer configuration) apply to in-flight transfers; collateral pools hold only operational amounts (~4M COOK combined as of July 3).

**Legacy escrow flow (deprecated July 10, 2026):** the retired flow's working wallet is a single-signer hot wallet holding a small residual float pending wind-down; reserves were never held there and remain under multi-sig custody.

**Validator concentration:** as of July 12, 2026 the network runs 4 active validators with stake concentrated among a small operator set; validator onboarding and stake distribution are active workstreams (see the live set at cookiescan.io/validators).

**Mitigations and context:**
- Every custodied wallet is publicly identified in Section 3.1 and auditable in real time; unauthorized movement would be immediately visible.
- Each vault has a single defined purpose, and vault outflows occur only via public multi-sig proposals.
- The signer group consists of long-standing community members whose involvement predates the public launch. Membership changes are executed transparently on-chain.
- The Hyperlane route removed custodial settlement from day-to-day transfers; the legacy flow's deprecation on July 10, 2026 completed that migration.

### 6.2 Market Risk

$COOK trades with limited liquidity concentrated in a single DEX pool (PumpSwap COOK/SOL, ~$27K liquidity as of July 3, 2026). Prices can move significantly on small orders. Verify pool depth before transacting.

## Document History

- **v3.1 (July 13, 2026):** Legacy escrow bridge recorded as deprecated (July 10); Hyperlane beta exit (July 6) recorded; Hyperlane established as the sole transfer path; validator set stated precisely (7 total, 4 active, Agave 3.1.13); network statistics refreshed through July 12; risk section updated (validator concentration added, escrow risk retired). Balance reconciliation remains as of July 3, 2026.
- **v3.0 (July 3, 2026):** Full single-timestamp reconciliation; genesis figure fixed at 279,862,165.78; dual-bridge architecture documented; governance corrected to 6-of-10; on-chain token facts verified (6 decimals, Token-2022, authorities null); circulating supply methodology aligned with CoinGecko.
- **v2.0 (June 5, 2026):** Tokenomics restatement for aggregator listings.
- **v1.0 (May 2026):** Initial publication.

## Glossary

- **$COOK**: The native utility token of Cookie Chain. Used for gas fees, staking, bridging, and ecosystem activity.
- **sCOOK**: Solana-side representation of $COOK (Pump.fun-launched Token-2022 SPL token, 6 decimals).
- **cCOOK**: Native Cookie Chain-side representation of $COOK.
- **Genesis Snapshot Distribution**: The launch-day crediting of 279,862,165.78 cCOOK to all snapshot wallets in proportion to their balances.
- **Equity Bridge (legacy bridge)**: The original community-operated escrow bridge (manual settlement, 12-24h), backed by the purchased sCOOK reserve. Operated May 26 - July 10, 2026; now deprecated.
- **Hyperlane Warp Route**: The instant collateral-type bridge, live July 3 and out of beta July 6, 2026; since the legacy bridge's deprecation on July 10, 2026, the sole transfer path between Cookie Chain and Solana.
- **Equity Reserve**: sCOOK purchased by the project and locked in the Solana multi-sig to back the genesis claim base of 279,862,165.78.
- **Vault 0 "Bridge Vault"**: Main pre-minted reserve on Cookie Chain (`G3mm...oGX`).
- **Vault 1 "Cookie Jar"**: Community treasury vault funded by community app protocol-fee donations (`568t...wrxe`).
- **Vault 2 "Baked Reserve"**: LST/validator staking rewards vault (`HXV5...E5m3`), backed 1:1 by the 100M sCOOK team deposit locked on Solana.
- **Bridge Operations Wallet**: Working wallet of the deprecated legacy escrow flow (`BTUT...nr2D`); residual float pending wind-down.
- **Solana Lock Vault**: Squads vault holding the equity reserve, the team deposit, and legacy-bridge user deposits (`DoYY...YCyx`).
- **Multi-Sig**: Community governance requiring 6 approvals from the 10-member signer set (as of July 3, 2026), via Cookiequads and Squads.
- **LST**: Liquid Staking Token for staking rewards on Cookie Chain.

## Conclusion

Cookie Chain's genesis snapshot honored every legacy holder with exactly 279,862,165.78 cCOOK, and the purchased equity reserve backs their path out at approximately 110% as of this writing. With the Hyperlane bridge live and the legacy escrow flow retired as of July 10, 2026, all transfers are instant and automated, while reserves remain under identical 10-member multi-sig governance on both chains with fully public wallet addresses. The model provides verifiable user protection with a clear path toward broader decentralization.

**This is not financial advice. DYOR and verify on cookiescan.io.**
