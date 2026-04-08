# Resources

A selection of developer tools, documentation, and references for building on Solana.

- [Learning](#learning)
- [Building](#building)
  - [AI Agent Skills](#ai-agent-skills)
  - [Infrastructure](#infrastructure)
  - [RPC Providers](#rpc-providers)
  - [Wallets](#wallets)
  - [Payments](#payments)
  - [DeFi](#defi)
  - [NFTs](#nfts)
  - [Mobile](#mobile)
  - [Gaming](#gaming)
  - [Cross-Chain](#cross-chain)
  - [Privacy and ZK](#privacy-and-zk)
  - [Agent Standards](#agent-standards)

# Learning

Get an introduction to Solana via these resources.

| Resource | URL | What |
|----------|-----|------|
| Blueshift | [blueshift.gg](https://blueshift.gg/) | Free Solana courses: on-chain programs, mobile dev, SVM internals. |
| Helius Blog | [helius.dev/blog](https://www.helius.dev/blog) | Technical deep-dives, tutorials, ecosystem updates. |
| Solana Awesome | [helius-labs/solana-awesome](https://github.com/helius-labs/solana-awesome) | Curated list of Solana resources. |

# Building

## AI Agent Skills

Non exhaustive list and reference standards for building with AI on Solana.
> Use [deepwiki.com](https://deepwiki.com/) to work with any public GitHub repo via AI-powered documentation.

| Resource | URL | What |
|----------|-----|------|
| Solana Dev Skill | [github.com/solana-foundation/solana-dev-skill](https://github.com/solana-foundation/solana-dev-skill/tree/main/skill) | Solana development skill for AI coding assistants. |
| Solana Agent Kit | [github.com/sendaifun/solana-agent-kit](https://github.com/sendaifun/solana-agent-kit) | 60+ pre-built actions for agents: DeFi, tokens, NFTs, payments. |
| ZK Compression | [github.com/Lightprotocol/skills](https://github.com/Lightprotocol/skills/tree/main/skills/payments) | Skills for scaling infrastructure for payments, program development, ZK applications and more. |
| Helius Core AI | [github.com/helius-labs/core-ai](https://github.com/helius-labs/core-ai) | CLI, AI assistant, and agent interface for Helius and Solana. |
| Awesome Solana AI | [github.com/solana-foundation/awesome-solana-ai](https://github.com/solana-foundation/awesome-solana-ai) | Curated list: agent kits, MCP servers, x402 tools, wallets, dev tools. |

## Infrastructure

Core documentation for building on Solana. Start with the Solana docs for fundamentals, use Anchor for program development, and ZK Compression for scaling with rent-free accounts.

| Resource | Docs | For |
|----------|------|-----|
| Solana | [solana.com/docs](https://solana.com/docs) | Solana basics: accounts, transactions, programs. |
| ZK Compression | [zkcompression.com](https://zkcompression.com) | Scaling infrastructure to reduce token and PDA account creation cost by 99%. |
| Anchor | [anchor-lang.com/docs](https://www.anchor-lang.com/docs) | Program development framework for Solana. |

## RPC Providers

Use one of these RPC providers run to interact with Solana. RPCs expose API endpoints that your app uses to read on-chain state, submit transactions, and subscribe to events.

| Provider | URL |
|----------|-----|
| Helius | [helius.dev](https://www.helius.dev/) |
| QuickNode | [quicknode.com](https://www.quicknode.com/) |
| Triton | [triton.one](https://triton.one/) |
| Alchemy | [alchemy.com](https://www.alchemy.com/) |

## Wallets

#### Crypto Native Wallets


For crypto native applications, connect to users' existing wallets via the [Solana Wallet Adapter](https://github.com/anza-xyz/wallet-adapter).

| Wallet | URL |
|--------|-----|
| Phantom | [phantom.app](https://phantom.app/) |
| Solflare | [solflare.com](https://solflare.com/) |
| Backpack | [backpack.app](https://backpack.app/) |

#### Embedded Wallets

For smoother UX and user onboarding, use one of the embedded wallet providers below. Their APIs cover all operations you need on Solana to send and receive tokens.

| Provider | URL |
|----------|-----|
| Privy | [privy.io](https://www.privy.io/) |
| Para | [getpara.com](https://getpara.com/) |
| Crossmint | [crossmint.com](https://www.crossmint.com/) |

## Payments

Documentation and infrastructure for accepting and sending payments on Solana.

> You can combine the infrastructure from below with one of the embedded wallet providers.

| Resource | Docs | For |
|----------|------|-----|
| Solana Payments | [solana.com/docs/payments](https://solana.com/docs/payments) | Payment basics: transfers, Solana Pay, merchant integration. |
| Light Token SDK | [zkcompression.com/payments/](https://www.zkcompression.com/light-token/payments/overview) | APIs to onboard users with 99% less cost. |
| Kora | [launch.solana.com/docs/kora](https://launch.solana.com/docs/kora) | Gasless transactions with relayer service: users can pay fees in any SPL token. |

## DeFi

| Protocol | What |
|----------|------|
| [Jupiter](https://jup.ag/) | DEX aggregator, limit orders, perpetuals. |
| [Pyth](https://pyth.network/) | High-frequency oracle for market data. |
| [Orca](https://www.orca.so/) | Concentrated liquidity AMM. |
| [Raydium](https://raydium.io/) | AMM and concentrated liquidity. |
| [Meteora](https://www.meteora.ag/) | Dynamic liquidity and memecoin pools. |
| [Drift](https://www.drift.trade/) | Perpetuals, spot, and lending. |
| [DFlow](https://www.dflow.net/) | Order flow and prediction market APIs. |

## NFTs

| Resource | URL | What |
|----------|-----|------|
| Metaplex | [developers.metaplex.com](https://developers.metaplex.com/) | NFT creation: Core standard, compressed NFTs via Bubblegum. |

## Mobile

| Resource | URL | What |
|----------|-----|------|
| Solana Mobile Stack | [docs.solanamobile.com](https://docs.solanamobile.com/) | Mobile Wallet Adapter, Seed Vault, Android SDK. |

## Gaming

| Resource | URL | What |
|----------|-----|------|
| MagicBlock | [magicblock.xyz](https://www.magicblock.xyz/) | On-chain game engine with Ephemeral Rollups. |

## Cross-Chain

| Resource | URL | What |
|----------|-----|------|
| Wormhole | [portalbridge.com](https://portalbridge.com/) | Bridge assets across 30+ chains. |
| deBridge | [debridge.com](https://debridge.com/) | Cross-chain swaps and token transfers. |

## Privacy and ZK

| Resource | URL | What |
|----------|-----|------|
| Noir | [noir-lang.org](https://noir-lang.org/) | ZK circuit language. Start here if you're new to ZK. |
| Noir on Solana | [github.com/solana-foundation/noir-examples](https://github.com/solana-foundation/noir-examples) | Working Noir circuits with Solana verifiers (unaudited). |
| Circom | [docs.circom.io](https://docs.circom.io/) | ZK circuit compiler. Use with snarkjs and groth16-solana. |
| groth16-solana | [github.com/Lightprotocol/groth16-solana](https://github.com/Lightprotocol/groth16-solana) | Groth16 verifier. Noir and Circom proofs verify through this. |
| ZK Compression | [zkcompression.com/zk](https://zkcompression.com/zk/overview) | Building ZK applications on Solana. |
| Arcium SDK | [docs.arcium.com](https://docs.arcium.com/) | MPC framework for private computation. |
| MagicBlock | [magicblock.gg](https://www.magicblock.gg/) | Ephemeral rollups with TEEs. |

## Agent Standards

####  Payments 
|  |  |
|----------|------|
| [x402](https://www.x402.org/) | HTTP-native payment protocol by Coinbase |
| [MPP](https://mpp.dev/overview) | HTTP-native payment protocol by Stripe and Paradigm |

Both x402 and MPP (Machine Payments Protocol) use the HTTP 402 Payment Required pattern: the server requires a payment before returning a protected response. On Solana, this is commonly implemented by asking the client to submit a small transfer, then the server verifies this onchain and serves the content. [Learn more about 402 here](https://solana.com/developers/guides/getstarted/intro-to-x402).

#### More agent standards

| Standard | What |
|----------|------|
| [ERC-8004](https://eips.ethereum.org/EIPS/eip-8004) | Trustless Agents: on-chain identity, service discovery, reputation |
| [ERC-8183](https://eips.ethereum.org/EIPS/eip-8183) | Agent Commerce: job escrow, provider submission, evaluator approve/reject |
| [ERC-8128](https://eips.ethereum.org/EIPS/eip-8128) | HTTP Message Signatures: per-request Ed25519 auth, no stored tokens |
| [ERC-5564](https://eips.ethereum.org/EIPS/eip-5564) | Stealth Addresses: one-time receive addresses, sender/receiver unlinkable |
| [Solana Agent Registry](https://solana.com/agent-registry/what-is-agent-registry) | PDA-based identity, A2A agent cards, MCP endpoints |
| [Open Wallet Standard](https://www.moonpay.com/newsroom/open-wallet-standard) | Multi-chain encrypted vault, keys never exposed to agent |
