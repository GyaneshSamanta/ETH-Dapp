# ETH-Dapp — WavePortal

> **A first-principles Ethereum dApp: a Solidity contract that records "waves" sent on-chain.**

![Solidity](https://img.shields.io/badge/Solidity-363636?logo=solidity&logoColor=white)
![Hardhat](https://img.shields.io/badge/Hardhat-FFF100?logo=hardhat&logoColor=black)
![Ethers.js](https://img.shields.io/badge/Ethers.js-2535A0?logo=ethereum&logoColor=white)

## About

- **What:** A learning-oriented Ethereum decentralized application — a Solidity smart contract (`WavePortal.sol`) plus a Hardhat dev environment for compiling, testing, and deploying it.
- **Who:** Built solo by Gyanesh Samanta as a hands-on intro to the Ethereum stack.
- **When:** Initial scaffold December 15, 2022; revisited March 28, 2026.
- **Where:** Personal sandbox project, designed to run locally on the Hardhat network.
- **Why:** To get past tutorials and actually feel the dev loop — write Solidity, compile with Hardhat, run unit tests, deploy to a local chain — before tackling anything serious on mainnet or a testnet.

## The Story

Web3 looks impenetrable from the outside: ABIs, gas, nonces, RPC endpoints, EOAs versus contract accounts. The only cure is to ship something tiny end-to-end.

WavePortal is that something. The contract lets a wallet send a "wave" — a transaction that triggers an event and increments a counter on-chain. There's no token, no DeFi primitive, no staking. Just the bare minimum needed to learn how Solidity state mutates, how Hardhat compiles and tests, and how Ethers.js bridges JavaScript to the EVM. The README's old `npx hardhat target` was a placeholder — the actual flow is `compile → test → run`, all of which work against Hardhat's built-in local node.

## Gallery

_No screenshots — this is a contract-only learning repo._

---

## Tech Stack

- **Language:** Solidity (smart contract)
- **Dev environment:** [Hardhat](https://hardhat.org/) `^2.12.4`
- **Toolbox:** `@nomicfoundation/hardhat-toolbox`, `@nomicfoundation/hardhat-chai-matchers`, `@nomiclabs/hardhat-ethers`
- **Library:** [Ethers.js](https://docs.ethers.org/) `^5.7.2`
- **Testing:** Chai
- **Frontend (planned):** React.js

## Repo Structure

```
ETH-Dapp/
├── contracts/
│   └── WavePortal.sol      # The smart contract
├── hardhat.config.js       # Hardhat network + compiler config
├── package.json
└── package-lock.json
```

## Getting Started

You'll need Node.js 16+ and npm.

```bash
git clone https://github.com/GyaneshSamanta/ETH-Dapp.git
cd ETH-Dapp
npm install
```

The standard Hardhat workflow:

```bash
npx hardhat compile                     # Compile Solidity to bytecode + ABI
npx hardhat test                        # Run unit tests against the in-memory chain
npx hardhat node                        # Start a local Ethereum node (separate terminal)
npx hardhat run scripts/deploy.js --network localhost   # Deploy
```

> Note: `scripts/deploy.js` and a `test/` directory are scaffolding you'll typically add as the project grows — the contract itself lives in `contracts/WavePortal.sol`.

## Contributing

This is a learning sandbox, so issues and PRs are welcome but light traffic is expected.

## License

[ISC](package.json).

## Credits

Built by [Gyanesh Samanta](https://github.com/GyaneshSamanta). Ethereum tooling courtesy of the Hardhat and Ethers.js teams.
