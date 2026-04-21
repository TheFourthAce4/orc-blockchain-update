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

## ✅ Deployment Checklist

- [ ] Clone this repository (see [Installation](#-installation--setup))
- [ ] Install all required dependencies (Node.js, npm packages)
- [ ] Configure environment variables (`.env` — see [Environment Variables](#environment-variables))
- [ ] Set up Immutable SDK credentials (Immutable Developer Hub)
- [ ] Set up Stripe API keys (Stripe Dashboard)
- [ ] Connect or configure the database (schema in `/database`)
- [ ] Run the backend server and verify API routes respond
- [ ] Open the WebGL build in a browser and verify game loads
- [ ] Test a wallet connection end-to-end
- [ ] Test a Stripe payment flow in test mode
- [ ] Confirm NFT minting and ownership transfer works
- [ ] Review the [User Guide](#-user-guide) for ongoing maintenance notes

---

## 🗂️ Repository Structure

```
orc-blockchain-update/
│
├── README.md                  ← You are here
│
├── /blockchain                ← Immutable SDK integration, NFT logic
│   └── (upload your files)
│
├── /payments                  ← Stripe integration, payment routes
│   └── (upload your files)
│
├── /backend                   ← Node.js / Express server
│   └── (upload your files)
│
├── /frontend                  ← Next.js / React pages (wallet, leaderboard, UI)
│   └── (upload your files)
│
├── /webgl-build               ← Unity WebGL build output
│   └── (upload your files)
│
├── /database                  ← DB schema, migrations, seed data
│   └── (upload your files)
│
└── /docs                      ← Any additional documentation, diagrams, reports
    └── (upload your files)
```

> **For teammates:** Drop your work into the relevant folder above. If your work spans multiple folders, use your judgment or add a sub-folder. Commit with a clear message describing what you added.

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

---

## 🤝 Support & Point of Contact

For questions about this codebase after project handoff, reach out to any team member:

| Name | Role | Contact |
|------|------|---------|
| Ninos Toma | Team Member | — |
| Abdullah Alghabban | Team Member | — |
| John Li | Team Member | — |
| Ethan Peterson | Team Member | — |
| Shiven Shekar | Team Member | — |

> **Teammates:** Fill in your preferred contact info (email or GitHub handle) before final submission.

---

## 📄 License

This project was developed as a capstone project for Arizona State University and is intended for use by the sponsor, Obi Onyejekwe. All rights to the Off-Road Champions game and brand belong to the sponsor.
