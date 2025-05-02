# Crypto-Price-Tracker-CLI-tool-in-Python-
Crypto Price Tracker (CLI tool in Python)
crypto-price-tracker/
├── crypto_tracker.py
├── requirements.txt
└── README.md
import requests

def get_price(symbol):
    url = f"https://api.coingecko.com/api/v3/simple/price?ids={symbol}&vs_currencies=usd"
    response = requests.get(url)

    if response.status_code == 200:
        data = response.json()
        if symbol in data:
            price = data[symbol]['usd']
            print(f"The current price of {symbol.upper()} is ${price}")
        else:
            print("Cryptocurrency not found.")
    else:
        print("Error fetching data from CoinGecko.")

if __name__ == "__main__":
    coin = input("Enter the cryptocurrency (e.g., bitcoin, ethereum): ").lower()
    get_price(coin)
requests
# 🪙 Crypto Price Tracker (CLI)

A simple Python tool to get the current price of any cryptocurrency using the CoinGecko API.

## 🚀 Features
- Fetches live prices in USD
- Works in the command line
- Minimal and clean Python code

## 🛠️ How to Use
1. Clone the repo  
```bash
git clone https://github.com/yourusername/crypto-price-tracker.git
cd crypto-price-tracker
pip install -r requirements.txt
python crypto_tracker.py
Enter the cryptocurrency (e.g., bitcoin, ethereum): bitcoin  
The current price of BITCOIN is $64250

---

### ✅ Next Step: Upload to GitHub
1. **Create a new repo** at [github.com/new](https://github.com/new)  
   Name it: `crypto-price-tracker`

2. **On your computer:**
```bash
git init
git remote add origin https://github.com/yourusername/crypto-price-tracker.git
git add .
git commit -m "Initial commit"
git push -u origin master
