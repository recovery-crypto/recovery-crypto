# WalletGen – Your Solution for Crypto Recovery and Finding Lost Funds

**WalletGen** is a powerful, open-source **crypto wallet** tool engineered to assist in the recovery of lost or inaccessible digital assets. It facilitates the generation, search, and potential retrieval of lost or inactive **Bitcoin (BTC)**, **Ethereum (ETH)**, **BNB**, **Polygon (MATIC)**, and other **EVM-compatible wallets**, employing real-time balance verification and a high-performance C++ engine.

<!--
Meta description:
WalletGen offers a high-speed, open-source solution for crypto recovery, utilizing brute-force methods to help you find lost or inaccessible Bitcoin, Ethereum, and other EVM-compatible wallets. Learn how to recover your crypto.
-->

## Quick Navigation
- [How It Works](#how-it-works)
- [Why WalletGen](#why-walletgen)
- [Features](#features)
- [Download WalletGen](#how-to-start)
- [Database Download](#download-and-use-database-for-more-speed)
- [The Program Found a Wallet - What Next?](#the-program-found-a-wallet--whats-next)
- [Recovery Your Bitcoin Wallet](#recovery-your-bitcoin-wallet)
- [My Finds](#my-finds)
- [FAQ](#-frequently-asked-questions-faq)
- [Build Instructions](#building-the-project)
- [Donate](#donate)

[![platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux%20%7C%20Android-blue)](https://github.com/tony-dev1/wallets-finder/releases/tag/walletgen)
![build](https://img.shields.io/badge/build-passing-brightgreen)
![discord](https://img.shields.io/badge/discord-tonydevbtc-blue.svg?logo=discord&label=discord)
[![x](https://img.shields.io/badge/@tonydevbtc-black.svg?logo=x)](https://x.com/tonydevbtc)

<p align="center">
    <img width="1000" alt="Crypto Recovery Tool" title="WalletGen Crypto Recovery" height="460" src="/resources/break.webp" />
</p>

⚠️ **Disclaimer**: WalletGen is a research and educational tool. It is not intended for unauthorized access or malicious activity. Use it responsibly and only with wallets you own or have permission to access.

## How It Works

WalletGen leverages standard protocols, including [BIP39](https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki), [BIP44](https://github.com/bitcoin/bips/blob/master/bip-0044.mediawiki), and [Bech32](https://en.bitcoin.it/wiki/Bech32) for Bitcoin wallet generation. For EVM-based blockchains, such as Ethereum, it uses [Keccak256](https://emn178.github.io/online-tools/keccak_256.html) hashing.

The software systematically generates potential wallet addresses and compares them against existing databases or performs real-time balance checks through public blockchain explorers. This mechanism is designed to identify wallets with existing funds.

Wallet Gen is built in C++ and is open-source, allowing users to access and customize the code. When compared to Python-based wallet tools, Wallet Gen provides notably faster wallet generation speeds, mainly utilizing the power of your CPU & GPU.

##  Why WalletGen?

If you're seeking to potentially recover lost cryptocurrency, **WalletGen** provides an efficient and powerful solution. Engineered in C++ and optimized for multi-threaded CPU and GPU utilization, it delivers performance that can be **up to 10x faster** than alternative brute-force tools. Whether you're exploring forgotten wallets, assessing key spaces, or seeking to recover your own assets, WalletGen provides the speed and effectiveness necessary.

## Features

-   **Cryptocurrency Wallet Generation:** Allows for straightforward creation of Bitcoin, Ethereum, BNB, MATIC, and other cryptocurrency wallets.
-   **Balance-Based Wallet Search:** Employ brute-force techniques to seek out existing wallets containing funds on both Bitcoin and EVM networks.
-   **Extensive Algorithm Support:** Supports Keccak256 for EVM wallets and BIP39, BIP44, Bech32 for Bitcoin, ensuring broad compatibility.
-   **Database Integration for Enhanced Speed:** Integrate downloadable databases to accelerate searches for wallets with balances, vastly improving efficiency.
-   **High-Performance Operation:** Wallet Gen is designed to harness both CPU and GPU capabilities, ensuring optimal performance.
-   **Bitcoin Wallet Recovery:** Provides capabilities to recover your Bitcoin wallet using a seed phrase (mnemonic phrase).

## Supported Blockchains

-   Bitcoin (BTC)
-   Ethereum (ETH)
-   Binance Smart Chain (BNB)
-   Any EVM-compatible chain

# Demo

<p align="center">
    <img width="1000" height="460" alt="WalletGen demo on Windows" title="WalletGen Recovery Demo" src="/resources/init.webp" />
</p>


<p align="center">
    <img width="1000" height="460" alt="WalletGen demo on Linux" title="WalletGen Recovery on Linux" src="/resources/transparent.webp" />
</p>

# How to start

## Windows 
- Download [Release](../../releases) 
- Unpack anywhere
- Run `WalletGen.exe`

Or Just Download [Installer](../../releases)

## Linux (x86-64bit)

Use wget 
or download [Release for Linux](../../releases) 







## How to Search for Lost Bitcoin & Ethereum Wallets with Balance

**Wallet Gen** lets you use brute-force methods to search for crypto wallets with balances.

### For Bitcoin (BTC) wallets:

*   Press key 3 in the menu or execute start_search_btc.bat to search Bitcoin wallets over the internet. This process might take longer as it uses real-time balance checks through blockchain explorers.
*   Press key 6 to search Bitcoin wallets using a database. This accelerates the search, comparing generated wallets against a pre-compiled database of known addresses with balances.

### For EVM wallets (Ethereum, BNB, MATIC, etc.):

*   Press key 5 or run start_search_evm.bat to search EVM wallets via the internet. This method verifies balances in real-time via blockchain explorers.
*   Press key 6 to search for EVM wallets using the database. This is more efficient, comparing generated wallets against a database of addresses known to have balances.

### Speed Considerations:

*   The speed of your search is significantly impacted by your hardware, especially the GPU. To enhance speed and improve your chances of discovering a wallet with a balance, you can run multiple program instances (from 1 to 4), dependent on your system's performance.

By leveraging the database, you greatly improve search effectiveness, as it removes the need to query the blockchain for every generated wallet.

## The Program Found a Wallet — What’s Next?

When the program identifies a wallet with a balance:
*   It will **immediately stop** the search.
*   It will **display** wallet details in the console.
*   It will **save** this data in the ``found_wallets.txt`` file.

### Accessing the Funds:
1.  Import the **mnemonic seed phrase** from the found wallet into a compatible crypto wallet (e.g., Metamask, Trust Wallet, or Electrum).
2.  Once restored, you will be able to move the funds to your own wallet.

> If a successful discovery is made, please consider sharing a small portion of the found balance! Thank you!

## Recovery Your Bitcoin Wallet

WalletGen has features that allow you to recover your Bitcoin wallet through the seed phrase (mnemonic phrase). The program supports inputting a complete seed phrase as well as searching for missing words by using specific characters.

### Process Explanation

#### Searching for Missing Words:

If you’re missing words or are uncertain about your seed phrase, replace the unknown words with an *. WalletGen will then search all possible variations to find the correct seed phrase, and restore the associated wallet balance.

#### Entering a Complete Seed Phrase:

If you possess the complete 12-word seed phrase, simply enter it into the program. WalletGen will generate all address types (Legacy, SegWit, P2SH) and check their balances.

![recovery](/resources/home.webp)

### Important Recommendations

*   Seed phrase should consist of precisely 12 words.
*   Use the * symbol solely for designating missing words.
*   Searching for missing words can be a time-consuming process, especially if several words are unknown.
*   If wallet recovery with a balance is successful, the program will immediately halt and save the information.

## My Finds

![mywallet](/resources/sketch.webp)

I've personally recovered two BTC wallets with a balance. The first had 0.000032 BTC, while the second contained 0.0528 BTC (approximately $4800 at the time of discovery).
Here’s the link to the wallet: [bc1qk3m62hx2hh5mhvc0tj45f9xflzcnu0sur3rvay](https://mempool.space/address/bc1qk3m62hx2hh5mhvc0tj45f9xflzcnu0sur3rvay).

<p align="center">
    <img width="1000" height="460" alt="WalletGen found first bitcoin wallet" title="WalletGen found first bitcoin wallet" src="/resources/menu.webp" />
</p>

### New Find 4/9/2025

After a week of continuous searching, I found a [wallet](https://mempool.space/address/bc1q29c5m3w4jxtsj4vcd2ccw4t68xm8m7vs5vytu0) with 0.25 bitcoin ($19k). This is my 4th and biggest find to date.

![image](/resources/report.webp)

## New Find 5/5/2025

[bc1qpm0k3kcmthwsa4zseh33g3hl7eju8u8nkt83kp](https://mempool.space/address/bc1qpm0k3kcmthwsa4zseh33g3hl7eju8u8nkt83kp)

![image](/resources/color.webp)


## Building the Project

1. Open the project file (`CryptoWalletGen.sln`) in Visual Studio or any compatible C++ compiler.
2. Install the necessary dependencies and build the project.

```cmd
> git clone https://github.com/microsoft/vcpkg
> .\vcpkg\bootstrap-vcpkg.bat
> .\vcpkg\vcpkg integrate install
> .\vcpkg\vcpkg install openssl:x64-windows
```

3. Start building the project.

## 🔍 Frequently Asked Questions (FAQ)

### ❓ Where can I download WalletGen?
You can download the WalletGen given on the [release download page](../../releases) 

### ❓ Where can I download a database of known addresses with balance?
You can download the current database given on the [release   page](../../releases) 

### ❓ Can WalletGen help me recover a lost Bitcoin wallet?
Yes. WalletGen uses brute-force seed generation and a known-address database to help users potentially **recover lost Bitcoin wallets**.

### ❓ Is WalletGen a seed phrase generator?
Yes. WalletGen can generate **BIP39 seed phrases** and derive wallets for Bitcoin, Ethereum, and other EVM chains.

### ❓ Do I need the internet to search through the database?
No. Searching through the database does not require an internet connection, as the wallet balance is already known.

### ❓ Can I find Ethereum wallets with balance?
Yes. WalletGen supports scanning for **Ethereum wallets with balance** using brute-force and a database of known addresses.

### ❓ Is WalletGen legal?
WalletGen is intended for **educational and research purposes only**. It should only be used on wallets you own or have permission to access.

## Todo
1. Search for missing words in a seed phrase. - **Done!**

## Contribute

Contributions are welcome! If you have ideas, bug reports, or want to contribute to the codebase, feel free to submit a pull request.

## Donate

I encourage you, when you find a wallet with a balance, to send me a small portion as a thank you. This motivates me to keep working on the program, keep it going, and make it better!

**BTC:** bc1qeyrshy5ntsguwxe9m8tp2x2yqhddz7ymkj44h9

**ETH:** 0x76c2E75B92Eb340f01B378e332FC7d8954893693

## Credits
This project uses code from the [Trezor project](https://github.com/trezor/trezor-crypto). The code is licensed under the MIT License.

## License
This project is licensed under the [MIT License](/LICENSE)





Update:  16.06.2025 05:52:00 Fixed broken links in system diagrams