# 256-bit Private-Key Visualiser

A little **toy** that lets you “feel” and “twist” Bitcoin private keys in your hands—one bit at a time. Inspired by various key-gen services and built with a modern, zero-framework web stack (just HTML, CSS & JavaScript).

> **⚠️ Security disclaimer:**  
> This tool is purely for educational and entertainment purposes. **Do _not_** use it to generate real private keys for storing coins—anyone can copy or brute-force your bit patterns, especially if they’re simple or memorable.

## Live Demo

👉 https://keyz.decker.im/

## Features

- **Interactive 16×16 grid** representing a 256-bit private key  
- Click or tap individual bits to flip between 0 / 1  
- **Clear**, **Random**, **ROL / ROR** (row rotates) & **ROU / ROD** (column rotates) controls  
- Real-time updates of:
  - Binary (multi-line)
  - HEX (grouped by nibble)
  - WIF (compressed)
  - Bitcoin addresses:
    - **BTC (P2PKH) compressed & uncompressed**
    - **P2SH-wrapped SegWit (P2WPKH)**
    - **Native SegWit (bech32 P2WPKH)**
    - **Taproot (bech32m P2TR)**
  - Live balance checks via selectable APIs (mempool.space & blockchain.info)  
- **Green flash** around the grid for 3 seconds when any balance is non-zero  
- **Click balance** to open the address on mempool.space in a new tab  
- **Hotkeys** support (W/A/S/D for column/row rotations)

## Tech Stack & Libraries

- **HTML5** & **CSS3** (modern neumorphic/dark theme)  
- **Vanilla JavaScript** (ES Modules, no frameworks)  
- [@noble/secp256k1](https://github.com/paulmillr/noble-secp256k1) — key derivation & curve math  
- [@noble/hashes](https://github.com/paulmillr/noble-hashes) — SHA-256 & RIPEMD-160  
- [bs58](https://github.com/cryptocoinjs/bs58) — Base58Check encoding  
- [bech32](https://github.com/bitcoinjs/bech32) & [bech32m](https://github.com/bitcoinjs/bech32) — SegWit & Taproot address encoding  
- **Fetch API** — balance lookups via REST  

> This project was bootstrapped and refined with the help of AI.

## Getting Started

1. Clone or download the repo  
2. Open `index.html` in your browser (no server required)  
3. Play with the bits, explore address formats & check balances  

---

© 2025 Decker  
Built “by hand” with a bit of AI magic. Enjoy responsibly!  
