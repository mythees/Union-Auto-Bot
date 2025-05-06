# Union Testnet Auto Bot - 🚀
## 📢 Join Our Community

# Telegram Channel: .[Channel](https://t.me/Offical_Im_kazuha)
# GitHub Repository: [Union](https://github.com/Kazuha787/Union-Auto-Bot.git)

Welcome to the **Union Testnet Auto Bot - KAZUHA**! 🎉 This is a powerful Node.js script designed to automate transactions on the Sepolia to Holesky bridge using the Union Testnet. The script features a sleek, real-time dashboard built with `blessed` and `blessed-contrib` to monitor transactions, wallet information, and network performance. It supports multiple wallets, USDC approvals, and detailed logging for a seamless user experience. 🛠️

---

## ✨ Features

- **Automated Transactions** 🤖: Sends transactions from multiple wallets on the Sepolia to Holesky bridge.
- **Real-Time Dashboard** 📊: Displays transaction logs, wallet balances, transaction performance, and network status using a terminal-based UI.
- **Multi-Wallet Support** 🔑: Reads wallet data from a `wallet.json` file to process transactions for multiple accounts.
- **USDC Approval Handling** 💰: Automatically checks and approves USDC allowances for the bridge contract.
- **Transaction Monitoring** 📡: Tracks transaction status (success, failed, pending) and performance metrics (time in ms).
- **Error Handling** 🚨: Robust error handling with detailed logs for debugging and user feedback.
- **Customizable** ⚙️: Allows users to specify the number of transactions per wallet via an interactive prompt.
- **Visual Analytics** 📈: Includes charts (line, donut, gauge) to visualize transaction performance and network usage.

---

## 🛠️ Prerequisites

Before running the script, ensure you have the following:

- **Node.js** (v16 or higher) 🟢
- **npm** (Node Package Manager) 📦
- A valid `wallet.json` file with wallet details (private keys and optional names) 🔐
- Access to a Sepolia RPC provider 🌐
- USDC funds in the wallets for transactions 💸
- Terminal or command-line interface 🖥️

---

## 📦 Installation

Follow these steps to set up the project:

1. **Clone the Repository** 📥
   ```bash
   git clone https://github.com/Kazuha787/Union-Auto-Bot.git
   cd Union-Auto-Bot
   ```
   **Install Dependencies**
   ```
    npm install
   ```

    ## 🛠️ Setup: Create wallet.json

1. **Create the File** 📄  
   In the project root, create a file named `wallet.json`.

2. **Add Wallet Details** 🔐  
   Use the following JSON structure to define your wallets. Each wallet needs a `name` (optional) and a `privatekey` (required). Example:
   ```json
   {
     "wallets": [
       {
         "name": "Wallet1",
         "privatekey": "0xYourPrivateKeyHere"
       },
       {
         "name": "Wallet2",
         "privatekey": "0xAnotherPrivateKeyHere"
       }
     ]
   }
   ```
   ⚠️ ***Warning***
   - Keep `wallet.json` secure and never share your private keys
   - Configure RPC Provider 🌐 The script uses `https://1rpc.io/sepolia` by default.
   - To use a different provider, update the rpcProviders array in the script.
   🚀 ***Usage Of Script** 
   - Enter Transaction Count 🔢 When prompted,
   - Input the number of transactions to send per wallet (e.g., 5).
   - Monitor the Dashboard 📊 The terminal will display a real-time dashboard with
   - Transaction Logs: Success, failure, and pending transaction updates.
   ***Wallet Information**
   - Wallet names, addresses, and USDC balances.Transaction Performance
   - Line chart showing transaction times (ms).
   ***Transaction Status***
   - Donut chart displaying success/failed/pending ratios
   **Network Usage***
   - Gauge showing network status
   ***System Information***
   - Current time, network details, and gas prices.
   - Exit the Script 🛑 Press Q, ESC, or Ctrl+C to exit the application.
## Run The Script 
```
node main.js
```

## File Structure

```
Union-Auto-Bot
├── index.js           # Main script with bot logic and dashboard UI
├── wallet.json        # Wallet configuration file (user-created)
├── package.json       # Project metadata and dependency list
├── node_modules/      # Installed Node.js dependencies
└── README.md          # Project documentation
```

## 🖥️ Dashboard Components

The bot features a terminal-based dashboard built with `blessed` and `blessed-contrib`, providing real-time insights:

- **Transaction Logs** 📜  
  Displays live updates for transaction events (success ✅, errors 🚨, pending ⏳) with color-coded messages.

- **Wallet Information Table** 📋  
  Shows wallet names, truncated addresses (e.g., `0x123...abc`), and USDC balances in a tabular format.

- **Transaction Performance Chart** 📈  
  A line chart tracking transaction execution times (in milliseconds) for performance analysis.

- **Transaction Status Donut** 🍩  
  A donut chart visualizing the ratio of successful, failed, and pending transactions.

- **Network Usage Gauge** 📏  
  A gauge indicating network status as a percentage, simulating real-time network health.

- **System Information Panel** ℹ️  
  Displays current time (Asia/Jakarta timezone), network details (Sepolia), gas prices, and API health.

🔧 The dashboard updates every 10 seconds for system info and in real-time for transaction events.


## 🛠️ Dependencies

The script relies on the following Node.js packages:

- **`ethers` (^6.0.0)**: Interacts with Ethereum wallets and smart contracts (e.g., USDC, bridge contract).
- **`axios` (^1.0.0)**: Makes HTTP requests to the Union GraphQL API for packet hash polling.
- **`moment-timezone` (^0.5.0)**: Handles timestamps and timezone formatting (Asia/Jakarta).
- **`blessed` (^0.1.0)**: Creates the terminal-based UI framework for the dashboard.
- **`blessed-contrib` (^4.0.0)**: Provides widgets like charts, gauges, and tables for the dashboard.
- **`fs` & `path`**: Built-in Node.js modules for file system operations (e.g., reading `wallet.json`).

Install dependencies with:  
```bash
npm install ethers axios moment-timezone blessed blessed-contrib
```
 ## ⭐ Star this repository if you find it helpful
📩 For questions or feedback, open an issue on GitHub.
