# 🔐 Blockchain-Based Network Security Audit Trail

This project is a final-year capstone solution that uses **Ethereum blockchain** and **Python (Flask)** to build a **tamper-proof audit trail** for network security events. It captures, stores, and displays immutable logs from firewalls, IDS/IPS, and other network components.

---

## 📌 Key Features

- 🔒 **Immutable Logs** using Ethereum Smart Contracts
- 🧪 **Real-Time Event Monitoring**
- 👥 **Role-based Access** (Admin, Analyst)
- 🗂️ **SQLite Database** for user authentication
- 📊 **Flask UI** for viewing and exporting logs
- 📎 Integration with tools like mitmproxy, SIEM, etc.

---

## 🧰 Technology Stack

| Layer         | Tools / Languages                |
|---------------|----------------------------------|
| Backend       | Python, Flask                    |
| Blockchain    | Ethereum, Solidity, Web3.py      |
| UI            | HTML, CSS, JavaScript (Flask)    |
| Database      | SQLite                           |
| Dev Tools     | Ganache, Remix, Truffle (optional) |
| Container (opt) | Docker, Kubernetes (optional)  |

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/VikashSecures/blockchain-network-security-audit.git
cd blockchain-network-security-audit
```

### 2. Install Requirements
```bash
pip install -r requirements.txt
```

---

## ⚙️ 3. Setup Local Ethereum Network with Ganache

1. **Download & Install Ganache**  
   👉 https://trufflesuite.com/ganache

2. **Start Ganache GUI**  
   - Create a new workspace or quickstart
   - Copy the RPC URL (e.g., `http://127.0.0.1:7545`)

3. **Note down:**
   - One of the account addresses
   - Its private key
   - The network RPC URL

---

## 📜 4. Deploy the Smart Contract

### ✅ Option A: Remix IDE (Easiest)
1. Go to https://remix.ethereum.org
2. Create a new file `smartcontract.sol` and paste your contract from `SmartContracts/`
3. Compile the contract
4. Deploy using "Injected Web3" (connects to Ganache)

### ✅ Option B: Truffle CLI (Advanced)
1. Install Truffle:
```bash
npm install -g truffle
```
2. Create a Truffle project and copy `smartcontract.sol` into `contracts/`
3. Configure `truffle-config.js` with Ganache RPC
4. Run:
```bash
truffle migrate --network development
```

---

## 🔗 5. Update Python Code

In `read.py` or Flask app, update:
- Contract Address (from Remix/Truffle)
- ABI (from `SmartContracts/SmartContract.abi`)
- RPC URL (`http://127.0.0.1:7545`)

### ✅ Example (Python)
```python
from web3 import Web3
import json

web3 = Web3(Web3.HTTPProvider("http://127.0.0.1:7545"))

contract_address = "0xYourContractAddress"
with open("SmartContracts/SmartContract.abi", "r") as abi_file:
    abi = json.load(abi_file)

contract = web3.eth.contract(address=contract_address, abi=abi)
```

---

## 🧪 6. Create the SQLite Database
```bash
python decoding/createdb.py
```

## 🚀 7. Start the Flask App
```bash
python decoding/app.py
```

---

## 📂 Project Structure

```
blockchain-network-security-audit/
│
├── intercept.py
├── decoding/
│   ├── app.py
│   ├── createdb.py
│   ├── users.db
│   ├── static/
│   └── templates/
├── SmartContracts/
│   ├── smartcontract.sol
│   ├── SmartContract.abi
│   └── SmartContract.bin
├── requirements.txt
└── README.md
```

---

## 👨‍💻 Authors

- **Vikash Chauhan** – Team Leader  
- **Gurdeep Singh**
- **Dharmesh Jethva**  
Client: Dr. Alex Wenjie Ye, VU Melbourne

---

