# ⚙️ BeeFi

> Transparent MEL ecosystem on **BNB Chain**  
> Built with open-source smart contracts, sustainable staking design, and long-term token alignment.

---

## 🌐 Overview

**BeeFi** is a BNB Chain-based Web3 ecosystem built around the **MEL Token**.

The current MEL smart contract architecture focuses on:

- Transparent token distribution
- Sustainable staking rewards
- Dedicated reward vault management
- Long-term project/team vesting
- Publicly verifiable on-chain contracts
- Open-source contract code for community review

BeeFi is designed to grow step by step, starting from a secure MEL token foundation and expanding toward staking, community utilities, NFTs, games, and future ecosystem features.

---

## 🧱 Core Smart Contract Architecture

| Contract | Purpose | Status |
|---|---|---|
| **MEL Token** | Fixed-supply ERC20 token for the BeeFi ecosystem | Deployed |
| **MEL Staking** | Dual-vault staking system with fixed and variable APR models | Deployed |
| **MEL RewardVault** | Dedicated MEL reward vault for staking reward distribution | Deployed |
| **MEL Vesting** | Fixed long-term vesting contract for project/team allocation | Deployed |

---

## 🔗 Deployed Contract Addresses

| Contract | Address |
|---|---|
| **MEL Token** | `0xbE46D9bF8b51a16D97018fEa4C63243a1577EB7A` |
| **MEL Staking** | `0x3183842091759Aae2f8C29BFf380df1aB733E4D8` |
| **MEL RewardVault** | `0x797bAcb0d4787e449aaB9b15D4583Dc7B3A226D2` |
| **MEL Vesting** | `0xd73530be7BEC2FC446655FE5FF7F5A725B6eFf63` |

---

## 💎 MEL Token

**MEL** is the core token of the BeeFi ecosystem.

### Token Information

| Item | Details |
|---|---|
| **Token Name** | MEL |
| **Token Symbol** | MEL |
| **Network** | BNB Chain |
| **Total Supply** | 800,000,000 MEL |
| **Token Standard** | ERC20 |
| **Permit Support** | EIP-2612 |

### Token Design

The MEL Token contract uses a fixed-supply model.  
The full token supply is minted once at deployment, and there is no hidden minting mechanism.

Key features include:

- Fixed total supply
- EIP-2612 Permit support
- Owner-controlled batch airdrop function
- Transfer pause mechanism for safety
- Emergency recovery for accidentally sent external tokens
- Direct native coin transfers rejected by default

---

## 📊 Tokenomics

| Category | Allocation | Amount |
|---|---:|---:|
| **Staking Pool** | 30% | 240,000,000 MEL |
| **Sales & Liquidity** | 35% | 280,000,000 MEL |
| **Ecosystem** | 25% | 200,000,000 MEL |
| **Project / Team Vesting** | 10% | 80,000,000 MEL |
| **Total Supply** | 100% | 800,000,000 MEL |

---

## 💰 Staking System

BeeFi uses a **dual-vault staking model** designed to balance accessibility, reward sustainability, and long-term participation.

### 🟢 Free Vault

The Free Vault is designed for flexible staking.

| Feature | Value |
|---|---|
| **APR** | 4% fixed APR |
| **Lock Period** | None |
| **Withdrawal Delay** | 48 hours |
| **Reward Claim** | Available while active |
| **Emergency Withdrawal** | Principal only |

### 🔵 Variable Vault

The Variable Vault is designed for users who prefer higher potential rewards with a longer commitment period.

| Feature | Value |
|---|---|
| **APR Range** | 7% – 19% variable APR |
| **APR Model** | Reference-utilization based |
| **Lock Period** | 52 days |
| **Withdrawal Delay** | 48 hours |
| **Reward Claim** | Available after lock period |
| **Emergency Withdrawal** | Principal only |

The Variable Vault APR is calculated using a fixed reference denominator:

```solidity
totalVariableStaked / REWARD_POOL_BASE
```

This model is designed to reduce excessive reward pressure as variable staking participation grows.

---

## 🏦 RewardVault Design

The **MEL RewardVault** is a dedicated reward vault used to manage staking rewards.

Its purpose is to separate reward storage from staking logic.

Key design points:

- Holds MEL tokens reserved for staking rewards
- Only the owner can fund the vault
- Only the authorized staking contract can release rewards
- Staking contract address can be set only once
- No generic owner withdrawal function for MEL reward tokens
- Non-MEL foreign tokens can be recovered if accidentally sent

This structure is designed to improve transparency and reduce unnecessary reward custody risk.

---

## 🔒 Vesting Design

The **MEL Vesting** contract manages the project/team allocation.

| Item | Details |
|---|---|
| **Total Vesting Allocation** | 80,000,000 MEL |
| **First Vesting Time** | 2026-10-25 11:45:00 KST |
| **First Tranche** | 5,000,000 MEL |
| **Regular Tranche** | 2,500,000 MEL |
| **Vesting Frequency** | Quarterly |
| **Final Vesting Time** | 2034-04-25 11:45:00 KST |
| **Admin Controls** | None |
| **Beneficiary Only Claim** | Yes |

The vesting schedule is fixed at deployment and cannot be modified later.

There is no owner, no admin pause, and no MEL recovery path in the vesting contract.  
This creates a strong long-term alignment structure for the project/team allocation.

---

## 🛡 Security & Transparency

BeeFi prioritizes transparent and security-focused development.

All currently deployed core MEL contracts are:

- Deployed on BNB Chain
- Publicly available on GitHub
- Designed with OpenZeppelin-based security patterns
- Structured with clear NatSpec documentation
- Built using custom errors and explicit validation
- Reviewed with SolidityScan security analysis

### SolidityScan Scores

| Contract | SolidityScan Score |
|---|---:|
| **MEL Token** | 93.65 |
| **MEL Staking** | 92.15 |
| **MEL RewardVault** | 96.23 |
| **MEL Vesting** | 97.34 |

Security scores are not a guarantee of zero risk.  
However, they reflect BeeFi's commitment to transparent, reviewable, and security-focused smart contract development.

---

## 🧩 Technical Principles

BeeFi smart contracts follow several core engineering principles:

- Clear separation of responsibilities
- No unnecessary upgrade complexity
- Conservative reward custody design
- Transparent token allocation
- Fixed vesting logic for long-term alignment
- Emergency withdrawal paths for staking users
- Explicit rejection of direct native coin transfers
- Open-source code for independent community review

---

## 🧭 BeeFi Philosophy

BeeFi is built around a simple principle:

> Sustainable growth is more important than short-term hype.

The project aims to build a transparent Web3 ecosystem where users can verify contract logic, token allocation, staking rules, and reward structures directly on-chain.

BeeFi starts with MEL on BNB Chain and will continue expanding step by step.

---

## 🔗 Official Links

| Platform | Link |
|---|---|
| **Website** | TBA |
| **X / Twitter** | https://x.com/bnbeefi |
| **BNB Chain Explorer** | https://bscscan.com/token/0xbE46D9bF8b51a16D97018fEa4C63243a1577EB7A |
| **GitHub** | TBA |

---

## ⚠️ Disclaimer

BeeFi is an experimental Web3 project.  
Smart contracts, DeFi systems, and digital assets involve risk.

Users should review all available information, verify contracts independently, and make their own decisions before interacting with any blockchain-based system.

---

## Built on BNB Chain. Designed for transparent growth.
