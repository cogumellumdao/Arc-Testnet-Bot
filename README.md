<img width="2400" height="268" alt="yooo (1)" src="https://github.com/user-attachments/assets/3735d26c-e1dc-4aa2-80e6-6462db746c21" />

# 🚀 Arc Testnet Bot

**Developed by Cogumellum**

A simple, straightforward, and multi-wallet automation bot for the Arc Testnet. It allows you to perform the main testnet interactions (Mint, Deploy, Register) automatically for all your wallets, without relying on API keys.

## ✨ Features

  * ✅ **Simple and Direct** - Focused only on the essentials.
  * ✅ **Fully Functional** - Executes Mint + Deploy + Register.
  * ✅ **Multi-Wallet** - Automatically processes all wallets from your `pv.txt` file.
  * ✅ **Proxy Support** - Native proxy support for each wallet.

-----

## 📋 Requirements

Before you start, you will need two essential programs installed on your computer:

1.  **[Node.js](https://nodejs.org/en/download/)**: Required to run the bot script (LTS version 18+ is recommended).
2.  **[Git](https://www.google.com/search?q=https://git-scm.com/downloads)**: Required to download the files from the GitHub repository.

-----

## 🚀 Installation Guide (For Beginners)

Follow these steps exactly to set up and run the bot from scratch.

### 1️⃣ Step 1: Open your Terminal (CMD)

You need a command-line interface to run the bot.

  * **On Windows**:
    1.  Press the `Windows Key + R` on your keyboard.
    2.  Type `cmd` and press `Enter`.
  <img width="1654" height="822" alt="image" src="https://github.com/user-attachments/assets/9fad2253-aa80-4104-a5e7-669732c7cc7b" />

Or you can simply click the `Windows Key` and type `cmd`.
<img width="1194" height="769" alt="image" src="https://github.com/user-attachments/assets/7862d62e-4854-4166-9298-d83ef95dcfac" />

### 2️⃣ Step 2: Download the Bot Files

Now, let's download (clone) the files from GitHub.

1.  Clone the GitHub repository:

    ```bash
    git clone https://github.com/cogumellumdao/Arc-Testnet-Bot.git .
    ```
<img width="927" height="179" alt="image" src="https://github.com/user-attachments/assets/209d17b0-6c77-48aa-a503-1f3789f1e91f" />

2.  In the terminal you just opened, create a folder for the bot and enter it. You can copy and paste these commands:

    ```bash
    cd Arc-Testnet-Bot
    ```
    <img width="502" height="108" alt="image" src="https://github.com/user-attachments/assets/8b33c545-a6b2-44b1-8503-0153f5b0925b" />


    *(Note: The `.` at the end downloads the files directly into your current folder.)*
    <img width="1203" height="327" alt="image" src="https://github.com/user-attachments/assets/8dd02af3-c14f-4bc9-a9dd-4a729cbfff39" />


### 3️⃣ Step 3: Install Dependencies

The bot needs some libraries (packages) to work.

1.  Still inside the `Arc-Testnet-Bot` folder in your terminal, run the following command to install everything needed:
    ```bash
    npm install ethers readline fs https http https-proxy-agent dotenv
    ```
<img width="1009" height="179" alt="image" src="https://github.com/user-attachments/assets/829b2b3d-98ce-44cd-807e-9acc4354231f" />

2.  Wait for the installation to complete.

### 4️⃣ Step 4: Configure Your Wallets

This is the most important part. You need to tell the bot which wallets to use.

1.  In the same folder where the bot files are (e.g., `Arc-Testnet-Bot`), create a new text file named `pv.txt`.

2.  Open this `pv.txt` file with a text editor (like Notepad).

3.  Add your private keys, one per line, in the format:
    `PRIVATE_KEY:WALLET_NAME`

    **Example `pv.txt`:**

    ```
    0xYourVeryLongPrivateKey123:MyWallet1
    0xAnotherSuperSecretPrivateKey456:MyWallet2
    0xOneMoreKey789abc:JohnsWallet
    ```
<img width="749" height="283" alt="image" src="https://github.com/user-attachments/assets/1de218e2-4a21-4e9a-b146-58555eeb9923" />

    *(**Optional - With Proxy**): If you want to use proxies, the format is `45.3.xxx.xxx:xx`*

    ```
    45.3.xxx.xxx:xx
    104.xxx.xxx.xx:xxxx
    154.xxx.xxx.xx:xxx
    ```

    *You can also use a `proxy.txt` file (see the advanced configuration section).*

-----
<img width="635" height="309" alt="image" src="https://github.com/user-attachments/assets/fa3ab79d-faed-44f0-a8e5-e607e0cb5ff4" />

## 🎯 How to Use (Recommended Flow)

After installation and setup, using the bot is simple:

### 1\. Get Test Tokens (Faucet)

Your wallets need funds to pay for "gas" (transaction fees) on the testnet.

1.  In your terminal, inside the bot's folder, run:
    ```bash
    node arc-bot.js
    ```
2.  From the main menu, choose **Option 4: 💧 Manual Faucet Guide**.
3.  The bot will show the address for your first wallet and the instructions.
4.  Go to the site: **[https://faucet.circle.com/](https://faucet.circle.com/)**
5.  Select the **Arc Testnet** network, paste your wallet address, and request the tokens.
6.  The Circle faucet has a limit (usually 1 request per hour per IP/address).
7.  Go back to the bot, press Enter to see the next wallet, and repeat the process for all of them.
<img width="1748" height="921" alt="image" src="https://github.com/user-attachments/assets/f1845c1e-6a6d-4e4a-a728-c37dcade25e8" />

### 2\. Run the Bot (AUTO ALL)

After your wallets have a balance (testnet ETH), you can run the automation.

1.  Start the bot (if not already open):
    ```bash
    node arc-bot.js
    ```
2.  From the main menu, choose **Option 5: 🚀 AUTO ALL**.
3.  The bot will:
      * Check the balance of all wallets in `pv.txt`.
      * Ask if you want to proceed only with the ones that have a balance.
      * Execute the 3 operations (Mint NFT, Deploy Token, Register Name) for each valid wallet, one after the other.
4.  Sit back and let the bot work\!

-----

## 📋 Main Menu

```
════════════════════════════════════════════════════════════
                     MAIN MENU
════════════════════════════════════════════════════════════
1. Mint NFT
2. Deploy Token
3. Register Name
4. 💧 Manual Faucet Guide
5. 🚀 AUTO ALL (Check + Mint + Deploy + Register)
6. Check All Balances
7. View Statistics
8. Exit
════════════════════════════════════════════════════════════
```

### Option Details

  * **1. Mint NFT**: Mint a standard testnet NFT. You can choose how many transactions to make per wallet.
  * **2. Deploy Token**: Create and deploy a new ERC20 token on the testnet. You define the name, symbol, and supply.
  * **3. Register Name**: Register a domain name on the Arc Name Service (similar to ENS).
  * **4. 💧 Manual Faucet Guide**: A step-by-step guide to get test tokens (ETH and USDC) from the official Circle faucet.
  * **5. 🚀 AUTO ALL**: The main function. Checks balances and runs Mint, Deploy, and Register for all valid wallets.
  * **6. Check All Balances**: Checks and displays the ETH balance for all wallets in your `pv.txt`.
  * **7. View Statistics**: Shows stats for the current session (total transactions, successes, failures, etc.).
  * **8. Exit**: Quits the bot.

-----

## ⚙️ Advanced Configuration

### File Structure

```
arc-bot-project/
├── arc-bot.js         # The main bot script
├── pv.txt             # (REQUIRED) Your private keys
├── proxy.txt          # (OPTIONAL) List of proxies
└── README.md          # This file
```

### `proxy.txt` File (Optional)

If you prefer to manage proxies in a separate file (instead of in `pv.txt`), create `proxy.txt`. The bot will rotate through this list for each wallet.

**Format (one per line):**

```
ip:port
ip:port:user:pass
```

### Code Adjustments

You can edit the `arc-bot.js` file to change advanced settings (lines \~26-32):

```javascript
const CONFIG = {
  MIN_BALANCE: 0.001,       // Minimum ETH balance required to run
  RETRY_ATTEMPTS: 3,        // Retries per operation
  RETRY_DELAY: 5000,        // Delay between retries (5s)
  TX_WAIT_TIME: 10000,      // Wait for TX confirmation (10s)
};
```

-----

## 🛡️ Security

⚠️ **VERY IMPORTANT:**

  * **NEVER** share your `pv.txt` file or your private keys with anyone.
  * The author is not responsible for any lost funds. This bot is intended for use on the **TESTNET** only.
  * If you use GitHub to store your code, add `pv.txt` and `proxy.txt` to your `.gitignore` file to avoid accidentally uploading them to the internet.
## ❓ Troubleshooting

  * **Error: "Limit exceeded" at the faucet**

      * **Cause:** You requested tokens less than 1 hour ago.
      * **Solution:** Wait for 1 full hour and try again.

  * **Error: "Insufficient balance" in the bot**

      * **Cause:** The wallet does not have enough testnet ETH.
      * **Solution:** Use **Option 4** and get more tokens from the faucet.

  * **Error: "Invalid private key"**

      * **Cause:** The private key in `pv.txt` is formatted incorrectly (e.g., has spaces, is missing `0x`, etc.).
      * **Solution:** Double-check your `pv.txt` file and correct the key.

  * **Error: Transaction Failed**

      * **Cause:** The network is busy, or there was insufficient gas.
      * **Solution:** The bot will retry automatically (up to `RETRY_ATTEMPTS`). If it keeps failing, try again later.
