# vApp Submission: [Verifiable Random Number Generator for On-Chain Gaming]

## Verification
```yaml
github_username: "0xhours"
discord_id: "1184705235747340369"
timestamp: "2025-01-15"
```

## Developer
- **Name**: Rizal Gilang Permana
- **GitHub**: @0xhours
- **Discord**: 0xhours
- **Experience**: ### I am a blockchain developer with extensive hands-on experience in smart contract development, deployment, and node testing across multiple ecosystems, including Ethereum-compatible chains, Solana, IBC (Inter-Blockchain Communication), and others. While my GitHub repositories highlight specific technical tasks on the Swisstronik testnet—such as deploying a basic "Hello World" smart contract (Task 1), creating and minting ERC20 tokens with minting, burning, transferring, and balance check functionalities (Task 2), minting ERC721 NFTs with support for minting and burning (Task 3), and minting PERC20 tokens as a privacy-enhanced variant (Task 4)—I've also completed numerous node testing projects and deployments on various blockchains that aren't publicly uploaded.

These additional experiences include setting up and running node testers on Solana for high-throughput validation, IBC for cross-chain interoperability testing, EVM-based networks for smart contract execution, and other protocols to ensure network stability and performance. My work spans a variety of programming languages beyond Solidity, such as Rust for Solana programs, Go for Cosmos/IBC integrations, and JavaScript/TypeScript for backend automation and cross-chain tooling. I've leveraged libraries like OpenZeppelin for ERC standards compliance, npm for scripting and dependency management, and frameworks like Anchor for Solana development.

Additionally, I've built a Node.js-based bot using Axios for API interactions, showcasing my proficiency in full-stack blockchain solutions. My focus encompasses token standards, decentralized applications (dApps), multi-chain deployments, and testnet environments, with a strong emphasis on security and efficiency. I am active on Twitter (@0xhours).

## Project

### Name & Category
- **Project**: Sound-UP
- **Category**: gaming

### Description
A decentralized, verifiable random number generator (VRNG) vApp that provides cryptographically secure randomness for on-chain games, lotteries, or NFTs. Traditional RNG in blockchain games relies on oracles or block hashes, which can be manipulated or predicted. This vApp uses zero-knowledge proofs (ZKPs) to generate and verify randomness from user-submitted entropy (e.g., commitments), ensuring fairness and tamper-resistance. Players can trust the outcomes without revealing seeds prematurely.


### SL Integration  
  - Use SL's decentralized verifiers for proof submission and attestation, ensuring low-latency (<1s) validation.
  - Store entropy data on Walrus for cheap, blob-based availability, with SL handling data integrity proofs.
  - Inter-chain: Leverage SL's proof-agnostic framework for exporting verified randomness to chains like Ethereum (via ZK light clients).

This solves trust issues in Web3 gaming, enabling provably fair mechanics and reducing disputes, while leveraging Soundness's low-latency verification for real-time play.

## Technical

### Architecture
- **ZK Integration**: Employ zkVMs (e.g., SP1 or RISC0 from Soundness examples) to generate proofs for randomness computation. Circuits prove that the combined entropy is unbiased and correctly mixed (e.g., via SHA-3 hashing in ZK).
- **Data Flow**: Users submit commitments → vApp aggregates off-chain → Generates ZK proof → SL verifies and attests on-chain → Game contracts consume the verified random value.
- **Dependencies**: vApp SDK (Rust), zkVM libraries (e.g., SP1), Sui SDK, optional oracles for initial seeds if hybrid.


### Stack
- **Frontend**: Web-based interface (e.g., React with Sui Wallet integration) for users to submit entropy commitments and view verified results.
- **Backend**: Rust-based vApp DSL for core logic, deploying on Soundness Layer testnet. Use Sui Move for any settlement if needed.
- **Blockchain**: SL 
- **Storage**: WALRUS

### Features
- Multi-party entropy collection: Users contribute hashed inputs, combined into a final random value.
- ZK-verified computation: Prove randomness generation without exposing individual contributions.
- Integration with games: Output verifiable seeds for dice rolls, card shuffles, or loot drops.
- Cross-chain support: Attest randomness to other chains via Soundness Layer's inter-chain verification.

## Timeline
Realistic Development TimelineWeek 1: Set up vApp SDK, research SL APIs/Walrus integration, implement basic entropy submission handler.
Week 2: Develop ZK circuits for randomness mixing, integrate proof generation with zkVM.
Week 3: Build frontend, test full flow on Soundness testnet, add error handling.
Week 4: Optimize for latency, community review/audit, deploy MVP and document.
Total: 4 weeks for a working PoC, assuming testnet access after approval.

### PoC (2-4 weeks)
- [ ] Basic functionality
- [ ] SL integration
- [ ] Simple UI

### MVP (4-8 weeks)  
- [ ] Full features
- [ ] Production ready
- [ ] User testing

## Innovation
What makes this unique? Why will people use it?

## Contact
= discord : @0xhours
- x : @0xhours
- email : 0xhours.eth@gmail.com


**Checklist before submitting:**
- [ ] All fields completed
- [ ] GitHub username matches PR author  
- [ ] SL integration explained
- [ ] Timeline is realistic
