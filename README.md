# DeflationaryBTC (DBTC)

<p align="center">
  <img src="DBTC_logo.png" alt="DBTC Logo" width="150"/>
</p>

<h1 align="center">DeflationaryBTC (DBTC)</h1>
<p align="center">
  Next-Generation Deflationary Token & Ecosystem on Polygon
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT"></a>
  <a href="https://soliditylang.org"><img src="https://img.shields.io/badge/Solidity-0.8.20-blue.svg" alt="Solidity"></a>
  <a href="https://book.getfoundry.sh/"><img src="https://img.shields.io/badge/Built%20With-Foundry-orange.svg" alt="Foundry"></a>
  <a href="https://polygon.technology/"><img src="https://img.shields.io/badge/Network-Polygon-8247e5.svg" alt="Polygon"></a>
  <img src="https://img.shields.io/badge/Audit-Verified-brightgreen" alt="Audit Status">
</p>
---

## 📖 Overview
**DeflationaryBTC (DBTC)** is an advanced ERC20 smart contract deployed on the **Polygon Mainnet**, designed to integrate **deflationary economics, staking, long-hold incentives, and automated liquidity mechanisms**.  
It is not a simple token but a **full-featured protocol** aimed at balancing scarcity, utility, and community-driven incentives.

**Deployed Contract:**  
[`0xB0Bf4C35dCF8E47F9b61C5b07B0cadd2945544E7`](https://polygonscan.com/address/0xB0Bf4C35dCF8E47F9b61C5b07B0cadd2945544E7)

**📄 Whitepaper:**  
[Download DBTC Whitepaper v1.0 (September 2025)](https://dwjcrypto.com/pdf/DBTC_Whitepaper_v1.0.pdf)

### Key Design Goals
- **Scarcity through burns** – Supply reduction continues annually until the hard cap of 21M tokens is reached.  
- **Sustainability through fees** – Every transfer collects fees that are redistributed across the ecosystem.  
- **Incentivized holding & staking** – Rewards are aligned with long-term holding and staking.  
- **DAO governance ready** – DAO address can update governance parameters.  
- **Security-first** – Based on OpenZeppelin standards with `Ownable2Step`, `ReentrancyGuard`, and `Pausable` for safety.

---

## ✨ Core Features
- 🔒 **Staking & Long Holding:** Users can lock tokens (6 or 12 months) and earn proportional rewards.  
- 💧 **Liquidity Provider Incentives:** Automated redistribution for LP contributors.  
- 💰 **Fee Redistribution System:**  
  - 2% transaction fee → redistributed across stakeholders.  
  - **60%** Liquidity Providers  
  - **30%** Long Holders  
  - **10%** Stakers  
- 🔥 **Annual Burn:** Once per year, up to **50% of the supply exceeding the cap** is burned automatically until the target supply is reached.  
- 🛑 **Emergency Controls:** Contract can be paused/unpaused by the owner for risk mitigation.

---

## ⚙️ Tokenomics
- **Token Name:** DeflationaryBTC  
- **Symbol:** DBTC  
- **Decimals:** 18  
- **Initial Supply:** `2,000,000,000 DBTC`  
- **Final Supply Cap:** `21,000,000 DBTC`  
- **Fee on Transfers:** 2%

---

## 🛠️ Development
This project is developed and tested with [**Foundry**](https://book.getfoundry.sh/).

### Install Foundry
```bash
curl -L https://foundry.paradigm.xyz | bash
foundryup

Build
```bash
forge build

Test
```bash
forge test -vv

deploy
```bash
forge script script/Deploy.s.sol --rpc-url $RPC_URL --private-key $PRIVATE_KEY --broadcast

✅ Security & Audit Notes

The contract has been tested and verified against:

✅ Access Control Validation
✅ Reentrancy Attacks
✅ Unchecked Transfer Risks
✅ Precision Loss in Division
✅ Annual Burn Logic
✅ DAO Update Governance Flow

All critical and high-severity issues resolved prior to deployment.

📂 Repository Structure

 ```bash
.
├── src/DBTC.sol              # Main smart contract
├── test/DBTC.t.sol           # Unit tests
├── script/Deploy.s.sol       # Deployment script
├── foundry.toml              # Foundry configuration
├── .github/workflows/ci.yml  # GitHub Actions (CI with Foundry)
└── README.md                 # Documentation

📜 License

MIT License
yaml
