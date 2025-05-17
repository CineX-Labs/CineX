# CineX Token

## Transforming AMC. Redefining Ownership.

CineX is a bold initiative to acquire and modernize AMC through blockchain, immersive technology, and decentralized ownership. This repository contains the core smart contract infrastructure for the CineX Token, the foundational asset powering a new era of audience-driven entertainment.

---

## Overview

CineX is pioneering a new category: decentralized entertainment economies.

We are building a platform that merges:

- Blockchain-native token utility and programmable ticketing  
- Next-gen theater technology, including AR/VR and holography  
- A community-first model of economic participation  

This codebase supports the launch of the CineX Token and the on-chain infrastructure required to upgrade legacy cinema operations and democratize entertainment ownership.

---

## Key Links

- Website: [https://cinex.tech](https://cinex.tech)  
- Whitepaper: [CineX_Whitepaper](/docs/CineX_Whitepaper.md)  
- One-Page Memo: [CineX_Memo.pdf](/docs/CineX_Memo.md)  
- Token Contract: [View on Etherscan](https://etherscan.io/token/0x721562c04324b6751d411fd45e5360bbddaec353)  
- Community: [Join the CineX Discord](https://discord.gg/9yNZU2jU)

---

## Repository Structure
contracts/        # Core Solidity contracts
scripts/          # Deployment and verification scripts
test/             # Test suite
docs/             # Whitepaper, memo, license
README.md         # Project summary

---

## Platform Architecture

- **CineX Token**: ERC20-compatible smart contract with swap fee and cooldown logic  
- **Upgradeable Contracts**: Built using OpenZeppelin proxy pattern  
- **Ecosystem Integration**: Designed for use with both theatrical and digital experiences  

---

## Contract Description

The CINEX contract is an ERC20 token with:

	•	Swap fees
	•	30-second cooldown between transfers
	•	Temporary restrictions on maximum transfer size
 
---

Functions Overview: getFee

	•	Returns: The current swap commission rate.
 
---

setFeeFreeList

	•	Purpose: Exempt specific addresses from fees.
	Inputs:
	•	account: Wallet address
	•	add: true to exempt, false to remove exemption
 
---
setTransferRestrictionFreeList

	•	Purpose: Remove transfer limits for certain addresses.
	Inputs:
	•	account: Wallet address
	•	add: Boolean flag

---
setPoolWithFeeList

	•	Purpose: Designate liquidity pools where swap fees are charged.
	Inputs:
	•	pool: Pool address
	•	add: Boolean flag

---
pause

	•	Effect: Globally halts all token transfers. Only admin.

---

unpause

	•	Effect: Restores token transfers. Only admin.


---

Smart Contracts Upgradeability

The CineX Token uses OpenZeppelin’s upgradeable contract pattern. This ensures:
	•	Seamless upgrades to contract logic without disrupting user balances
	•	Continued extensibility and patching post-deployment
	•	Robust proxy architecture for governance and evolution


 ---

## Licensing and Contribution

This repository is maintained by the CineX Foundation. Contributions are currently closed to the public. All contracts are published for transparency and will be submitted for formal auditing. For security-related disclosures, contact: `contact@cinex.tech`.

---

## Legal Disclaimer

This codebase is for informational and educational purposes only. Nothing in this repository constitutes legal, financial, or investment advice. Use of this software is at your own risk. CineX Foundation and its contributors disclaim all liability for loss or damages arising from use of this codebase. Full disclaimers are available on [cinex.tech/terms](https://cinex.tech/terms).
