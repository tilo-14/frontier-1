# Hackathon Ideas

A curated, non exhaustive list of ideas to participate in the Solana Frontier Hackathon.

## Payments and Stablecoins

- P2P payment app: QR/NFC scan to send USDC on Solana, contact list lookup, request payments ([Solana Pay](https://solanapay.com/))
- Split payments: group expense splitting, auto-settle in USDC
- Recurring payments: scheduled USDC transfers using token delegation (approve + periodic pull)
- Merchant checkout: Solana Pay integration with invoice generation and webhook callbacks
- Payroll and Cross-border remittance: USDC to local currency via off-ramp (MoonPay/Meso), Light Token accounts for recipients with no wallet

## AI Agents

### Identity and Discovery

- Agent identity + reputation registry using [Solana Agent Registry](https://solana.com/agent-registry/what-is-agent-registry) with compressed PDA-backed reputation scores
- [ERC-8004](https://eips.ethereum.org/EIPS/eip-8004) to Solana bridge: mirror Ethereum 8004 Identity Registry entries to Solana PDAs via Wormhole, propagate SAID registrations back to EVM; cross-chain agent discovery
- 8004 reputation aggregator for MCP servers: 8004 is a universal service registry, not just agents ([rick.build reframe](https://www.rick.build/blog/agentic-commerce-infrastructure)); index uptime/responseTime/successRate across MCP tool servers, expose rankings as MCP tool
- Agent-to-agent marketplace: register capabilities, discover via A2A agent cards, settle via x402 (AlphaClaw built this at the SURGE hackathon)
 
### Authentication
- [ERC-8128](https://eips.ethereum.org/EIPS/eip-8128) auth middleware for Solana: per-request Ed25519 HTTP signatures (RFC 9421), server verifies against SAID or bridged 8004, no stored tokens or API keys
- Passkey-delegated agent signer: @solana/mpp supports secp256r1 (WebAuthn); owner approves policy via biometric tap, agent operates with hardware-backed delegated signer
 
### Commerce
- [ERC-8183](https://eips.ethereum.org/EIPS/eip-8183) job marketplace on Solana: implement 8183 Job primitive (escrow, provider submission, evaluator approve/reject); evaluator = AI agent or ZK verifier; hooks update 8004 reputation after each job
- 8183 hook library: reusable hooks for reputation-gating (query 8004 score), bidding (providers compete on price), privacy (submission = ZK proof), underwriting (staked collateral + slashing)
- AP2 mandate issuer for Solana: [AP2](https://ap2-protocol.org/) uses cryptographic Mandates for agent purchase auth; build Ed25519-signed mandates recognized by AP2-compliant merchants, settle via x402
- Visa TAP identity module: TAP uses PKI for merchant bot-filter access; wrap Visa-registered key signing into Solana agent, combine with AP2 mandates for full checkout

## DeFi

- Tokenized stock lending: use Ondo/Galaxy equities as collateral for stablecoin borrowing with stock-market-aware liquidation logic
- Light-PDA AMM: LP positions as Light-PDAs with no rent-exemption per position ([cp-swap-reference](https://github.com/Lightprotocol/cp-swap-reference))
- RWA yield aggregator: compare yields across Ondo (OUSG), Spiko (SAFO), Maple on Solana; auto-allocate by risk/duration, expose as x402-gated API for agent treasury management

## Prediction Markets

- Kalshi positions as lending collateral via [DFlow](https://solana.com/news/dflow-prediction-markets-api) (positions are SPL tokens, $20B+ with 0% borrowing utilization)
- Parlay engine: combine 2-4 Kalshi/DFlow positions into a single composite SPL token with multiplied odds ([PredictShark](https://polymark.et/product/predictshark) does this on Polygon, nothing on Solana yet)
- Prediction market oracle: price Kalshi positions from order book data for use as DeFi collateral
- Prediction market aggregator across Kalshi, DFlow, and other sources (Capitola won $25K at the Cypherpunk hackathon with this concept)
- Agent-managed prediction portfolio: AI agent monitors markets for mispriced outcomes, rebalances via DFlow, pays for data feeds via x402, spending constrained by Light Token spend permissions

## Privacy and ZK
 
- Private stablecoin transfers: Token-2022 Confidential Balances + Light Token for scale
- [ERC-5564](https://eips.ethereum.org/EIPS/eip-5564) stealth addresses ported to Solana: one-time receive addresses via ECDH, sender/receiver unlinkable; UX problems that blocked human adoption (key mgmt, scanning, fragmented balances) are trivial for agents
- ZK identity attestation: prove claims ("over 18", "passed KYC") without revealing identity, using Groth16 proofs stored as compressed PDAs
- ZK compliance passport: one proof of AML/KYC compliance gates access to multiple protocols
- Private .sol domain registration: commitment scheme + nullifiers to prevent double-registration, registrant hidden behind a ZK proof
- Private agent registry: prove membership in a registered operator set and reputation above threshold via ZK range proof, without revealing which operator or exact score
- Confidential payment channel: batch N confidential transfers off-chain (Token2022 Confidential Balances), settle net on-chain in one encrypted transfer; target B2B settlement
