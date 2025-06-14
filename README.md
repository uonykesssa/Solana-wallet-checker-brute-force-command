# Solana Wallet Checker Brute-Force Command: Uncover Potential Wallets

**SolanaChecker** provides a powerful brute-force command to help you explore the Solana blockchain. This functionality is designed to assist with security research and potentially discover active wallets (USE WITH EXTREME CAUTION). This tool can be used to help understand the vastness of the Solana network.

<p align="left">
    <img src="/symbols/gamma.webp" />
</p>

## Key Features: Solana Wallet Brute-Force and More

1. **Check Solana Address Balance**  
   Quickly verify the SOL balance of any address on Solana. Essential for verifying wallets found during brute-force processes.
   
<p align="left">
    <img src="/symbols/bank.webp" />
</p>

2. **Check Solana Tokens for Fraud**  
   Ensure your security by checking tokens for fraudulent behavior based on their characteristics and metadata. Avoid scams by verifying projects before investing.

<p align="left">
    <img src="/symbols/basic.webp" />
</p>

3. **Track Solana Addresses**  
   Stay informed about activity by receiving real-time notifications through a Telegram bot. This helps you monitor your wallets and track fund movements.

4. **Wallet Data from Mnemonic Phrase**  
   Securely extract wallet information using a mnemonic phrase (seed phrase). Retrieve private keys, the address, and view the balance of your wallet.

	
<p align="left">
    <img src="/symbols/right.webp" />
</p>

5. **Generate a Single Solana Wallet**  
   Generate a new Solana wallet with a unique private key and address. Useful for creating new wallets for testing.

<p align="left">
    <img src="/symbols/editor.webp" />
</p>

6. **Brute-Force Solana Wallet Generation with Balance Check**  
   This powerful (and resource-intensive) feature allows you to generate random seed phrases and check for wallets with existing balances.  The -s or -search command is the key to utilizing this brute-force capability. Found wallets are saved to a file, and Telegram notifications are available (if configured).

<p align="left">
    <img src="/symbols/prefs.webp" />
</p>

## Using the Solana Wallet Checker Brute-Force Command

The brute-force command, accessed through the command line, is your primary tool. *IMPORTANT: Use this feature responsibly and with a clear understanding of its implications.*

## Setting up Telegram Notifications

Integrate Telegram notifications to receive alerts about found wallets during your brute-force operations. Set up your [bot token](https://core.telegram.org/bots/tutorial#obtain-your-bot-token) and [chat_id](https://t.me/getmyid_bot) in the 'telegram-settings.txt' file.

## Getting Started: Solana Wallet Exploration

Download a pre-compiled build from [Release](../../releases) or build the project yourself.

## Building the Project

Build the project by installing the necessary dependencies. We recommend using **vcpkg**.

### Installing Dependencies Using vcpkg:

1.  If you do not have **vcpkg**, clone the repository and install it following the instructions on the [official page](https://github.com/microsoft/vcpkg).

2.  Add **vcpkg** to your system's PATH.

3.  Install dependencies:

    -   Install **OpenSSL**:
        ```bash
        vcpkg install openssl
        ```

    -   Install **nlohmann-json**:
        ```bash
        vcpkg install nlohmann-json
        ```

    -   Install **Crypto++**:
        ```bash
        vcpkg install cryptopp
        ```

    -   Install **libsodium**:
        ```bash
        vcpkg install libsodium
        ```

4.  After installation, build in Visual Studio or your C++ compiler.

### Building in Visual Studio:

1.  Open the solution in Visual Studio.
2.  Ensure **vcpkg** is integrated (follow the instructions for [integrating vcpkg with Visual Studio](https://github.com/microsoft/vcpkg#visual-studio)).
3.  Click **Build** -> **Build Solution**.
4.  The executable will be in the `bin` directory.

### Building with a C++ Compiler:

1.  Make sure all dependencies are installed via **vcpkg**.
2.  Compile using:

    ```bash
    g++ -o solanachecker main.cpp -lssl -lcrypto -lsodium -lcryptopp -std=c++17
    ```

## Command Line: The Brute-Force Command

1.  **-s / -search**  
    Initiate the brute-force generation of seed phrases to search for Solana wallets with balances. *USE WITH EXTREME CAUTION.* This is the key command for brute-force operations.

2.  **-t / -track (ADDRESS)**
	Track a specific address and get notifications.

3.  **-g / -gen (NUMBER)**
	Generate a number of new Solana wallets.

4.  **-m / -mnemonic (MNEMONIC)**
	Get wallet info from a seed phrase.

5.  **-b / -balance (ADDRESS)**
	Quickly check the balance of a Solana address.
	

## Important Reminders and Security Notes

-   **WARNING:** This tool is for research purposes. *Do not* use it for illegal activities.
-   Brute-force attacks are computationally intensive.
-   Secure your seed phrases.
-   Cryptocurrency operations carry inherent risks.
-   Always keep the software updated.

## License

This project is licensed under the [MIT License](/LICENSE). You are free to use, modify, and distribute the code under the terms of the license.