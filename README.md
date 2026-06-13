# 🏁 Off-Road Champions — Blockchain Update

> **Capstone Project | Arizona State University**
> BlockChain Update Team: Ninos Toma, Abdullah Alghabban, John Li, Ethan Peterson, Shiven Shekar
> Sponsor: Obi Onyejekwe | obi.onyejekwe@gmail.com

---

## 📋 Project Summary

The **Off-Road Champions (ORC) Blockchain Update** modernizes the existing ORC game platform by integrating blockchain-based NFT asset ownership and a payment processing system. Players can purchase, own, and trade in-game assets (vehicles, skins, upgrades) as verifiable NFTs on the blockchain. The platform also includes a WebGL browser build of the game, a leaderboard, and a wallet interface.

**Core additions this team delivered:**
- NFT minting and ownership via the Immutable SDK
- Payment integration via Stripe (purchasing in-game items)
- Wallet connection and asset display UI
- WebGL browser build of the game client
- Leaderboard, player account, and transaction infrastructure

---

## ⚙️ Installation & Setup

### Prerequisites

| Tool | Version | Notes |
|------|---------|-------|
| Node.js | v18+ | [nodejs.org](https://nodejs.org) |
| npm | v9+ | Comes with Node.js |
| Unity | 2022.x LTS | Only needed to rebuild the WebGL client |
| Git | Latest | [git-scm.com](https://git-scm.com) |

### Clone the Repository

```bash
git clone https://github.com/<your-org>/orc-blockchain-update.git
cd orc-blockchain-update
```

### Install Backend Dependencies

```bash
cd backend
npm install
```

### Install Frontend Dependencies

```bash
cd frontend
npm install
```

---

## 🔑 Environment Variables

Create a `.env` file in the `/backend` directory (never commit this file). Template:

```env
# Immutable SDK
IMMUTABLE_API_KEY=your_immutable_api_key
IMMUTABLE_ENVIRONMENT=sandbox       # or "production"

# Stripe
STRIPE_SECRET_KEY=sk_test_...
STRIPE_PUBLISHABLE_KEY=pk_test_...
STRIPE_WEBHOOK_SECRET=whsec_...

# Database
DATABASE_URL=your_database_connection_string

# Server
PORT=3001
NODE_ENV=development
```

> ⚠️ The `.env` file is in `.gitignore` and will **not** be committed. Obi: request the production keys from the team directly.

---

## 🔗 Key Libraries & APIs

### Blockchain / NFT
| Library | Version | Source |
|---------|---------|--------|
| `@imtbl/sdk` | `^2.x` | [Immutable Developer Hub](https://docs.immutable.com) |

### Payments
| Library | Version | Source |
|---------|---------|--------|
| `stripe` | `^14.x` | [stripe.com/docs](https://stripe.com/docs) |

### Backend
| Library | Version | Source |
|---------|---------|--------|
| Node.js | `18+` | [nodejs.org](https://nodejs.org) |
| Express | `^4.x` | [expressjs.com](https://expressjs.com) |

### Frontend
| Library | Version | Source |
|---------|---------|--------|
| Next.js | `^14.x` | [nextjs.org](https://nextjs.org) |
| React | `^18.x` | [react.dev](https://react.dev) |

> **Teammates:** Please update the versions in this table to match what you actually used in your code.

---

## 📖 User Guide

### For the Sponsor (Obi)

**Running the backend:**
```bash
cd backend
node server.js          # or: npm start
```

**Running the frontend:**
```bash
cd frontend
npm run dev             # development
npm run build && npm start   # production
```

**Opening the WebGL game:**
Simply open `webgl-build/index.html` in a modern browser (Chrome or Firefox recommended). No server required for the game itself.

### Key Features & How to Use Them

| Feature | How It Works |
|---------|-------------|
| **Wallet Connection** | Players connect a compatible wallet (e.g., Passport by Immutable) via the wallet page |
| **NFT Ownership** | Owned assets are displayed in the player's wallet; minting happens on purchase |
| **Buying Items** | Stripe checkout handles payment; on success, an NFT is minted to the player's wallet |
| **Leaderboard** | Auto-updated based on game results stored in the database |
| **WebGL Game** | Playable in-browser; connects to the backend for account and inventory data |
