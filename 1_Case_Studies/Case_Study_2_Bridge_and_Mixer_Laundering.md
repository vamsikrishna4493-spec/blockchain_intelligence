# 🧠 Case Study 2: Fei Protocol – Reentrancy Exploit & Laundering Flow

## 🎯 Objective
Investigate the **Fei Protocol (Rari Fuse)** exploit on the **Ethereum Mainnet (April 2022)**,  
trace post-exploit fund movement, and identify laundering patterns involving **mixers and exchange deposits**.

---

## 🧩 Background
In **April 2022**, Fei Protocol’s integrated **Rari Capital Fuse pools** suffered a **reentrancy vulnerability** exploit,  
resulting in a total loss of **~$80 million** across multiple ERC-20 assets including **ETH, DAI, USDC, and LUSD**.  

The attack exploited a **Compound fork smart contract** that failed to follow the *check-effect-interaction* pattern —  
allowing the attacker to withdraw collateral **before** their borrow records were updated.

The initial attacker wallet identified:  
`0x6162759edad730152f0df8115c698a42e666157f`

---

## 🧠 Investigation Process

### 1. **Alert Intake and Case Setup**
- KYT module triggered alerts for high-risk transactions tagged as  
  `Exploit Proceeds`, `DeFi Vulnerability`, `Mixer Interaction`.
- Case create in **Case Manager** with metadata:
  - Network: Ethereum Mainnet  
  - Tokens involved: ETH, DAI, USDC, LUSD  
  - First seen: `2022-04-30 08:06 UTC`

---

### 2. **On-Chain Tracing (Etherscan / Breadcrumbs / Chainalysis Reactor)**
- Step 1: Exploit initiated via Fuse Pool contracts → multiple borrow/withdraw calls in the same block (reentrancy loop).
- Step 2: Attacker consolidated tokens into primary wallet  
  `0x6162759e...6157f`.
- Step 3: Swapped partial funds via **Uniswap V2** (DAI → ETH, ETH → USDC).  
- Step 4: Bridged smaller portions to **BSC** and **Polygon** networks using **Anyswap / Multichain**.  
- Step 5: Deposited large chunks (~100 ETH batches) into **Tornado Cash (0xd90e2f925da726b50c4ed8d0fb90ad053324f31b)**.  
- Step 6: Post-mixer withdrawals observed moving to **new clean wallets**, then partial inflows to **Binance** and **Huobi** hot wallets.

---

### 3. **Pattern Recognition**
| Indicator | Description |
|------------|-------------|
| **Reentrancy Behavior** | Multiple borrow/withdraw calls within the same block |
| **Rapid Consolidation** | Funds merged into 1 primary address within 5 minutes |
| **Token Swaps** | Exploit proceeds diversified (DAI → ETH → USDC) |
| **Bridging Behavior** | Multi-chain movement (Ethereum → BSC → Polygon) |
| **Obfuscation Method** | Tornado Cash mixer deposits in 100 ETH increments |
| **Off-Ramp Targets** | Centralized exchanges (Binance, Huobi) |

---

### 4. **OSINT & Intelligence Correlation**
- Verified incident via **CertiK post-mortem** and **Coindesk reports** confirming ~$80M loss.  
- Address `0x6162759edad730152f0df8115c698a42e666157f` labeled as **Fei Protocol Exploiter** on **Etherscan**.  
- Related addresses appeared in **Chainabuse.com** tagged “DeFi Exploit”.  
- Mixer addresses cross-referenced with **Chainalysis Sanctions Intel**,  
  indicating overlap with previously known laundering routes.

---

## 📊 Findings
| Type | Value |
|------|-------|
| Source of Funds | Fei / Rari Fuse Reentrancy Exploit |
| Attack Vector | Check-Effect-Interaction bypass |
| Laundering Path | Ethereum → BSC → Polygon |
| Bridge Used | Multichain (Anyswap) |
| Mixer Used | Tornado Cash |
| Approx. Laundered Value | ~$78–80 million |
| Final Destinations | Binance, Huobi |
| Classification | Smart Contract Exploit + Cross-chain Laundering |

---

## 🧾 Compliance Outcomes to be made
- Escalate case internally as **High Priority – Exploit Proceeds**.  
- File **Suspicious Matter Report (SMR)** under **FATF Recommendation 16** guidance.  
- Share address list and evidence with **CEX compliance contacts** for freezing action.  
- Update internal **risk-scoring models** to flag future reentrancy-linked exploit flows.

---

## 🧠 Learning
- Reentrancy remains a common root cause in DeFi protocol hacks — inherited vulnerabilities from open-source forks (e.g., Compound).  
- Rapid cross-chain fund movement + mixers = typical obfuscation flow post-exploit.  
- Early detection in KYT systems and prompt coordination with exchanges significantly improve recovery odds.

---

## 🧾 References
- CertiK Fei Protocol Incident Report (2022)  
- Coindesk: *Fei Protocol Loses $80M in Rari Fuse Exploit*  
- Etherscan: *Fei Protocol Exploiter Address – 0x6162759e...6157f*  
- Chainalysis Blog: *Reentrancy Exploits and Laundering Typologies in DeFi*  

---
---

✅ **Tags:** `#BridgeLaundering` `#TornadoCash` `#DeFiExploit` `#CrossChain` `#Compliance`

