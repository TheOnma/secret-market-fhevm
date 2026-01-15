# Secret Market 🔮

**Bet in Secret. Win in Public.**

A prediction market where your bets are encrypted on-chain using Fully Homomorphic Encryption (FHE). Other traders can't see your positions, so no one can copy your strategy or front-run your moves.

## Why This Matters

Traditional prediction markets have a problem: everyone can see your bets. If you place a large position, others might:
- Copy your strategy
- Front-run your trades
- Use your position data against you

Secret Market solves this. Your bet amounts are encrypted on-chain using Zama's FHEVM technology. You see your positions, but no one else can.

## How It Works

1. **Connect your wallet** (MetaMask)
2. **Pick a market** (e.g., "Will BTC hit $100k?")
3. **Place your bet** - YES or NO
4. **Your position is encrypted** on-chain using FHE
5. **Win in public** when the market resolves

## Current Markets

- Bitcoin: "Will BTC close above $100k this year?"
- Ethereum: "What price will ETH hit Sept 29 - Oct 5?"

## Tech Stack

**Smart Contracts:**
- Solidity + FHEVM (euint128 encrypted types)
- Hardhat for development
- Comprehensive test coverage

**Frontend:**
- React/Next.js
- TypeScript
- FHEVM React hooks
- MetaMask integration

## Quick Start
```bash
# Install dependencies
npm install

# Start local node
npm run hardhat-node

# Deploy contracts (new terminal)
npm run deploy

# Start frontend (new terminal)
cd packages/site
npm run dev:mock
```

Open http://localhost:3000 and connect your wallet.

## Project Structure
```
fhevm-project/
├── packages/
│   ├── fhevm-hardhat-template/  # Smart contracts
│   │   ├── contracts/PredictionMarket.sol
│   │   └── test/
│   └── site/                    # Frontend
│       ├── components/PredictionMarketDemo.tsx
│       └── hooks/usePredictionMarket.tsx
```

## What Makes This Different

**Privacy by default:** Your bets are encrypted at the smart contract level, not just hidden in the UI.

**No trusted third party:** Encryption happens on-chain using FHEVM. No relayer, no centralized server.

**Real FHE:** Uses Zama's Fully Homomorphic Encryption - computations on encrypted data without decryption.

## Development
```bash
# Run tests
npm run test

# Deploy to localhost
npm run hardhat-node
npm run deploy

# Start dev server
npm run dev:mock
```

## Built With

- [Zama FHEVM](https://www.zama.ai/) - Fully Homomorphic Encryption
- [Hardhat](https://hardhat.org/) - Smart contract development
- [Next.js](https://nextjs.org/) - React framework
- Inspired by Polymarket's UI/UX

## Recognition

🏆 Received Zama OG Developer Contributor NFT

## License

BSD-3-Clause-Clear

---

**Built with ❤️ for a more private DeFi future**
