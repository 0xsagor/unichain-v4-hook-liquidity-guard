# Unichain v4 Hook Liquidity Guard

With the roll-out of **Unichain**, maximizing capital efficiency while defending Liquidity Providers against Toxic Order Flow (LVR - Loss Versus Rebalancing) is critical. This repository features a highly optimized **Uniswap v4 Hook** designed to interface directly with pool lifecycle execution points.

## Hook Execution Pipeline
The contract implements targeted overrides to dynamically scale pool swap fees based on immediate block metrics, protecting passive liquidity from predatory arbitrage vectors.

- **beforeInitialize:** Provisions standard pool keys.
- **beforeSwap:** Inspects inbound trade volume and updates parameters if a block congestion threshold is breached.
- **afterSwap:** Restores normal operating baselines.

## Development Setup
1. Install project structures: `npm install`
2. Compile bytecode components using Foundry: `forge build`
3. Run test suites locally: `forge test`

## Specifications
- **Language:** Solidity ^0.8.26
- **Protocol:** Uniswap v4 Core Framework
- **Target Network:** Unichain L2 Execution Environment
