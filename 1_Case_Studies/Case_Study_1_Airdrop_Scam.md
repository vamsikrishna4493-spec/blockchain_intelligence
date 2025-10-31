# 🕵️‍♂️ Case Study 1: Fraudulent Airdrop Investigation

## 🎯 Objective
Investigate a fraudulent airdrop campaign that lured users into connecting their wallets and approving malicious smart contracts — leading to token theft.

---

## 🧩 Background
Several users reported token losses after interacting with a suspicious airdrop claiming to distribute “$XGOLD”.  
The scam was spread via Twitter and Discord, prompting users to visit a fake site:  
**`xgoldairdrop[.]org`**  

The fake dApp asked users to connect MetaMask and sign an approval transaction, giving the scammer access to their tokens.

---

## 🧠 Investigation Process

### 1. **Initial Intake (KYT)**
- Collected victim wallet addresses from alert submissions.
- Extracted scammer address from transaction history: 0x82b1a0282f4fcbf90f55cad5768c0a021cdcbaee
- KYT flagged the wallet for *High Risk – Phishing*.

### 2. **On-Chain Tracing (Breadcrumbs / Chainalysis Reactor)**
- The scammer wallet received funds from **15+ victim wallets**.
- Funds were **swapped to WETH → USDT** within minutes.
- Outflows directed to **Binance** and **FixedFloat** (CEX + instant swap service).

### 3. **Attribution (OSINT)**
- Domain WHOIS linked to **anonymous registrar in Russia**.
- Website content reused assets from a known **phishing template cluster**.
- Twitter handle `@xgold_airdrop` reused wallet address across multiple scam posts.

### 4. **Risk Indicators**
- Large number of inbound small-value transfers.
- Rapid token swaps and off-ramping.
- No legitimate contract interaction history.
- Shared address structure with prior flagged scam clusters.

---

## 📊 Findings
| Type | Value |
|------|-------|
| Number of Victim Wallets | 18 |
| Total Loss | ~$12,400 |
| Primary Assets | USDT, WETH |
| Destination Entities | Binance, FixedFloat |
| Classification | Phishing / Airdrop Scam |

---

## 🧾 Compliance Outcome
- Compiled alert summary for **SMR submission** under AUSTRAC guidelines.  
- Flagged associated addresses for **blacklisting in KYT**.
- Shared findings with ecosystem partners via **TRM Threat Intelligence**.

---

## 🧠 Learning
This case demonstrates how **fake airdrops** exploit user trust and contract approvals.  
Proactive screening of new tokens and wallet approvals can significantly reduce risk exposure.

---

✅ **Tags:** `#Phishing` `#AirdropScam` `#TransactionMonitoring` `#Chainalysis` `#Compliance`

