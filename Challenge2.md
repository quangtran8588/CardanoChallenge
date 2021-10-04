## Challenge 2: Migrating Ethereum Standard (ERC-721) into Cardano

### What is ERC-721?

Ethereum introduces ERC-721 standard for Non-Fungible Token (NFT) that serves as a backbone of many industries, i.e. game and art that offer collectible items (weapons, skills or amazing kitties). A Non-Fungible Token (NFT) is used to identify something or someone in a unique way. In other words, this type of Token is unique and no replicated value of the same Token within the same Smart Contract

A standard allows wallet/broker/auction applications to work with any NFT on Ethereum. This standard is inspired by the ERC-20 token standard and builds on two years of experience since EIP-20 was created. EIP-20 is insufficient for tracking NFTs because each asset is distinct (non-fungible) whereas each of a quantity of tokens is identical (fungible).

For further information, please check out this [ERC-721](https://ethereum.org/en/developers/docs/standards/tokens/erc-721/)

### Challenge Description

____

- Bring the concept/standard of ERC-721 from Ethereum to Cardano

```solidity
function balanceOf(address _owner) external view returns (uint256)

function ownerOf(uint256 _tokenId) external view returns (address)

function safeTransferFrom(address _from, address _to, uint256 _tokenId, bytes data) external payable

function safeTransferFrom(address _from, address _to, uint256 _tokenId) external payable
    
function transferFrom(address _from, address _to, uint256 _tokenId) external payable
    
function approve(address _approved, uint256 _tokenId) external payable

function setApprovalForAll(address _operator, bool _approved) external

function getApproved(uint256 _tokenId) external view returns (address)
    
function isApprovedForAll(address _owner, address _operator) external view returns (bool)
```

- Logic implementations should follow this library [Openzeppelin ERC-721](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC721/ERC721.sol)
- Please note that your logic is allowed to change so that it could adapt Cardano architecture and data structure layout as long as it maintains its securities and features similarly as the original library

#### Requirements

____

- Your CERC-721 (Cardano ERC-721) library should be deployed on Cardano network (local or public testnet)
- The program should demonstrate these three essential tasks:
  - Be able to mint NFT item
  - NFT item is unique and should be owned by one User
  - NFT item can be transferred and its ownership should also be updated
- Provide README to instruct on how to test/verify your submission
