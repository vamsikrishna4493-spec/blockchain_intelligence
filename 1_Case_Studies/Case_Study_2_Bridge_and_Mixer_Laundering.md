# 🌉 Case Study 2: Bridge and Mixer Laundering Investigation

## 🎯 Objective
Trace the movement of illicit funds linked to a DeFi protocol exploit and identify laundering typologies using cross-chain bridges and mixers.

---

## 🧩 Background
On 14 June 2025, MoonPay’s KYT system generated multiple high-severity alerts connected to a known **DeFi exploit** on the **Arbitrum** network.  
Funds originating from the attacker’s wallet were traced moving through **multiple chains** and obfuscation tools before arriving at **centralized exchanges**.

The initial source address flagged by KYT: 0x3e8f76bA2390c2B7F46a452b8DfA72F9806E6E1b

---

## 🧠 Investigation Process

### 1. **Intake and Alert Review**
- KYT flagged several inbound transfers with tags:  
  `High Risk – Exploit Proceeds`, `Cross-chain Activity`.
- Created case in **Case Manager** and attached wallet metadata and alert notes.

---

### 2. **On-Chain Tracing (Chainalysis Reactor / Breadcrumbs)**
- Initial source: Exploited funds from **DeFi lending pool**.
- Step 1: Attacker swapped tokens on **Uniswap (ETH → USDC)**.  
- Step 2: Bridged funds via **Multichain Bridge** from Arbitrum → Ethereum → BSC.  
- Step 3: On BSC, attacker converted USDC → BNB → **Tornado Cash** (mixer).  
- Step 4: Partial withdrawals from mixer to fresh addresses → **CEX deposit wallets (Binance, OKX)**.

---

### 3. **Pattern Recognition**
| Indicator | Description |
|------------|-------------|
| **Bridging Behavior** | Multiple chains used within 2 hours |
| **Small Repeated Transfers** | Split into 50–100 smaller transactions |
| **Destination Entities** | Known CEX wallets with past exposure to laundering |
| **Timing Pattern** | Immediate off-ramping post-bridge swap |
| **Token Swaps** | ETH → USDC → BNB to reduce traceability |

---

### 4. **OSINT Analysis**
- Twitter posts from blockchain sleuths confirmed related **exploit wallet cluster**.
- Address also appeared in **Chainabuse.com** reports tagged “DeFi Exploit”.
- Mixer address linked to known **North Korea–related laundering operations** (per Chainalysis Intel).

---

## 📊 Findings
| Type | Value |
|------|-------|
| Source of Funds | DeFi Protocol Exploit |
| Laundering Path | Arbitrum → Ethereum → BSC |
| Bridge Used | Multichain |
| Mixer Used | Tornado Cash |
| Estimated Laundered Value | ~$3.2 million |
| Final Destinations | Binance, OKX |
| Classification | Cross-chain Money Laundering |

---

## 🧾 Compliance Outcome
- Escalated case for **Suspicious Matter Report (SMR)** under AUSTRAC jurisdiction.  
- Shared intelligence with **CEX compliance contacts** for wallet freezing.  
- Added addresses to internal **watchlist** and **risk scoring model** for typology reference.

---

## 🧠 Learning
Cross-chain laundering is becoming more prevalent due to the growth of bridge protocols.  
FIU teams must monitor not just **on-chain movements** but also **cross-chain asset behavior** and **timing correlations** to detect hidden patterns.

---

✅ **Tags:** `#BridgeLaundering` `#TornadoCash` `#DeFiExploit` `#CrossChain` `#Compliance`

