# Reown AppKit React dApp

## Overview
This is a React-based decentralized application (dApp) example using Reown AppKit (formerly WalletConnect) for Web3 wallet integration. The project demonstrates multi-chain support for both EVM-compatible chains (Ethereum, Arbitrum) and Solana networks.

**Tech Stack:**
- React 19.0.0
- Vite 6.2.0 (build tool)
- TypeScript
- Reown AppKit 1.8.12 (wallet connection)
- Wagmi 2.12.14 (Ethereum integration)
- Solana Web3.js (Solana integration)
- TanStack React Query (data fetching)

**Current Status:** ✅ Fully configured and running in Replit environment

## Project Structure
```
├── public/               # Static assets (favicon, logos)
├── src/
│   ├── assets/          # React logo and other assets
│   ├── components/      # React components
│   │   ├── ActionButtonList.tsx
│   │   └── InfoList.tsx
│   ├── config/          # AppKit configuration
│   │   └── index.tsx
│   ├── css/             # Stylesheets
│   ├── App.tsx          # Main app component
│   └── main.tsx         # Entry point
├── vite.config.ts       # Vite configuration (configured for Replit)
└── package.json         # Dependencies
```

## Recent Changes (Nov 29, 2025)
- ✅ Configured Vite to run on port 5000 with host 0.0.0.0
- ✅ Added `allowedHosts: true` to support Replit's proxy/iframe environment
- ✅ Installed all npm dependencies
- ✅ Set up development workflow
- ✅ Configured static deployment (builds to `dist/`)

## Development Setup

### Running Locally
The app runs automatically via the "Start application" workflow. To manually start:
```bash
npm run dev
```
The dev server runs on port 5000 and is accessible through Replit's webview.

### Environment Variables
- `VITE_PROJECT_ID`: Reown (WalletConnect) project ID
  - Default: Includes a demo project ID for localhost testing
  - For production: Get your own from [Reown Dashboard](https://dashboard.reown.com)

### Building for Production
```bash
npm run build
```
Output is in the `dist/` directory.

## Deployment Configuration
- **Type:** Static deployment
- **Build command:** `npm run build`
- **Output directory:** `dist`
- The app can be published directly from Replit

## Features
- Multi-chain wallet connection (EVM + Solana)
- Support for mainnet and testnets
- Connect/disconnect wallet functionality
- Chain switching
- Network: Ethereum Mainnet, Arbitrum, Solana Mainnet/Devnet/Testnet

## User Preferences
None documented yet.

## Architecture Notes
- Frontend-only dApp (no backend required)
- Uses Reown AppKit for wallet abstraction
- Wagmi adapter handles EVM chains
- Solana adapter handles Solana chains
- Query client manages async state
- Configured for Replit's proxy environment with `allowedHosts: true`
