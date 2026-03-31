<div align="center">

# seti.

**Prediction markets for real-world events — built with a modular, multi-chain architecture**

</div>

---

## Overview

**seti** is a prediction market platform that lets users create, trade, and resolve markets on real-world outcomes.  
The project is designed to be **consumer-friendly**, **modular**, and ready for **privacy-preserving + programmable access** use cases.

Rather than being tied to a single chain, seti can be deployed as a multi-network stack:

- **Flow**: launch consumer-facing apps with smooth UX and mainstream onboarding
- **Starknet**: build privacy-preserving systems (e.g., private positions, private reputation, selective disclosure)
- **NEAR**: create modular apps with clean separation between market logic, settlement, and UI
- **Lit Protocol**: programmable wallets + gated financial access (membership, compliance gates, subscriptions, teams)
- **Filecoin**: store proofs or datasets (market evidence bundles, model outputs, attestations, archived metadata)

---

## Live Demo

Demo URL: **https://seti-mvp.vercel.app/**

> Note: The demo may run in a “UI-only / mocked backend” mode depending on the current deployment target.

---

## Core Features

### Marketplace Platform
- **Live Market Browsing**: explore active markets across categories
- **Category Management**: Crypto, Stocks, Sports, Politics, Technology, Economics, Space, and more
- **Dynamic Pricing**: YES/NO pricing based on liquidity and trading activity
- **Market Analytics**: 24h volume, total liquidity, and performance visualization
- **Responsive Interface**: optimized for desktop and mobile

### Trading Infrastructure
- **Streamlined Trading**: one-click YES/NO positions with clear confirmations
- **Automated Market Making (AMM)**: liquidity pool based pricing (configurable)
- **Portfolio Tracking**: track positions and potential payouts
- **Transparent Risk**: clear pricing + payout calculations before execution

### Programmable Access (Lit Protocol)
- **Programmable Wallet Flows**: support gated trading, team vaults, or delegated actions
- **Access Control**: restrict certain markets/features to holders, subscribers, or verified users
- **Policy Enforcement**: encode rules for who can trade, when, and under what conditions

### Privacy-Preserving Systems (Starknet)
- **Selective Disclosure / Privacy Options** (design target):
  - private positions until resolution
  - private eligibility proofs
  - optional identity / reputation signals without doxxing
- **Proof-Friendly Architecture**: design that can emit/store proofs where needed

### Data & Proof Storage (Filecoin)
- **Evidence & Dataset Archival**: store supporting datasets, snapshots, or proofs
- **Auditability**: preserve references that help verify market resolution decisions
- **Long-term Storage**: keep market metadata durable and accessible

---

## Tech Stack

- **Frontend**: React + TypeScript
- **Build**: Vite
- **Styling**: Tailwind CSS
- **UI**: shadcn/ui + Radix UI
- **State**: React Query
- **Routing**: React Router

> Chain modules are intended to be pluggable so the same UI can target Flow / Starknet / NEAR depending on the deployment.

---

## Getting Started

### Requirements
- **Node.js** 18+
- npm or yarn
- Modern browser (Chrome/Firefox/Safari/Edge)

### Install
```bash
git clone https://github.com/mokayaj857/seti.git
cd seti
npm install
```

### Environment config
```bash
cp .env.example .env.local
```

Suggested environment variables (adjust to your integration choices):
```env
# App
VITE_APP_NAME=seti
VITE_APP_ENV=development

# Flow (example placeholders)
VITE_FLOW_NETWORK=testnet
VITE_FLOW_ACCESS_NODE=

# Starknet (example placeholders)
VITE_STARKNET_NETWORK=sepolia
VITE_STARKNET_RPC_URL=

# NEAR (example placeholders)
VITE_NEAR_NETWORK=testnet
VITE_NEAR_RPC_URL=

# Lit Protocol (example placeholders)
VITE_LIT_NETWORK=cayenne
VITE_LIT_APP_ID=

# Filecoin / storage (example placeholders)
VITE_FILECOIN_NETWORK=calibration
VITE_STORAGE_PROVIDER=
```

### Run dev server
```bash
npm run dev
```

Then open:
- `http://localhost:8080`

---

## Project Structure

```text
src/
├── components/          # Reusable UI components
├── hooks/               # Custom hooks (wallet, markets, pricing, etc.)
├── pages/               # Route pages
├── types/               # Shared types and interfaces
├── App.tsx
└── main.tsx
```

---

## Deployment

### Vercel
```bash
npm run build
```

Set environment variables in Vercel, then deploy.

---

## Roadmap (High-Level)

- [ ] Flow-first consumer onboarding + production wallet UX
- [ ] Starknet privacy-preserving position / eligibility design
- [ ] NEAR modular contract/app composition
- [ ] Lit Protocol gated access + programmable wallets for advanced flows
- [ ] Filecoin storage of evidence bundles / proofs / datasets for auditability

---

## License

MIT — see `LICENSE`.
