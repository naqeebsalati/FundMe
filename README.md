# FundMe Smart Contract

A decentralized crowdfunding smart contract written in Solidity. This project allows users to contribute ETH to the contract and only the owner (deployer) can withdraw the funds.

## Features

- Accepts ETH from funders (minimum contribution in USD)
- Uses Chainlink price feeds to convert ETH to USD
- Owner-only withdrawal functionality
- Secure access control with Solidity modifiers
- Optimized gas usage using `constant`, `immutable`, and custom errors
- Handles direct ETH transfers using `receive()` and `fallback()`
- Deployed on zkSync Sepolia Testnet

## Technologies

- Solidity (`^0.8.24`)
- Chainlink AggregatorV3Interface
- Remix IDE & MetaMask
- zkSync Sepolia Testnet
- Chainlink Price Feeds

## Contract Functions

### `fund()`
Allows users to fund the contract if they meet the minimum USD threshold.

### `withdraw()`
Allows only the contract owner to withdraw all funds.

### `getPrice()`
Returns the latest ETH/USD price.

### `getVersion()`
Returns the version of the Chainlink price feed.

## Deployment

### Prerequisites
- MetaMask wallet with zkSync Sepolia ETH
- Remix IDE with zkSync plugin
- Solidity compiler set to version `0.8.24`

### Steps
1. Replace the price feed address with the zkSync-compatible one.
2. Compile the contract in Remix.
3. Deploy using the zkSync plugin and MetaMask.

## Testing

- Tested fund/withdraw functions on Remix
- Verified contract behavior using receive and fallback functions
- Checked gas optimizations and error handling

## License

MIT License

---

Feel free to fork, improve, or contribute to the project!
