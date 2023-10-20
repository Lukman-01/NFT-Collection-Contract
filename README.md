# Crypto Devs NFT Project

This project lets you deploy a whitelist contract and an NFT contract where whitelisted users can mint NFTs for free while others need to pay.

## Features

- Whitelist system with a maximum number of allowed addresses.
- An NFT (ERC-721) contract with the following functionalities:
  - Limited total supply (20 NFTs).
  - 1 NFT per transaction rule.
  - Whitelisted users can mint for free.
  - Non-whitelisted users must pay 0.01 ETH to mint.

## Environment Setup

1. Clone this repository.
2. Navigate to the `hardhat` directory.
3. Set up environment variables by creating a `.env` file with the following entries:

```bash
PRIVATE_KEY="your_metamask_private_key"
RPC_URL="your_quicknode_http_provider_link"
ETHERSCAN_API_KEY="your_etherscan_api_key"
```

## Deployment

1. Install the required npm packages:

```bash
npm install
npm install @openzeppelin/contracts
npm install dotenv
```

2. Deploy the Whitelist contract:

```bash
npx hardhat run scripts/deploy.js --network sepolia
```

3. Take note of the contract address of the deployed Whitelist.

4. Replace the placeholder address in `deploy-nft.js` with your Whitelist contract address.

5. Deploy the NFT contract:

```bash
npx hardhat run scripts/deploy-nft.js --network sepolia
```

6. Interact with the contracts via Etherscan (Sepolia Testnet) or programmatically through web3 or ethers.js libraries.

## Testing

### For Whitelisted Addresses

1. Use Sepolia Etherscan to connect your wallet and interact with the Whitelist contract's "addAddressToWhitelist" function.
2. Now, interact with the NFT contract's `mint` function without sending any ETH.

### For Non-Whitelisted Addresses

1. Use Sepolia Etherscan to connect your wallet and interact with the NFT contract's `mint` function.
2. You'll need to send exactly 0.01 ETH for the minting to succeed.

## Important Notes

- Always ensure you're using a testnet account for deployment to avoid any loss of real funds.
- Keep your private key and other environment variables confidential. Avoid publishing or sharing your `.env` file.