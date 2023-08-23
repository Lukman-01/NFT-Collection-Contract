# CryptoDevs NFT Collection

The CryptoDevs NFT Collection is a smart contract-based project built on the Ethereum blockchain that allows users to mint unique NFTs (Non-Fungible Tokens) representing Crypto Devs. These NFTs are distinct and scarce digital assets, each with its own individuality. The project aims to create an engaging and rewarding experience for users while promoting transparency and inclusivity.

## Contracts

This repository contains two Solidity smart contracts:

1. **CryptoDevs.sol**: This contract implements the ERC721Enumerable standard, enabling the creation and management of the CryptoDevs NFTs. It also integrates access control through the Ownable contract. Users can mint Crypto Dev NFTs by sending the required amount of Ether. There are reserved tokens for whitelisted addresses, ensuring early access for selected participants. The contract safeguards against exceeding the maximum supply and ensures fair distribution.

2. **Whitelist.sol**: The Whitelist contract manages a list of whitelisted Ethereum addresses. It allows addresses to be added to the whitelist, restricting certain actions or providing privileges based on membership. This contract is utilized in the CryptoDevs contract to reserve tokens for whitelisted users.

## Getting Started

To interact with the CryptoDevs NFT Collection and the Whitelist contract, follow these steps:

1. Deploy the Whitelist contract with a specified maximum number of whitelisted addresses.
2. Deploy the CryptoDevs contract, providing the address of the deployed Whitelist contract.
3. Users can add their addresses to the whitelist through the Whitelist contract.
4. Users can then mint Crypto Dev NFTs using the CryptoDevs contract, following the specified rules for pricing and whitelisting.
