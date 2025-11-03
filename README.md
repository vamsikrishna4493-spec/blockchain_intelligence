# 🧩 Crypto Compliance & Blockchain Investigations Portfolio  

**Author:** Vamsi Krishna  
**Role:** Independent Blockchain Investigator | Crypto Compliance & FIU Analyst  
**Experience:** 2+ Years in Crypto Transaction Monitoring, Risk Analysis & AML Investigations  

---

## 👋 Introduction  

Hi, I’m **Vamsi Krishna**, a blockchain investigator with hands-on experience in **crypto compliance, FIU operations, and on-chain analysis**.  

Over the past two years, I’ve independently worked on **transaction monitoring, wallet risk assessment, and exploit tracing**, combining investigative tools like **Breadcrumbs, Chainalysis KYT, Reactor, and Etherscan** with regulatory frameworks such as **FATF** and **AUSTRAC**.  

My focus lies in connecting blockchain forensics with compliance reporting — identifying illicit fund movements, mapping laundering patterns, and preparing defensible, regulator-ready case documentation.  

---

## 🎯 Objective  

This repository demonstrates my capabilities in **crypto transaction monitoring, AML investigations, and compliance reporting**, with case studies that reflect real FIU workflows and escalation logic.  

You’ll find:
- End-to-end case investigations  
- Transaction tracing and behavioral pattern analysis  
- Risk documentation aligned with **FATF / AUSTRAC** standards  
- Practical examples of **SAR/SMR reporting**  

---

## 🧭 Repository Overview  

| Folder | Description |
|--------|--------------|
| `1_Case_Studies/` | Real-world style investigations — scams, exploits, and laundering typologies. |
| `2_Tools_and_Methods/` | My investigative stack: tracing tools, OSINT resources, and workflows. |
| `3_Compliance_Procedures/` | FIU workflows, red-flag indicators, and SMR templates. |

---

## 🔍 Featured Case Studies  

---

### 🕵️ Case Study 1: Fraudulent Airdrop Scam  

#### 🎯 Objective  
Investigate a phishing-based airdrop scam that drained wallets through malicious contract approvals.  

#### 🧩 Background  
A fake **$XGOLD** airdrop campaign was promoted across **Twitter and Discord**, hosted on `xgoldairdrop[.]org`.  
Users connecting their wallets unknowingly approved token transfers to the attacker.  

#### 🧠 Investigation Steps  

**1. Case Intake**  
- Collected ~15 victim addresses.  
- Main scam wallet: `0x82b1a0282f4fcbf90f55cad5768c0a021cdcbaee`.  
- Tagged in KYT as **High Risk – Phishing**.  

**2. On-Chain Analysis**  
- Funds consolidated from victims into one wallet.  
- Swapped via **Uniswap V2** (WETH → USDT).  
- Outflows to **Binance** and **FixedFloat**.  

**3. OSINT Verification**  
- WHOIS: Russian domain registrar.  
- Scam reused same wallet in multiple Twitter campaigns.  

#### 📊 Findings  

| Metric | Value |
|--------|-------|
| Victim Wallets | 18 |
| Total Loss | ~$12,400 |
| Assets | USDT, WETH |
| Destination | Binance, FixedFloat |
| Category | Airdrop / Phishing Scam |

#### 🧾 Compliance Outcome  
- **SMR** filed under **AUSTRAC** guidelines.  
- Scammer wallet added to internal blacklist.  
- Findings shared with exchange partners.  

**Key Learning:** Fake airdrops exploit contract approval mechanics — preventive education and wallet security checks are critical.  

✅ **Tags:** `#Phishing` `#AirdropScam` `#Compliance`  

---

### 🧠 Case Study 2: Fei Protocol – Reentrancy Exploit & Laundering Flow  

#### 🎯 Objective  
Reconstruct and trace the **Fei Protocol (Rari Fuse)** exploit that resulted in ~$80M loss, identifying laundering flow post-attack.  

#### 🧩 Background  
In April 2022, Fei Protocol’s Rari Fuse pools were exploited due to a **reentrancy vulnerability** in Compound-fork contracts.  
The bug allowed attackers to withdraw collateral before loan balances updated.  

Primary exploiter: `0x6162759edad730152f0df8115c698a42e666157f`.  

#### 🧠 Investigation Steps  

**1. Alert & Case Setup**  
- Alert: **Exploit Proceeds** tagged in KYT.  
- Assets: ETH, DAI, USDC, LUSD.  
- First seen: `2022-04-30 08:06 UTC`.  

**2. Transaction Tracing**  
- Detected reentrancy loop (borrow/withdraw in same block).  
- Funds aggregated → swapped (DAI → ETH → USDC).  
- Bridged via **Multichain** to **BSC** and **Polygon**.  
- Sent 100 ETH batches through **Tornado Cash**.  
- Mixer withdrawals → Binance & Huobi.  

**3. Risk Indicators**

| Indicator | Observation |
|------------|-------------|
| Reentrancy pattern | Borrow/withdraw within same block |
| Fund consolidation | Merged to single wallet |
| Cross-chain flow | Bridging to BSC & Polygon |
| Obfuscation | Tornado Cash deposits |
| Off-ramping | Exchange deposits |

**4. OSINT Correlation**  
- Verified via **CertiK**, **Coindesk**, **Chainabuse**.  
- Etherscan labeled exploiter wallet.  
- Chainalysis intel confirmed mixer overlaps.  

#### 📊 Findings  

| Field | Detail |
|-------|--------|
| Source | Fei/Rari Fuse Exploit |
| Attack Vector | Smart Contract Reentrancy |
| Laundering Route | Multichain → Tornado Cash → Exchanges |
| Estimated Loss | ~$78–80M |
| Exchanges | Binance, Huobi |
| Classification | DeFi Exploit + Laundering Flow |

#### 🧾 Compliance Outcome  
- Flagged **High Priority – Exploit Proceeds**.  
- SMR filed under **FATF Recommendation 16**.  
- Shared with CEX compliance teams for potential freeze.  
- KYT models updated to detect reentrancy typologies.  

**Key Learning:** Reentrancy remains a top DeFi threat. Mixer and bridge usage post-exploit shows the evolution of laundering tactics.  

✅ **Tags:** `#DeFiExploit` `#CrossChain` `#TornadoCash`  

---

## 🛠️ Tools & Methods  

| Category | Tools |
|-----------|-------|
| Blockchain Analytics | Breadcrumbs, Chainalysis KYT, Reactor, TRM Explorer |
| Explorers | Etherscan, BscScan, TronScan, Arkham Intelligence |
| OSINT Sources | Whois, URLScan, ScamSniffer, Telegram, Reddit |
| Visualization | Power BI, Graphviz |
| Compliance Frameworks | FATF, AUSTRAC, FinCEN, EU AMLD5, Travel Rule |

---

## 🧾 Compliance Procedures & Reporting  

### 🔑 Core Functions  
- **Transaction Monitoring:** Reviewing KYT alerts & escalation.  
- **EDD:** Deep-dive into high-risk counterparties.  
- **Case Documentation:** Trace evidence + risk scoring + rationale.  
- **SAR/SMR Drafting:** AUSTRAC/FATF-aligned reporting.  

### ⚖️ Key Frameworks  
- FATF Recommendations **15 & 16**  
- **AUSTRAC**, **EU AMLD5**, and **Travel Rule** obligations  
- Internal scoring models (behavioral, transactional, counterparty)  

### ✅ Outcome  
All cases are:
- **Defensible** — on-chain verified  
- **Consistent** — structured logic  
- **Auditable** — compliant documentation  

---

## 💬 Investigative Philo
e Investigator Portfolio”ompliance research or discuss investigative frameworks, feel free to connect!
