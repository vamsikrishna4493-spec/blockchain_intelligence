# 🧩 Crypto Compliance & Blockchain Investigations Portfolio  

**Author:** Vamsi Krishna  
**Role:** Independent Blockchain Investigator | Crypto Compliance & FIU Analyst  
**Experience:** 2+ Years in Crypto Transaction Monitoring, Risk Analysis, and AML Investigations  

---

## 👋 Introduction  

Hi, I’m **Vamsi Krishna**, a blockchain investigator specializing in **crypto compliance, FIU operations, and on-chain investigations**.  

For the past two years, I’ve worked independently on **transaction monitoring and fund flow tracing**, reconstructing suspicious cases and investigating high-risk wallet activity using tools like **Breadcrumbs, Etherscan, Chainalysis KYT, Reactor, and OSINT sources**.  

My work focuses on uncovering illicit fund flows, identifying behavioral typologies, and improving red-flag indicators that help **Financial Intelligence Units (FIUs)** detect and prevent crypto-related financial crime.  

---

## 🎯 Objective  

This repository showcases my **crypto compliance and investigation capabilities**, aligning with the role of an **FIU Transaction Monitoring Analyst**.  

It demonstrates:  
- End-to-end investigation processes  
- Analytical reasoning in blockchain transaction tracing  
- Familiarity with **AML/CFT frameworks, VASP investigations, and SMR/SAR reporting**  
- Documentation and compliance discipline expected in a regulated crypto environment  

---

## 🧭 Repository Structure  

| Folder | Description |
|--------|--------------|
| `1_Case_Studies/` | Real-world styled case investigations — investment scams, bridge/mixer tracing, exploit tracking. |
| `2_Tools_and_Methods/` | My investigative stack — tools, OSINT sources, tracing workflows. |
| `3_Compliance_Procedures/` | FIU workflows, red-flag libraries, and SMR templates (AUSTRAC/FinCEN aligned). |

---

## 🔍 Featured Case Studies  

---

### 🕵️‍♂️ Case Study 1: Fraudulent Airdrop Investigation  

#### 🎯 Objective  
Investigate a fraudulent airdrop campaign that lured users into connecting wallets and approving malicious contracts, leading to token theft.  

#### 🧩 Background  
Victims reported losses after engaging with a fake **$XGOLD** airdrop promoted on **Twitter and Discord** via:  
🔗 `xgoldairdrop[.]org`  

The malicious dApp prompted users to connect MetaMask and sign approvals granting token transfer access.  

#### 🧠 Investigation Process  

**1. Initial Intake (KYT)**  
- Collected 15+ victim wallet addresses.  
- Identified scammer wallet: `0x82b1a0282f4fcbf90f55cad5768c0a021cdcbaee`.  
- KYT flagged: **High Risk – Phishing.**  

**2. On-Chain Tracing (Breadcrumbs / Chainalysis Reactor)**  
- Funds from 18 victims consolidated into scam wallet.  
- Immediate swaps: WETH → USDT.  
- Outflows to **Binance** and **FixedFloat**.  

**3. Attribution (OSINT)**  
- Domain WHOIS: Russian registrar, reused phishing template.  
- Twitter handle **@xgold_airdrop** reused same wallet in other scam posts.  

**4. Risk Indicators**  
| Indicator | Description |
|------------|-------------|
| Repeated small inbound transfers | Typical phishing collection behavior |
| Rapid token swaps | Immediate laundering |
| No prior contract interactions | Fresh scam wallet |
| Known scam template | Shared assets across scam cluster |

#### 📊 Findings  
| Type | Value |
|------|-------|
| Victim Wallets | 18 |
| Total Loss | ~$12,400 |
| Assets | USDT, WETH |
| Destination | Binance, FixedFloat |
| Classification | Phishing / Airdrop Scam |

#### 🧾 Compliance Outcome  
- SMR prepared under **AUSTRAC** standards.  
- Scammer addresses blacklisted in KYT.  
- Findings shared with partners.  

#### 🧠 Learning  
Fake airdrops exploit user trust and contract approvals.  
Education + proactive screening can significantly reduce risk exposure.  

✅ **Tags:** #Phishing #AirdropScam #TransactionMonitoring #Chainalysis #Compliance  

---

### 🧠 Case Study 2: Fei Protocol – Reentrancy Exploit & Laundering Flow  

#### 🎯 Objective  
Investigate the **Fei Protocol (Rari Fuse)** reentrancy exploit and trace post-exploit fund movements across bridges and mixers.  

#### 🧩 Background  
In **April 2022**, Fei Protocol’s Rari Fuse pools were exploited via a **reentrancy vulnerability**, leading to ~$80M loss in ETH, DAI, USDC, and LUSD.  
Root cause: failure to implement **check-effect-interaction pattern**.  

Initial exploiter:  
`0x6162759edad730152f0df8115c698a42e666157f`  

#### 🧠 Investigation Process  

**1. Alert Intake and Case Setup**  
- KYT tagged “Exploit Proceeds”, “Mixer Interaction”.  
- Tokens: ETH, DAI, USDC, LUSD.  
- First seen: `2022-04-30 08:06 UTC`.  

**2. On-Chain Tracing (Etherscan / Breadcrumbs / Reactor)**  
- Multiple reentrant borrow/withdraw calls in single block.  
- Consolidated funds into exploiter wallet.  
- Swaps via Uniswap V2 → DAI → ETH → USDC.  
- Bridged to **BSC** and **Polygon** (via Multichain).  
- Deposited ~100 ETH batches into **Tornado Cash**.  
- Post-mixer withdrawals → new wallets → **Binance, Huobi**.  

**3. Pattern Recognition**  
| Indicator | Description |
|------------|-------------|
| Reentrancy | Multiple borrow/withdraw in single block |
| Rapid consolidation | Funds merged to 1 main address |
| Cross-chain | Bridging between Ethereum, BSC, Polygon |
| Obfuscation | Tornado Cash 100 ETH deposits |
| Off-ramping | Exchange hot wallet deposits |

**4. OSINT Correlation**  
- Confirmed via **CertiK**, **Coindesk**, **Chainabuse**.  
- Labeled as “Fei Protocol Exploiter” on **Etherscan**.  
- Chainalysis Intel: mixer overlap with sanctioned laundering wallets.  

#### 📊 Findings  
| Type | Value |
|------|-------|
| Source | Fei/Rari Fuse Exploit |
| Attack Vector | Reentrancy (Compound fork) |
| Bridge | Multichain / Anyswap |
| Mixer | Tornado Cash |
| Laundered Value | ~$78–80M |
| Destination | Binance, Huobi |
| Classification | Smart Contract Exploit + Cross-chain Laundering |

#### 🧾 Compliance Outcomes  
- Escalated internally: **High Priority – Exploit Proceeds.**  
- Filed **SMR** under **FATF Recommendation 16**.  
- Shared with CEX compliance contacts for wallet freezing.  
- Updated KYT risk models to detect reentrancy exploit typologies.  

#### 🧠 Learning  
- Reentrancy remains a frequent DeFi exploit vector.  
- Cross-chain bridges + mixers accelerate laundering.  
- Early alerting and CEX coordination improve recovery chances.  

#### 🧾 References  
- CertiK: *Fei Protocol Incident Report (2022)*  
- Coindesk: *Fei Protocol Loses $80M in Rari Fuse Exploit*  
- Etherscan: Fei Exploiter – `0x6162759e...6157f`  
- Chainalysis: *Reentrancy Exploits & Laundering Typologies*  

✅ **Tags:** #DeFiExploit #BridgeLaundering #TornadoCash #CrossChain #Compliance  

---

## 🛠️ Tools & Techniques  

| Category | Tools Used |
|-----------|-------------|
| Blockchain Analytics | Breadcrumbs, Chainalysis KYT, Reactor, TRM Explorer |
| On-Chain Explorers | Etherscan, BscScan, TronScan, Arkham Intelligence |
| OSINT Sources | Whois, URLScan, ScamSniffer, Reddit, Telegram |
| Visualization & Reporting | Power BI, Graphviz, Google Sheets |
| Compliance Frameworks | FATF, AUSTRAC, FinCEN, EU AMLD, Travel Rule |


---

## 🧾 Compliance Procedures and Reporting Standards  

### 🧩 Key Compliance Functions  
- **Transaction Monitoring** – Reviewing KYT alerts & escalation.  
- **Enhanced Due Diligence (EDD)** – Investigating high-risk counterparties.  
- **Case Documentation** – Summaries with risk scoring & rationale.  
- **SAR/SMR Drafting** – AUSTRAC & FATF compliant submissions.  

### 📘 Frameworks & Guidelines  
- **FATF Recommendation 15 & 16** (VASPs & Wire Transfers)  
- **AUSTRAC / EU AMLD5** obligations  
- **Travel Rule, KYC, KYT procedures**  
- **Internal risk models** — transactional, behavioral, counterparty-based  

### 🚀 Outcome  
By adhering to global AML/CFT standards, my investigations remain:  
✅ **Defensible** – backed by verifiable on-chain data  
✅ **Consistent** – structured escalation logic  
✅ **Auditable** – compliant with internal & regulatory review  

---

## 🧩 Conclusion  

This portfolio demonstrates my ability to:  
- Conduct **end-to-end blockchain investigations**  
- Interpret **cross-chain laundering patterns**  
- Apply **compliance reasoning and reporting frameworks**  
- Contribute effectively to **FIU and AML operations** in the crypto sector   

---

## 🧠 Investigative Philosophy

My investigative approach follows three core principles:

1. **Behavioral Reconstruction** — studying previously solved cases to identify typology patterns and behavioral markers.  
2. **Evidence Integrity** — ensuring all data is verifiable and timestamped from chain explorers.  
3. **Compliance-First Mindset** — aligning all analyses with AML/CFT standards and regulatory expectations.  

I believe effective FIU work is both *technical and intuitive* — it requires data precision, investigative storytelling, and ethical responsibility.

---

## 🚀 Future Learning Goals

- Expand knowledge of **DeFi typologies** and **NFT-related wash trading**  
- Advance into **smart contract forensics** for deeper transaction analysis  
- Contribute to open-source crypto compliance datasets and typology guides  

---

> *This portfolio is created for educational and professional demonstration purposes.  
> All examples are anonymized and based on simulated or public blockchain data.*

---

🟢 *Last Updated:* October 2025  
🟢 *Version:* 1.0 — “Crypto Compliance Investigator Portfolio”

---
📫 **Contact:** 
  LinkedIn - https://www.linkedin.com/in/vamsi-krishna-b05ab5239/ | Email - vamsi.krishna4493@gmail.com

---
If you’d like to collaborate on blockchain compliance research or discuss investigative frameworks, feel free to connect!
