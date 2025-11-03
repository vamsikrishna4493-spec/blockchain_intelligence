🧩 Crypto Compliance & Blockchain Investigations Portfolio

Author: Vamsi Krishna
Role: Independent Blockchain Investigator | Crypto Compliance & FIU Analyst
Experience: 2+ Years in Crypto Transaction Monitoring, Risk Analysis, and AML Investigations

👋 Introduction

Hi, I’m Vamsi Krishna, a blockchain investigator with hands-on experience in crypto compliance, FIU operations, and on-chain investigations.

Over the last two years, I’ve worked independently on several transaction monitoring and fund tracing cases, analyzing wallet behavior, investigating exploit proceeds, and documenting risk typologies using tools like Breadcrumbs, Chainalysis KYT, Reactor, and Etherscan.

My focus lies in identifying illicit fund movements, mapping behavioral patterns across wallets, and building defensible reports that support Financial Intelligence Unit (FIU) functions and compliance operations.

🎯 Objective

This portfolio showcases my experience in crypto compliance and blockchain investigations, with an emphasis on AML/CFT controls and case handling.

It’s designed to reflect how I approach real-world investigations, from alert intake to reporting, and how I align technical tracing with regulatory expectations.

You’ll find:

Step-by-step case investigations and analysis workflows

Compliance documentation and escalation frameworks

Examples of reporting and risk rationale as used in FIU environments

🧭 Repository Overview
Folder	Description
1_Case_Studies/	Investigation case files – scams, exploits, laundering typologies.
2_Tools_and_Methods/	Investigative stack – tracing tools, OSINT sources, and techniques.
3_Compliance_Procedures/	FIU workflows, red-flag indicators, and SMR templates.
🔍 Featured Case Studies
🕵️ Case Study 1: Fraudulent Airdrop Scam
🎯 Objective

Investigate a phishing airdrop campaign that drained victims’ wallets through malicious smart contract approvals.

🧩 Background

A fake campaign promoted a token called $XGOLD across Twitter and Discord, hosted on xgoldairdrop[.]org.
Users were prompted to connect MetaMask and unknowingly approved transactions that allowed the attacker to transfer their tokens.

🧠 Investigation Steps

1. Case Intake

Collected ~15 victim wallets and linked transactions.

Identified main scam wallet: 0x82b1a0282f4fcbf90f55cad5768c0a021cdcbaee.

Chainalysis KYT tagged the address as High Risk – Phishing.

2. On-Chain Analysis

Funds from victims consolidated into the scam wallet.

Tokens swapped on Uniswap V2: WETH → USDT.

Outflows directed to Binance and FixedFloat for cash-out.

3. OSINT Support

WHOIS lookup showed Russian domain registrar.

Scam wallet reused in other phishing campaigns tied to Twitter handle @xgold_airdrop.

📊 Summary
Metric	Value
Victim Wallets	18
Total Loss	~$12,400
Assets	USDT, WETH
Destination	Binance, FixedFloat
Category	Airdrop Phishing Scam
🧾 Compliance Notes

SMR filed following AUSTRAC guidelines.

Wallet address added to internal watchlist.

Report shared with exchange partners for visibility.

💡 Key Takeaways

This case underlines how malicious contract approvals remain one of the simplest but most effective phishing tactics.
Early awareness and smart contract permission alerts could prevent similar thefts.

✅ Tags: #Phishing #AirdropScam #Compliance #OnChainAnalysis

🧠 Case Study 2: Fei Protocol – Reentrancy Exploit & Laundering Flow
🎯 Objective

Reconstruct the Fei Protocol exploit that drained ~$80M in April 2022 and trace post-exploit laundering patterns across networks.

🧩 Background

The Fei Protocol x Rari Fuse exploit on Ethereum stemmed from a reentrancy vulnerability in the lending pool contracts.
Attackers were able to withdraw collateral before loan balances updated, bypassing accounting logic.

Primary exploiter wallet: 0x6162759edad730152f0df8115c698a42e666157f.

🧠 Investigation Steps

1. Intake and Case Initialization

Alert type: Exploit Proceeds.

Assets involved: ETH, DAI, USDC, LUSD.

Event timestamp: 2022-04-30 08:06 UTC.

2. On-Chain Reconstruction

Identified repeated borrow() and withdraw() calls in same block – classic reentrancy pattern.

Exploited funds aggregated into a single wallet.

Conducted swaps on Uniswap V2 (DAI → ETH → USDC).

Funds bridged via Multichain to BSC and Polygon.

Approximately 100 ETH batches sent through Tornado Cash.

Subsequent withdrawals redistributed to fresh wallets, then to Binance and Huobi.

3. Typology and Risk Mapping

Indicator	Observation
Reentrancy behavior	Repeated borrow/withdraw loops
Consolidation	Merging to a single wallet
Cross-chain activity	Bridge use across BSC & Polygon
Obfuscation	Tornado Cash usage
Off-ramping	Deposits to centralized exchanges

4. OSINT Correlation

Cross-verified via CertiK, Coindesk, and Chainabuse reports.

Etherscan officially labeled exploiter address.

Mixer overlap confirmed by Chainalysis Intelligence dataset.

📊 Findings
Field	Detail
Source	Fei / Rari Fuse Exploit
Attack Vector	Smart Contract Reentrancy
Laundering Path	Multichain → Tornado Cash → Exchanges
Value	~$78–80M
Exchanges Involved	Binance, Huobi
Classification	DeFi Exploit / Laundering Typology
🧾 Compliance Outcome

Escalated as High Priority – Exploit Proceeds.

SMR prepared under FATF Recommendation 16 (transfer transparency).

Shared with exchange compliance teams for asset freezing.

Updated internal KYT model to flag reentrancy-based exploit patterns.

💡 Key Takeaways

Reentrancy remains one of the most exploited vulnerabilities in DeFi.

Bridges and mixers enable quick cross-chain laundering.

Early intelligence coordination with exchanges improves asset recovery chances.

✅ Tags: #DeFiExploit #CrossChainLaundering #Compliance #TornadoCash

🛠️ Tools & Methodology
Category	Tools Used
Blockchain Analytics	Breadcrumbs, Chainalysis KYT & Reactor, TRM Explorer
Explorers	Etherscan, BscScan, TronScan, Arkham Intelligence
OSINT	Whois, URLScan, ScamSniffer, Telegram, Reddit
Visualization	Power BI, Graphviz
Compliance Frameworks	FATF, AUSTRAC, FinCEN, EU AMLD5, Travel Rule
🧾 Compliance Procedures & Reporting
🔑 Core Functions

Transaction Monitoring: Reviewing alerts and conducting risk escalation.

Enhanced Due Diligence (EDD): Profiling high-risk counterparties and wallet behavior.

Case Documentation: Preparing summaries with trace visuals, risk scores, and compliance notes.

Reporting: Drafting SMRs/SARs under AUSTRAC & FATF standards.

⚖️ Frameworks & Regulations

FATF Recommendations 15 & 16 (Virtual Assets, Wire Transfers)

AUSTRAC, EU AMLD5, and Travel Rule compliance obligations

Internal risk scoring based on behavioral, transactional, and counterparty metrics

✅ Outcome

All investigations are designed to be:

Defensible — backed by on-chain evidence

Consistent — following structured escalation logic

Auditable — compliant for internal and regulatory review

💬 Investigative Philosophy

Behavioral Reconstruction — Understand how actors operate by analyzing patterns across confirmed cases.

Evidence Integrity — Maintain timestamped, verifiable data trails.

Compliance-First Approach — Align investigations with AML/CFT frameworks and risk policy expectations.

To me, crypto compliance is about connecting technical forensics with regulatory reasoning — balancing precision and professional judgment.

🚀 Future Goals

Deepen skills in smart contract forensics and cross-chain exploit tracing.

Explore NFT wash trading typologies and analytics.

Contribute to open-source datasets that support crypto compliance education.

All case studies here are for educational and professional demonstration purposes.
Data and wallet addresses are sourced from public records or anonymized simulations.

🟢 Last Updated: October 2025
🟢 Version: 1.0 — “Crypto Compliance Investigator Portfolio”ompliance research or discuss investigative frameworks, feel free to connect!
