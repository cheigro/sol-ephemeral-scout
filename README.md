# Sol-Ephemeral-Scout 🔍

An advanced, open-source Command Line Interface (CLI) designed to inspect, track, and debug delegated accounts within **Solana Ephemeral Rollups** (e.g., MagicBlock architecture).

## 🚨 The Problem & Blind Spot
Ephemeral rollups allow high-throughput applications and on-chain games on Solana to achieve sub-50ms latency by temporarily delegating L1 account states to an ephemeral execution layer. However, developers currently face a **critical blind spot**: once an account is locked/delegated on L1, traditional block explorers (like Solscan) cannot inspect its live mutations inside the ephemeral runtime. If a transaction hangs or a runtime error occurs, the state remains a "black box" until session finalization.

## 💡 The Solution
`sol-ephemeral-scout` breaks the black box. It queries active ephemeral runtime RPCs and validators to provide developers with instant, real-time feedback on delegated accounts before L1 settlement.

## 🛠️ Tech Stack & Architecture
- **Language:** Rust 🦀
- **Frameworks:** `clap` (CLI parser), `solana-client`, `solana-sdk`
- **Target Integration:** MagicBlock Ephemeral Runtime Specs

## 🚀 Quick Start (Milestone 1 Preview)

### Prerequisites
Ensure you have Rust and Cargo installed:
```bash
curl --proto '=https' --tlsv1.2 -sSf https://rustup.rs | sh
```

### Installation
Clone the repository and build the CLI binary:
```bash
git clone https://github.com
cd sol-ephemeral-scout
cargo build --release
```

### Usage
To inspect a delegated account on the ephemeral runtime:
```bash
./target/release/sol-ephemeral-scout inspect --account <SOLANA_PUBLIC_KEY>
```

## 🗺️ Roadmap & Milestones (Grant Proposal)
- **Milestone 1 (Weeks 1-2):** Core CLI architecture setup, arguments parsing, and simulation engine. [In Progress]
- **Milestone 2 (Weeks 3-4):** Active RPC streaming binding to live ephemeral runtimes, real-time error log dumping, and MIT official release.

## 📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

