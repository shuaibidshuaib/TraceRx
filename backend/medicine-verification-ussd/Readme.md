
This project is a USSD-based drug verification system built with **FastAPI**, integrated with **Firebase** for drug metadata and **Hedera Hashgraph** for on-chain verification.

## 📦 Project Structure

```
medicine-verification-ussd/
├── main.py                  # FastAPI app entry point
├── firebase_utils.py        # Firebase Firestore integration
├── hedera_utils.py          # Hedera verification logic
├── serviceAccountKey.json   # Firebase credentials (DO NOT SHARE PUBLICLY)
├── .env                     # Environment variables
├── requirements.txt         # Python dependencies
├── venv/                    # Virtual environment (optional)
└── ext/, __pycache__/       # Internal folders
```



##  How to Run Locally

###  Requirements
- Python 3.9+
- pip
- I used flow sim simulator, ive to reprogram some parts of the program using go programming langauge,html,css and js.
 africastalking.com, ussd sandbox gave me a lot of issues.


### Setup Instructions

1. **Create a virtual environment (optional but recommended)**  
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

2. **Install dependencies**  
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the FastAPI server**  
   ```bash
   uvicorn main:app --reload
   ```

4. **Open FlowSim: Universal USSD Simulator and set the USSD endpoint to**  
   ```
   http://localhost:8000/ussd
   ```

---

## Testing the Flow

1. Dial `*384` in FlowSim.
2. Enter a valid drug batch ID .
3. You should see a response like:
   ```
   {
  "batchId": "BATCH12345",
  "name": "Paracetamol",
  "expiryDate": "2026-08-15",
  "manufacturer": "XYZ Pharma"
   }

   ```

---

## Firebase Setup

- Ensure your Firestore has a `drugs` collection.
- Each document ID should match a batch ID (e.g., `ABC123`) and contain fields for e.g:
  ```json
 {
  "batchId": "BATCH12345",
  "name": "Paracetamol",
  "expiryDate": "2026-08-15",
  "manufacturer": "XYZ Pharma"
}

 ## Hedera Integration

- The `hedera_utils.py` file contains placeholder logic.
- Replace it with actual Hedera SDK calls to verify drug authenticity on-chain.

## ⚠️ Security Notes

- Do **not** expose `serviceAccountKey.json` publicly.
- Use `.env` for secrets in production.


