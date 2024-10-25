# Decentralized Stablecoin (DSC)

## Overview

Decentralized Stablecoin (DSC) is a decentralized, algorithmically pegged cryptocurrency that aims to maintain a stable value of **1 DSC = 1 USD**. The system achieves stability by using overcollateralized assets like ETH and BTC and relies on automated, decentralized mechanisms to manage the peg. This stablecoin system is inspired by MakerDAO’s model and provides transparency, security, and stability to its users.

### Key Features:
- **Exogenous Collateralization**: Backed by external crypto assets such as ETH and BTC.
- **Pegged to USD**: Maintains a 1:1 value ratio with the US dollar.
- **Algorithmically Stable**: Implements automated mechanisms to ensure stability and maintain the peg.
- **Overcollateralized**: Ensures that the value of collateral is always greater than the circulating DSC.

## Tech Stack

- **Smart Contract**: Solidity
- **Testing Framework**: Foundry
- **Oracle**: Chainlink price feeds

## Contracts

### DSCEngine

The DSCEngine contract is the core of the stablecoin system, responsible for the following:
- **Minting DSC**: Users can deposit collateral and mint DSC tokens based on their collateral.
- **Redeeming Collateral**: Users can burn DSC tokens and redeem their underlying collateral.
- **Liquidation**: If a user’s health factor drops below a minimum threshold, their position can be liquidated with a liquidation bonus for liquidators.

### DecentralizedStableCoin (DSC)

The DSC contract implements an ERC20 token that represents the decentralized stablecoin. This contract allows for minting and burning of DSC tokens, governed by the DSCEngine.


## Getting Started

### Prerequisites
- **Foundry**: A fast, portable Ethereum development toolkit.

### Installation
1. **Clone the repository**:
   ```bash
   git clone https://github.com/viktor81562/DeFi-Stablecoin
   cd DeFi-Stablecoin
   forge install
   forge build
   forge test
   forge script script/DeployDSC.s.sol
