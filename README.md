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

### 3. Start Ganache (or another local Ethereum node)

### 4. Deploy the Smart Contract
Use Remix or Truffle to deploy `SmartContracts/smartcontract.sol`. Save the ABI and contract address.

### 5. Create the SQLite Database
```bash
python decoding/createdb.py
```

### 6. Start the Flask App
```bash
python decoding/app.py
```

---

## 📂 Project Structure

```
blockchain-network-security-audit/
│
├── intercept.py                  # Script to intercept network events
├── decoding/
│   ├── app.py                    # Flask backend
│   ├── createdb.py               # DB init script
│   ├── users.db                  # SQLite DB
│   ├── static/                   # CSS & JS
│   └── templates/                # HTML templates
├── SmartContracts/
│   ├── smartcontract.sol         # Solidity smart contract
│   ├── SmartContract.abi         # ABI for interacting with contract
│   └── SmartContract.bin         # Compiled bytecode
└── README.md
```

---

## 👨‍💻 Authors

- **Vikash Chauhan** – Team Leader  
- **Gurdeep Singh**
- **Dharmesh Jethva**  
Client: Dr. Alex Wenjie Ye, VU Melbourne

---


