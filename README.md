# VestRoll: ZK-Payroll

VestRoll is a payroll and invoicing platform built for the 2026 financial ecosystem. Built with **Next.js 15**, **React 19**, and the **Stellar Soroban** stack, it offers a "No-Crypto" UX where privacy, speed, and biometric security are standard.

---

## 🏗️ The 2026 Technology Stack

### Core Architecture

- **Framework**: [Next.js 15.5](https://nextjs.org/) (App Router & Turbopack)
- **Library**: [React 19](https://react.dev/)
- **State**: Redux Toolkit (UI) & Zustand (Store)

### Identity & Privacy (ZK)

- **Auth**: [@stellar/passkey-kit](https://github.com/stellar/passkey-kit) (FaceID/TouchID Biometric Login)
- **Privacy**: [Stellar Protocol 25 (X-Ray)](https://stellar.org/blog/developers/protocol-25-x-ray) & `circomlib` for ZK-shielded payroll.
- **Smart Accounts**: [@stellar/smart-account-kit](https://github.com/stellar/smart-account-kit) for automated contract-wallet deployment.

### Finance & Fiat Bridge

- **Fiat Providers**: Native integration for **Monnify** and **Flutterwave** (NGN On-ramps).
- **Stellar Bridge**: [SEP-24](https://stellar.org/developers/stellar-wallet-sdk) via Stellar Wallet SDK for automated NGN-to-USDC settlement.
- **Gasless UX**: **Launchtube** / Fee-Bumping infrastructure (Zero XLM required for users).

---

## 📂 Project Structure

```text
vestroll/
├── src/
│   ├── api/                # ZK-Circuit logic & Service Orchestration
│   ├── app/                # Next.js App Router (Invisible Crypto UX)
│   ├── components/         # Biometric Auth & Shielded UI Components
│   ├── server/
│   │   ├── services/       # Monnify, Flutterwave & Blockchain Services
│   │   └── db/             # Drizzle Schema (Auth, Org, Fiat, ZK)
│   └── lib/                # Passkey & Smart Account SDK wrappers
└── brain/                  # Master Roadmaps & Technical Documentation
```

---

## ✨ Key Features

- **Invisible Onboarding**: Users sign up with Email and Biometrics (Passkeys). No seed phrases, no private keys, no 12-word recovery.
- **Hybrid Recovery**: A "Best of Both Worlds" security model—Biometric speed for daily use, Email recovery for account resets.
- **ZK-Shielded Payments**: Payroll amounts are hidden from the public ledger using Zero-Knowledge proofs, providing enterprise-grade confidentiality.
- **Automated Fiat-Stable Bridge**: Deposits in **Naira (NGN)** are automatically reflected as **USDC** in the Smart Wallet, enabling instant global payouts.
- **Atomic Batching**: Disburse 100+ payroll entries in a single biometric signature using Soroban atomic transactions.
- **Invisible Gas**: Transaction fees are sponsored (Launchtube) or paid in USDC, ensuring users never need to hold or know about XLM.

---

## 🎯 Target Audience & Ecosystem Impact

### Who is this for?

- **Global Enterprises**: Companies with distributed teams needing seamless cross-border payroll.
- **DAO & Web3 Organizations**: Native crypto organizations requiring fiat and stablecoin payroll solutions.
- **Freelancers & Contractors**: Individuals seeking transparent, instant, and low-fee payments.

### Contribution to the Stellar Ecosystem

VestRoll plays a pivotal role in the **Stellar ecosystem** by:

1.  **Driving Real-World Utility**: Moving beyond speculation to practical, high-volume stablecoin use cases (Payroll).
2.  **Highlighting Efficiency**: Showcasing Stellar's speed and low fees for frequent, small-to-large value transactions.

---

## 🚀 Getting Started

### Prerequisites

- Node.js 20.x or higher
- **pnpm** (preferred)
- **Stellar CLI** (for local Soroban development)

### Installation

1. Clone the repository and install dependencies:
   ```bash
   pnpm install
   ```
2. Configure Environment:
   Add `STELLAR_RPC_URL` and `LAUNCHTUBE_API_KEY` to your `.env.local`.
3. Start development server:
   ```bash
   pnpm dev
   ```

---

## 🛡️ Roadmap & Strategy

VestRoll development is structured across 4 Strategic Tranches:

1. **Tranche 1**: Foundation & Biometric Onboarding.
2. **Tranche 2**: Fiat-Stable Bridge (NGN MVP).
3. **Tranche 3**: Privacy Shield (Shielded Testnet).
4. **Tranche 4**: Mainnet Launch & UX Audit.

**Detailed Checklists:**

- [Master Engineering Roadmap](file:///C:/Users/TCE HUB/.gemini/antigravity/brain/6ca2dde2-48cc-4948-bc2e-55cf56f46056/vestroll_master_roadmap_2026.md)
- [Backend Contributor Guide (150+ Tasks)](file:///C:/Users/TCE HUB/.gemini/antigravity/brain/6ca2dde2-48cc-4948-bc2e-55cf56f46056/backend_engineering_roadmap.md)
- [NGN Fiat Implementation Guide](file:///C:/Users/TCE HUB/.gemini/antigravity/brain/6ca2dde2-48cc-4948-bc2e-55cf56f46056/fiat_naira_roadmap.md)

---

## 📄 License

Commercial - All rights reserved to SafeVault/VestRoll.
