# Soroban Token Swap

An Automated Market Maker (AMM) and token swap smart contract for [Soroban](https://soroban.stellar.org/) on Stellar.

## Features

- **Constant Product AMM**: x * y = k pricing model
- **Liquidity Pools**: Create and manage token pair pools
- **Slippage Protection**: Configurable slippage tolerance
- **Fee Tiers**: Adjustable swap fees (0.1%, 0.3%, 1%)
- **LP Token Receipt**: Automatic LP token minting/burning
- **Flash Swaps**: Atomic multi-hop swaps across pools

## Architecture

```
┌──────────┐     ┌──────────────┐     ┌──────────┐
│  Token A  │────▶│              │────▶│  Token B  │
└──────────┘     │   AMM Pool   │     └──────────┘
                 │   Contract   │
┌──────────┐     │              │     ┌──────────┐
│  LP Token │◀────│              │────▶│  Fees     │
└──────────┘     └──────────────┘     └──────────┘
```

## Quick Start

```bash
soroban contract build
cargo test
```

## License

MIT
