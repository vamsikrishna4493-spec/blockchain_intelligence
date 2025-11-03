# 🧠 Case Study 2: Fei Protocol – Reentrancy Exploit & Laundering Flow

## 🎯 Objective
Investigate the **Fei Protocol (Rari Fuse)** exploit on the **Ethereum Mainnet (April 2022)** to trace the flow of stolen funds and uncover laundering patterns involving **mixers, bridges, and centralized exchanges**.

---

## 🧩 Background
In **April 2022**, the **Fei Protocol**—which had merged with **Rari Capital’s Fuse pools**—suffered a major **reentrancy exploit**.  
The vulnerability allowed an attacker to repeatedly borrow and withdraw before the contract could update their collateral balance, exploiting a flaw in the **Compound fork** codebase.  

The total loss was estimated at **~$80 million**, spanning several ERC-20 tokens such as **ETH, DAI, USDC, and LUSD**.  
The primary attacker wallet identified was:  
`0x6162759edad730152f0df8115c698a42e666157f`

---

## 🧠 Investigation Process

### 1. **Alert Intake and Case Setup**
- **KYT** triggered multiple alerts labeled: `Exploit Proceeds`, `DeFi Vulnerability`, and `Mixer Interaction`.  
- A case was created in **Case Manager**, with the following metadata captured:
  - **Network:** Ethereum Mainnet  
  - **Tokens:** ETH, DAI, USDC, LUSD  
  - **Timestamp:** 2022-04-30 08:06 UTC  
- Initial enrichment confirmed the address cluster was linked to the **Fei / Rari Fuse exploit**.

---

### 2. **On-Chain Tracing (Etherscan / Breadcrumbs / Chainalysis Reactor)**
- **Step 1:** The exploit was executed through multiple borrow-and-withdraw calls within a single block (classic **reentrancy loop**).  
- **Step 2:** The attacker consolidated assets into the main wallet `0x6162759e...6157f`.  
- **Step 3:** Funds were partially **swapped on Uniswap V2** (DAI → ETH → USDC) to increase liquidity.  
- **Step 4:** Smaller portions were **bridged via Multichain (Anyswap)** to **BSC** and **Polygon** networks.  
- **Step 5:** Approximately **100 ETH batches** were then deposited into **Tornado Cash** (`0xd90e2f925da726b50c4ed8d0fb90ad053324f31b`).  
- **Step 6:** Post-mixing withdrawals were distributed to new “clean” wallets, followed by inflows to **Binance** and **Huobi** exchange deposit addresses.

---

### 3. **Pattern Recognition**
| Indicator | Description |
|------------|-------------|
| **Reentrancy Activity** | Multiple borrow/withdraw loops within the same block |
| **Rapid Consolidation** | Tokens merged into one primary address within minutes |
| **Swap Behavior** | Conversion from DAI → ETH → USDC for obfuscation |
| **Cross-Chain Movement** | Ethereum → BSC → Polygon |
| **Obfuscation Method** | Tornado Cash mixer deposits (100 ETH increments) |
| **Off-Ramp Entities** | Binance and Huobi CEX hot wallets |

---

### 4. **OSINT & Intelligence Correlation**
- Verified incident through **CertiK’s post-mortem** and **CoinDesk’s public report** confirming the $80M loss.  
- On **Etherscan**, wallet `0x6162759edad730152f0df8115c698a42e666157f` is labeled as the **Fei Protocol Exploiter**.  
- Related addresses appeared on **Chainabuse.com** tagged as “DeFi Exploit.”  
- Mixer interaction addresses were cross-referenced with **Chainalysis Sanctions Intel**, revealing overlap with previously identified **laundering clusters**.

---

## 📊 Findings
| Category | Details |
|-----------|----------|
| **Source of Funds** | Fei / Rari Fuse Reentrancy Exploit |
| **Attack Vector** | Check-Effect-Interaction Bypass |
| **Laundering Path** | Ethereum → BSC → Polygon |
| **Bridge Used** | Multichain (Anyswap) |
| **Mixer Used** | Tornado Cash |
| **Estimated Laundered Value** | ~$78–80 million |
| **Final Destinations** | Binance, Huobi |
| **Classification** | Smart Contract Exploit + Cross-Chain Laundering |

---

## 🧾 Compliance Actions
- Escalated case internally as **High Priority – Exploit Proceeds**.  
- Filed **Suspicious Matter Report (SMR)** aligned with **FATF Recommendation 16**.  
- Shared confirmed addresses and transaction evidence with **CEX compliance teams** for potential wallet freezes.  
- Updated internal **risk-scoring models** to detect reentrancy-related exploit flows.  

---

## 🧠 Key Learnings
- **Reentrancy vulnerabilities** remain one of the most exploited flaws in DeFi, often inherited from forked codebases.  
- The combination of **bridging and mixers** continues to be a preferred laundering typology post-exploit.  
- **Timely alert escalation and inter-exchange collaboration** significantly improve fund recovery and mitigation outcomes.  

---

## 📚 References
- [CertiK Incident Report – Fei Protocol (2022)](https://www.certik.com/resources/blog)  
- [CoinDesk: Fei Protocol Loses $80M in Rari Fuse Exploit](https://www.coindesk.com)  
- [Etherscan Label: Fei Protocol Exploiter – 0x6162759e...6157f](https://etherscan.io/address/0x6162759edad730152f0df8115c698a42e666157f)  
- [Chainalysis Blog: Reentrancy Exploits and Laundering Typologies in DeFi](https://blog.chainalysis.com)  

---

✅ **Tags:** `#BridgeLaundering` `#TornadoCash` `#DeFiExploit` `#CrossChain` `#Compliance`  


