# TraceRx: Distributed Ledger for Medicine Authenticity Verification in Africa


**Live Demos:**  
- **User App:** [tracerx.netlify.app](https://tracerx.netlify.app) – Web app for QR scanning, verification, and more. Clinics, pharmacies, and individuals can scan QR codes or generate them (MVP feature; restricted in production).  
- **Admin/Manufacturer App:** [tracerxadmin.netlify.app](https://tracerxadmin.netlify.app) – For medicine manufacturers to upload data, mint tokens on Hedera, and verify availability.

**Quick Start Instructions:**  
- In the User App, scan a QR code (e.g., sample below) or enter a batch ID like `AMX2000` or `AMX2001` in the QR generation page, then generate and stick it somewhere else, then scan with the in built scanner.
- Note: In a production version, QR codes would be hidden under scratch-off coatings for security. This MVP omits some restrictions for demo purposes.  
![QR Code](./assets/qr%20(2).png.png)

## Overview
In low- and middle-income countries, **1 in 10 medical products** fails quality tests, with Africa bearing a disproportionate burden: nearly **one in five medicines** is falsified or substandard. According to WHO and UNODC reports, this crisis causes approximately **500,000 deaths annually in sub-Saharan Africa**, including **267,000 from fake antimalarials** and **169,000 childhood deaths** from substandard pneumonia treatments.

TraceRx is Africa's pioneering verification platform, designed to combat counterfeit drugs using **Hedera's distributed ledger technology (DLT)** for secure, tamper-proof batch recording. Unlike existing solutions, TraceRx is inclusive: it supports **both smartphones and feature phones**, ensuring accessibility in low-connectivity areas. By bridging digital divides, TraceRx empowers patients, pharmacies, and clinics to verify medicine authenticity instantly, saving lives and restoring trust in healthcare.

## The Problem: A Silent Killer in Africa
Counterfeit medicines not only erode public trust but also lead to preventable deaths and the rise of drug-resistant diseases. In rural Africa, where many rely on basic feature phones and face unreliable internet, most tech solutions exclude the most vulnerable. Traditional methods like scratch codes are outdated, prone to tampering, and lack transparency. The result? A thriving black market for fakes, with devastating human and economic costs.

## Why TraceRx? The Inclusive Solution
TraceRx stands out by addressing these gaps head-on:  
- **Inclusivity for All Devices:** QR scanning for smartphones and USSD codes for feature phones – no internet required for basic users.  
- **DLT-Powered Security:** Leveraging Hedera's DLT for immutable records, ensuring transparency and trust without high costs.  
- **Africa-First Design:** Built for low-bandwidth environments, small clinics, and pharmacies, with tokenomics to incentivize reporting fakes.  
- **Impact-Driven:** Prevents deaths, reduces waste, and supports drug-resistant disease control by enabling real-time authenticity checks.

Why Hedera? We chose Hedera for its unparalleled **transparency, speed (certified carbon-negative), low fees**, and scalability – perfect for high-volume transactions in resource-constrained settings. This enables affordable, enterprise-grade DLT without compromising on performance.

## How TraceRx Works
1. **Batch Registration:** Manufacturers upload medicine data via the Admin App, which mints an immutable token on Hedera's network for tamper-proof recording.  
2. **Verification for Smartphones:** Users scan QR codes in the User App for instant authenticity checks. Once scanned, the batch is marked as "verified" – subsequent scans flag potential duplicates or fakes.  
3. **Verification for Feature Phones:** Dial a USSD short code (e.g., `*384#`) to enter a batch ID and receive SMS confirmation – no app or internet needed.  
4. **Backend Integration:** A Node.js + Express API connects verification requests to Hedera for validation and Firebase for real-time storage.  
5. **Reporting and Incentives:** Users report fakes via the app and earn free HBAR tokens, adding a tokenomics layer to encourage community vigilance.

## Key Features
- **Hedera DLT Integration:** Immutable, fast, low-cost record-keeping for drug batches.  
- **QR Code Scanning & Generation:** Instant verification; generates unique batch IDs (MVP: open to all; production: manufacturer-only with scratch-off security).  
- **USSD Access:** Internet-free verification for rural users via short codes like `*384#` (simulated with Python, Ngrok, and a custom flow in Go for reliability).  
- **Fake Medicine Reporting:** Users earn HBAR rewards for reports, tokenizing incentives to build a vigilant ecosystem.  
- **Data Export:** Download verification history as JSON for personal or regulatory use.  
- **Cross-Platform Compatibility:** Works seamlessly on web, mobile (Flutter), and basic phones.  
- **Secure Backend:** Firebase Auth for user management and Firestore for scalable, real-time data.

## Tech Stack
- **Frontend:** Flutter (mobile with QR scanner) + HTML/CSS/JS (web apps).  
- **Backend:** Node.js + Express API.  
- **Database:** Firebase Firestore for real-time storage.  
- **DLT/Blockchain:** Hedera Hashgraph for minting and verifying tokens.  
- **USSD Simulation:** Python with Ngrok and custom Go adaptations (overcame Africa's Talking sandbox issues for robust testing).  

## How TraceRx Outshines Competitors
TraceRx differentiates itself with an Africa-centric, inclusive approach, combining open DLT with user-friendly tools. Here's a comparison:

| Competitor              | Limitations                                      | TraceRx Advantage                              |
|-------------------------|--------------------------------------------------|------------------------------------------------|
| **PharmaLedger (EU)**  | Academic and bureaucratic; no end-user tools     | Instant QR/USSD checks for patients and pharmacies |
| **ScanTrust**          | Proprietary QR; no public DLT                    | Open Hedera DLT + free public verification     |
| **Sproxil (USA/Nigeria)** | Scratch codes; limited traceability              | Immutable DLT trails + USSD/QR hybrid access   |
| **RxAll (Nigeria/USA)**| Closed AI model; no blockchain transparency      | Transparent, open-source DLT; Africa-first design |
| **MediLedger / VeChain / IBM Pharma** | Expensive, corporate-only; not Africa-focused | Affordable, scalable for small clinics; inclusive for all devices |

## Future Opportunities & Roadmap
This MVP focuses on core verification, but we've designed for growth:  
- **Restricted Access:** Limit uploads and QR generation to licensed manufacturers (require license verification).  
- **Enhanced Security:** Mandate scratch-off coatings on QR codes to prevent premature exposure.  
- **Regulatory API:** Provide paid API access for drug control bodies to monitor fake hotspots (e.g., frequent scans/reports by location).  
- **Monetization:** Charge manufacturers for uploads and QR generation; expand tokenomics with more HBAR rewards.  
- **Scalability:** Integrate advanced analytics, AI for pattern detection, and partnerships with African health authorities.  

With endless opportunities in Africa's growing pharma sector, TraceRx is poised to scale into a full ecosystem, driving transparency and saving lives.

**Built for Impact:** TraceRx isn't just tech – it's a lifeline for millions. Let's end the counterfeit crisis together.  

