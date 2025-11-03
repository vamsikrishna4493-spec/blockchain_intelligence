# Case Study 1: Fraudulent Airdrop Investigation  

## Objective  
Investigate a deceptive airdrop campaign that tricked users into connecting their wallets and approving malicious smart contracts — resulting in unauthorized token transfers and asset theft.  

---

## Background  
Multiple users reported unexpected token losses after participating in an airdrop promoting the fake token **$XGOLD**.  
The scam circulated through **Twitter and Discord**, directing victims to a fraudulent website:  
**`xgoldairdrop[.]org`**  

Once connected, the malicious dApp prompted users to approve a transaction granting the attacker full token transfer permissions via the `approve()` function.  

---

## Investigation Process  

### 1. **Initial Intake (KYT)**  
- Collected impacted wallet addresses submitted through alert reports.  
- Identified the primary scammer wallet: `0x82b1a0282f4fcbf90f55cad5768c0a021cdcbaee`.  
- KYT flagged the address with **High Risk – Phishing / Malicious Contract** indicators.  

---

### 2. **On-Chain Tracing (Breadcrumbs / Chainalysis Reactor)**  
- The scammer wallet consolidated funds from **15+ victim wallets**.  
- Tokens were quickly **swapped from WETH → USDT** within minutes of receipt.  
- Outflows were routed to **Binance** and **FixedFloat** (a known instant swap service) for off-ramping.  

---

### 3. **Attribution (OSINT)**  
- **WHOIS lookup** of `xgoldairdrop[.]org` revealed an **anonymous registrar based in Russia**.  
- Website assets matched templates used in other known phishing clusters.  
- The associated **Twitter account** `@xgold_airdrop` reused the same wallet address across multiple scam promotions.  

---

### 4. **Risk Indicators**  
| Indicator | Description |  
|------------|--------------|  
| **Inbound Transfers** | Numerous small-value deposits from victim wallets |  
| **Rapid Token Swaps** | Immediate conversion to stablecoins post-theft |  
| **Off-Ramping Behavior** | Funds sent to CEX and swap services |  
| **Address Clustering** | Shared traits with previously flagged phishing campaigns |  

---

## Findings  
| Category | Details |  
|-----------|----------|  
| **Number of Victim Wallets** | 18 |  
| **Estimated Total Loss** | ~$12,400 |  
| **Primary Assets Stolen** | USDT, WETH |  
| **Destination Entities** | Binance, FixedFloat |  
| **Classification** | Phishing / Airdrop Scam |  

---

## Compliance Outcome  
- Compiled a case summary for **Suspicious Matter Report (SMR)** filing under **AUSTRAC** guidelines.  
- Submitted wallet addresses for **blacklisting and ongoing monitoring** in the KYT system.  
- Shared intelligence and wallet clusters with **ecosystem partners** and exchange compliance teams.  

---

## Learning  
This case illustrates how **fraudulent airdrops** exploit wallet approval mechanisms to steal user assets.  
It emphasizes the importance of **user education**, **smart contract permission awareness**, and **real-time alert escalation** to prevent similar phishing-based losses in the future.  

Proactive screening of new tokens and wallet approvals can significantly reduce risk exposure.

---

✅ **Tags:** `#Phishing` `#AirdropScam` `#TransactionMonitoring` `#Chainalysis` `#Compliance`

