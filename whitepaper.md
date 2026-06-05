# Cookie Chain ($COOK) Tokenomics White Paper

**Version 1.3**  
**Date:** June 5, 2026  
**Last Updated:** June 5, 2026  

## Official Links
- Website: https://cookiechain.wtf
- Explorer: https://cookiescan.io
- Bridge: https://bridge.cookiescan.io
- Docs: https://docs.cookiechain.wtf
- Community Multi-Sig (Cookie Chain side): https://cookiequads.vercel.app/community (and https://sig.cookiechain.wtf)
- Solana Multi-Sig (Squads): https://app.squads.so/squads/DoYYCtcG2vfrE3HtxBBXiNVieMutvWBXsgbF3SKtYCyx
- Solana CA (sCOOK): 36ZrtQoab5MhhySaP1YSTwUahSk6GRVUTtZ6cuVfm9e1
- Twitter: @TheCookieChain
- Telegram: t.me/TheCookieNetChain

## Executive Summary

Cookie Chain is a high-performance, community-operated Solana Virtual Machine (SVM) Layer 1 blockchain — a hard fork from Gorbagana designed for transparency, low fees, and fair legacy token migration.

$COOK has a fixed total supply of 1,000,000,000 tokens. The tokenomics feature an equity-backed bridge model where a pre-minted Community Controlled Wallet serves as the reserve for 1:1 distributions as users bridge from Solana. This protects trapped value from the legacy chain.

The structure is governed by community multi-sigs on both sides and is transitional — with plans to migrate to a Hyperlane bridge for native burn/mint mechanics.

## 1. Introduction & Background

Gorbagana faced challenges leading to trapped ("gulag") tokens. Cookie Chain was launched as a community hard fork on May 26, 2026 to preserve the ecosystem while providing a fair migration path.

To back legacy holders, the project acquired ~27% supply initially (now dynamic equity reserve) via Pump.fun and developer intervention, creating a fully backed equity bridge.

## 2. Token Overview

- Ticker: $COOK
- Total/Max Supply: 1,000,000,000 (fixed, fully pre-minted)
- Decimals: 9
- Native on Cookie Chain SVM; bridged sCOOK on Solana
- Primary Utility: Gas, bridging, staking, dApps

Current bridged volume: ~398M COOK (as of latest explorer data).

## 3. Token Allocation & Distribution

The following table provides a clear breakdown of the main wallets that power the Cookie Chain ecosystem and equity bridge:

| Wallet Type                        | Side          | Address                                      | Approx. Balance | % of Supply | Primary Role |
|------------------------------------|---------------|----------------------------------------------|-----------------|-------------|--------------|
| Community Controlled Wallet / Vault 0 | Cookie Chain | `G3mm95M4ns7mk8oseWGJnirvgyMahMz3vZEUhdJn8oGX` | ~590M          | ~59%       | Pre-minted reserve for equity bridge distributions |
| Bridge Reserve Wallet              | Cookie Chain | `BTUTiNcsrYFCsmAxQN4diwp7JT8cobthygR4vV5bnr2D` | ~17.2M         | ~1.72%     | Dedicated bridge liquidity and claims support |
| LST / Staking Rewards Wallet       | Cookie Chain | `HXV5qzn7fezEifX7BYx13Z8Yi5wZvpUcgm5fQ1gfE5m3` | ~101M          | ~10.1%     | Distribution of staking rewards |
| Solana Multisig / Lock Wallet      | Solana       | `DoYYCtcG2vfrE3HtxBBXiNVieMutvWBXsgbF3SKtYCyx` | N/A (locks sCOOK) | N/A        | Controls Solana-side locking for bridging |

**Equity Bridge Mechanics**:
- When users bridge sCOOK from Solana, it is locked in the Solana Multisig wallet.
- Equivalent cCOOK is released from the Community Controlled Wallet (Vault 0) to the user's Cookie Chain address.
- This dynamic equity model maintains full 1:1 backing.
- All operations governed by community multi-sig (6-of-11 threshold).

**Remaining Supply**: ~29% is distributed across community holders, DEX liquidity pools, and ecosystem incentives. All movements are transparent and auditable via the multi-sig dashboards.

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

## Glossary

- **$COOK**: The native utility token of Cookie Chain. Used for gas fees, staking, bridging, and ecosystem activity.
- **sCOOK**: Solana-side version of $COOK (Pump.fun launched token).
- **cCOOK**: Native Cookie Chain-side version of $COOK.
- **Equity / Lock-Unlock Bridge**: The current 1:1 community multi-sig bridge. sCOOK is locked on Solana; equivalent cCOOK is released from the reserve on Cookie Chain (see allocation table above).
- **Community Controlled Wallet / Vault 0**: Main pre-minted reserve on Cookie Chain (`G3mm95M4ns7mk8oseWGJnirvgyMahMz3vZEUhdJn8oGX`).
- **Bridge Reserve Wallet**: Dedicated Cookie Chain wallet for bridge liquidity (`BTUTiNcsrYFCsmAxQN4diwp7JT8cobthygR4vV5bnr2D`).
- **Solana Multisig / Lock Wallet**: Controls locking of sCOOK on Solana (`DoYYCtcG2vfrE3HtxBBXiNVieMutvWBXsgbF3SKtYCyx`).
- **Multi-Sig**: Community governance system (6-of-11 threshold) using Cookiequads and Squads for transparent control of key wallets and bridge operations.
- **Hyperlane Bridge**: Planned upgrade for native burn/mint mechanics, reducing reliance on equity reserves.
- **LST**: Liquid Staking Token for staking rewards on Cookie Chain.
- **Gulag Supply**: Legacy trapped tokens from Gorbagana that the equity bridge helps unlock.

(See the **Token Allocation & Distribution** table above for visual reference to the main wallets.)

## Conclusion

The equity bridge and multi-sig model provide strong user protection during migration while planning for greater decentralization. All verifiable on-chain.

**This is not financial advice. DYOR and verify on cookiescan.io.**

---
*This is the living draft. Additional sections/details will be expanded as more info is provided.*