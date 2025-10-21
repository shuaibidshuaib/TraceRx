
#  TraceRx Admin Portal V2

**Live Demo:** [https://tracerxadmnew.netlify.app](https://tracerxadmnew.netlify.app)

Built with modern tools and intelligent architecture, **TraceRx Admin V2** redefines digital pharmaceutical oversight. By integrating **Hedera Hashgraph’s distributed ledger (DLT)**, **EVM-compatible smart contracts**, and **AI-driven analytics**, this version delivers a transparent, scalable, and secure solution to combat counterfeit drugs in Africa’s supply chain.

---

##  Mission

**"To build a transparent, secure, and inclusive pharmaceutical ecosystem, reducing counterfeit medicine cases by 30% within two years through Hedera’s immutable distributed ledger and AI-powered insights."**

---

##  Core Features

### 1. **Secure Drug Batch Uploads**

* Seamless, multi-step form for uploading verified drug batches.
* Each upload is linked to a **Hedera Consensus Service (HCS)** transaction for **tamper-proof records**.
* Records are stored under **Topic ID:** [0.0.6825354](https://hashscan.io/testnet/topic/0.0.6825354).

### 2. **Manufacturer Verification via Smart Contract**

* Smart contract (EVM-compatible) built on Hedera to verify or revoke manufacturers.
* Verification tied to **HashPack wallet addresses** for legitimacy.
* Every action is permanently recorded for full transparency.

### 3. **AI Counterfeit Analytics**

* Integrated **Flask + scikit-learn** AI model for anomaly detection and counterfeit prediction.
* Real-time **Leaflet maps** and **Chart.js visualizations** display hotspot predictions.

---

##  Design & User Experience

* **Responsive Interface:** Built with **Vite**, **TypeScript**, **React**, and **Tailwind CSS** for a smooth experience.
* **UI Framework:** **shadcn/ui** components for consistency and performance.
* **Accessibility:** High-contrast visuals, keyboard navigation, and lightweight structure.

---

##  Tech Stack

| Layer          | Technology                                       | Purpose                               |
| -------------- | ------------------------------------------------ | ------------------------------------- |
| **Frontend**   | Vite, React, TypeScript, Tailwind CSS, shadcn/ui | UI & state management                 |
| **Backend**    | Node.js, Express                                 | API & contract execution              |
| **AI Service** | Python, Flask, scikit-learn                      | Machine learning & predictions        |
| **DLT Layer**  | Hedera Hashgraph (HCS + EVM)                     | Immutable, decentralized ledger       |
| **Utilities**  | Leaflet.js, Chart.js, XLSX.js                    | Maps, data visualization & processing |
| **Data Layer** | Firestore (mirrored data)                        | Cloud-mirrored records for redundancy |

---

##  System Architecture

* Node.js + Express handles backend logic and communication with Hedera.
* Flask AI microservice processes and predicts counterfeit risks.
* Hedera DLT ensures immutable recordkeeping.
* Firestore mirrors key data for redundancy and quick queries.
* Frontend connects everything through RESTful APIs for real-time sync.

---

##  Getting Started

### Prerequisites

* Node.js v18+
* Python 3.9+
* Hedera Testnet Account → [portal.hedera.com](https://portal.hedera.com)
* HashPack Wallet (Your wallet address is needed)

---

###  Installation Steps

1. **Clone the Repository**

   ```bash
   git clone https://github.com/myusername/tracerx-admin-latest-ui.git
   cd tracerx-admin-latest-ui
   ```

2. **Backend Setup**

   ```bash
   cd backend
   npm install
   cp .env.example .env
   # Add HEDERA_OPERATOR_ID, PRIVATE_KEY, TOPIC_ID
   node server.js
   ```

3. **AI Service Setup**

   ```bash
   cd ../ai-service
   python -m venv venv
   source venv/bin/activate  # or venv\Scripts\activate on Windows
   pip install -r requirements.txt
   pip install flask-cors firebase-admin
   python app.py
   ```

4. **Frontend Setup (Admin UI)**

   ```bash
   cd ../frontend/tracerx-admin-latest-ui
   npm install
   npm run dev
   ```

   Open the app on `http://localhost:5173` (default Vite port).

---

##  Testing Features

* Upload a drug batch (e.g., *Aspirin – BATCH-2025-002*).
* Verify or revoke a manufacturer using their Hedera wallet address.
* Analyze AI results and view predicted counterfeit hotspots on the map.
* Check immutable logs on [Hedera HashScan](https://hashscan.io/testnet/topic/0.0.6825354).

>  **Note:**
> If you want to use the scanner app after uploading a medicine through Admin V2, ensure the API endpoint reads from the `drug_batches` collection instead of the `drug` collection.

---

##  Deployment

* **Frontend:** [Netlify](https://tracerxadmnew.netlify.app)
* **Backend & AI:** Railway or Render
* **DLT:** Hedera Testnet

---

##  Related Links

* **Smart Contract Events (HashScan):** [View Here](https://hashscan.io/testnet/contract/0.0.6825354)
* **HCS Topic Logs:** [View Here](https://hashscan.io/testnet/topic/0.0.6825354)
* **Pitch Deck:** [TraceRx Pitch Deck](https://drive.google.com/file/d/1-X2itzViID5xqROR5f_LRDWW4qhdLl2C/view?usp=sharing)
* **Certificate:** [View Certificate](https://drive.google.com/file/d/1DNiF-e7p94Zows00-w_X-YJdMNURQHAu/view?usp=sharing)

