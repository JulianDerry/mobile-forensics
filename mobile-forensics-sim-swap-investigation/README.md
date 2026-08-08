# Operation SIM Shift. Mobile Money Fraud via SIM Swap

**Digital Forensics Examination Report**  
**Case Reference:** HC-GH-2025-SF-0089

---

## Case Overview

| Property | Value |
|----------|-------|
| Case ID | HC-GH-2025-SF-0089 |
| Investigation Title | Operation SIM Shift |
| Investigation Type | Mobile Money Fraud (SIM Swap) |
| Jurisdiction | Republic of Ghana |
| Device | Samsung Galaxy A23 |
| Android Version | 13 |
| Extraction Method | File System + Logical |
| Primary Tool | Cellebrite UFED 4PC |
| Image Format | E01 |
| Hash Verification | MD5 verified |
| Lead Examiner | Julian Derry |
| Organization | Hive Consult |
| Report Date | 2025-04-02 |

---

## Table of Contents

- [Executive Summary](#executive-summary)
- [Evidence Overview](#evidence-overview)
- [Forensic Integrity](#forensic-integrity)
- [Social Engineering Analysis](#social-engineering-analysis)
- [SIM Swap Execution](#sim-swap-execution)
- [Financial Crime Analysis](#financial-crime-analysis)
- [Complete Timeline](#complete-timeline)
- [Fraud Stage Analysis](#fraud-stage-analysis)
- [Evidence Gaps](#evidence-gaps)
- [Security Failure Analysis](#security-failure-analysis)
- [Findings and Conclusions](#findings-and-conclusions)
- [Appendix A — Exhibit Register](#appendix-a--exhibit-register)
- [Appendix B — Key Timestamps](#appendix-b--key-timestamps)
- [Appendix C — Glossary](#appendix-c--glossary)

---

## Executive Summary

This case documents a coordinated SIM swap fraud that resulted in the unauthorized withdrawal of **GH₵ 4,350.00** from a victim’s mobile money account. The investigation established a complete attack chain beginning with WhatsApp-based social engineering, followed by identity document disclosure, OTP interception, physical SIM swap execution, account takeover, financial extraction, and fund laundering.

The forensic examination was conducted on a **Samsung Galaxy A23** acquired through a verified **E01 forensic image**. Multiple independent artefacts were correlated, including WhatsApp messages, SMS records, network registration events, application databases, browser history, and account linkage logs.

---

## Evidence Overview

### Exhibit Details

| Attribute | Value |
|---|---|
| Exhibit Reference | HC-GH-2025-SF-0089-E001 |
| Device Make & Model | Samsung Galaxy A23 |
| IMEI | 359876543210987 |
| Android Version | 13 |
| Extraction Method | File System + Logical |
| Extraction Tool | Cellebrite UFED 4PC |
| Extraction Date | 2025-04-02 |

---

## Forensic Integrity

### Image Verification

| Attribute | Value |
|---|---|
| Image Format | E01 |
| MD5 Hash (Provided) | `411b57cc86dca89d34eb5b89713788c3` |
| MD5 Hash (Verified) | `411b57cc86dca89d34eb5b89713788c3` |
| Hash Match | YES |
| Verification Tool | QuickHash v3.3.4 |
| Verification Date | 2025-04-01 01:20 |

**Integrity Finding:** The forensic image hash matched the reference value supplied by the submitting authority, confirming that the image is an exact and unaltered copy of the original device.

---

## Social Engineering Analysis

### Initial Contact

| Attribute | Value |
|---|---|
| Communication Channel | WhatsApp |
| Timestamp | 2025-04-01 08:20 |
| Direction | Inbound |
| Fraudster Persona | AnansePay Telecom Support |

### Fraudulent Pretext

> “Hello, this is Ananse Telecom Support. Our records show your SIM card is faulty and will stop working today. To avoid losing your number permanently, we need to verify your identity. Please send a photo of your Ghana Card.”

<img width="1361" height="46" alt="1" src="https://github.com/user-attachments/assets/150ecb53-ace1-4c3f-9ce3-cc0970605f6e" />

The message used urgency, authority impersonation, and fear of loss to manipulate the victim.

### Identity Document Disclosure

| Event | Time | Location |
|---|---|---|
| Front Ghana Card sent | 2025-04-01 08:52 | WhatsApp Images / DCIM/Camera |
| Back Ghana Card sent | 2025-04-01 08:53 | WhatsApp Images / DCIM/Camera |

<img width="1984" height="407" alt="2" src="https://github.com/user-attachments/assets/d370355f-8c56-40e4-a3e6-d5f0a578b212" />
<img width="1984" height="1277" alt="3" src="https://github.com/user-attachments/assets/447d4e3b-2cb6-4367-a9b8-b68bd837625d" />

---

## SIM Swap Execution

### OTP Interception

| Attribute | Value |
|---|---|
| OTP Code | 583920 |
| OTP Received | 2025-04-01 09:14 |
| Victim Action | Forwarded OTP via WhatsApp |

### Retail SIM Swap

| Attribute | Value |
|---|---|
| Swap Executed | 2025-04-01 09:14:05 |
| Telecom Outlet | Ananse Telecom — Kaneshie, Accra |
| Time from OTP to Swap | 5 seconds |

<img width="1504" height="294" alt="4" src="https://github.com/user-attachments/assets/77217cfa-19f4-44a9-8ce7-4b2f05f65e1f" />

The SIM swap was completed within **5 seconds** of OTP delivery.

### Service Disruption

| Attribute | Value |
|---|---|
| Last Message Before Loss | 09:16 |
| First Message After Loss | 09:58 |
| Outage Duration | 42 minutes |
| Service Restored | 15:39:15 |

<img width="1503" height="180" alt="5" src="https://github.com/user-attachments/assets/e4e188da-7ea4-4465-92bb-bdf5e2546372" />

The victim lost cellular service for **42 minutes**, creating a window during which the fraudster could operate the account without OTP interception.

---

## Financial Crime Analysis

### Pre-Fraud Balance

| Attribute | Value |
|---|---|
| Account Balance | GH₵ 4,350.00 |

### Device Linkage

| Attribute | Value |
|---|---|
| Linked Device | Infinix Hot 30 |
| Linkage Time | 2025-04-01 09:55 |

### Fraudulent Transactions

| Time | Recipient | Account | Amount |
|---|---|---|---|
| 09:38 | KWABENA MENSAH | 0284281931 | GH₵ 4,200.00 |
| 09:42 | KWABENA MENSAH | 0284281931 | GH₵ 150.00 |

**Total Loss:** **GH₵ 4,350.00**

### Fund Laundering

<img width="1038" height="220" alt="6" src="https://github.com/user-attachments/assets/33ffb81f-b647-4e91-b33a-28289e396b67" />

<img width="1984" height="434" alt="7" src="https://github.com/user-attachments/assets/db9613f3-b0da-41f3-8d08-f4036b9d3349" />

Funds were subsequently transferred to **ABDUL RAHMAN** within approximately **27 minutes** of the first withdrawal.

---

## Complete Timeline


| Time | Event |
|---|---|
| 08:20 | Fraudster initiates WhatsApp contact |
| 08:52 | Front Ghana Card transmitted |
| 08:53 | Back Ghana Card transmitted |
| 09:14 | OTP received and disclosed |
| 09:14:05 | SIM swap executed |
| 09:16 | Final fraudster message |
| 09:38 | Transfer 1 — GH₵ 4,200 |
| 09:42 | Transfer 2 — GH₵ 150 |
| 09:55 | Infinix Hot 30 linked |
| 09:58 | Victim notices service loss |
| 15:39 | SIM restored |
| 2025-04-02 | Police report filed |

---

## Fraud Stage Analysis

### Stage 1 — Reconnaissance

Victim identified as an AnansePay user.

### Stage 2 — Social Engineering

WhatsApp impersonation used to obtain Ghana Card images and OTP.

### Stage 3 — Technical Execution

Physical SIM swap completed at Kaneshie telecom outlet.

### Stage 4 — Financial Extraction

Mobile money account drained in two transactions.

### Stage 5 — Fund Laundering

Funds moved to a secondary mule account.

---

## Evidence Gaps

Additional evidence required for attribution includes:

- Telecom CCTV footage
- SIM swap request forms
- KYC records
- Mobile money account records
- WhatsApp subscriber data
- IP address logs
- Call Detail Records (CDRs)
- Forensic image of the linked Infinix Hot 30

---

## Security Failure Analysis

| Failure | Preventive Control |
|---|---|
| Responded to unsolicited support contact | Verify through official telecom channels |
| Sent Ghana Card images | Never transmit ID documents via messaging apps |
| Shared OTP | OTPs must never be shared |
| Delayed reporting | Immediately contact telecom and mobile money provider |
| No transaction limits | Enable limits and secondary authentication |
| Delayed fraud escalation | Report within minutes to improve recovery chances |

---

## Findings and Conclusions

### Key Findings

- E01 image integrity verified.
- SIM swap executed at **09:14:05**.
- Account fully drained by **09:42**.
- Infinix Hot 30 linked at **09:55**.
- Two mule accounts identified.
- Evidence indicates a coordinated and pre-meditated operation.

### Professional Opinion

The recovered digital evidence is consistent with a **coordinated SIM swap fraud** conducted on **2025-04-01**, resulting in an unauthorized loss of **GH₵ 4,350.00**. The perpetrators used WhatsApp social engineering, identity document harvesting, OTP interception, physical SIM replacement, account takeover, and rapid fund laundering.

---

## Appendix A — Exhibit Register

| Ref | Description | Status |
|---|---|---|
| EX-001 | Samsung Galaxy A23 | Examined |
| EX-002 | E01 Forensic Image | Examined |

---

## Appendix B — Key Timestamps

| Timestamp | Event |
|---|---|
| 2025-04-01 08:20 | First WhatsApp contact |
| 2025-04-01 08:52 | Front Ghana Card sent |
| 2025-04-01 08:53 | Back Ghana Card sent |
| 2025-04-01 09:14 | OTP disclosed |
| 2025-04-01 09:14:05 | SIM swap executed |
| 2025-04-01 09:38 | Transfer 1 |
| 2025-04-01 09:42 | Transfer 2 |
| 2025-04-01 09:55 | Device linked |
| 2025-04-01 09:58 | Victim notices outage |
| 2025-04-01 15:39 | SIM restored |
| 2025-04-02 | Police report filed |

---

## Appendix C — Glossary

| Term | Definition |
|---|---|
| SIM Swap | Fraudulent transfer of a phone number to a new SIM card |
| OTP | One-Time Password |
| E01 | Expert Witness Format forensic image |
| MD5 Hash | File integrity verification hash |
| Mule Account | Account used to receive or move illicit funds |
| Logical Extraction | Extraction of accessible file system data |
| File System Extraction | Deeper extraction including file system structures |
| Layering | Movement of funds through multiple accounts to hide origin |

---

**End of Report — HC-GH-2025-SF-0089**
