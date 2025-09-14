# Lotus Monorepo

Everything you need to run Lotus: smart contracts, backend, mobile app, admin dashboard, tools, and AI.

## Structure
- apps/backend: Node.js backend with Lotus AI
- apps/wallet_app: Flutter app with PETAL, QR, card simulator, AI
- apps/admin: React dashboard for approvals + AI studio
- packages/contracts: Solidity contracts (PETAL + Rewards)
- packages/tools: Partner QR signer + prompt seeds

## Setup

### 1. Install tools
- Node.js 20+, pnpm 9+
- Flutter 3.24+
- GitHub Codespaces or mobile IDE

### 2. Install dependencies
pnpm install

### 3. Deploy contracts
- Fill packages/contracts/.env
- Run: pnpm build:contracts && pnpm test:contracts && pnpm --filter lotus-contracts run deploy

### 4. Start backend
- Fill apps/backend/.env
- Run: pnpm dev:backend

### 5. Run admin dashboard
pnpm dev:admin

### 6. Run Flutter app
cd apps/wallet_app
flutter pub get
flutter run

## Push to GitHub
- Create repo: lotus-monorepo
- git init && git add . && git commit -m "init"
- git remote add origin https://github.com/YOUR_USERNAME/lotus-monorepo.git
- git push -u origin main
