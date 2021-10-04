## Challenge 3: Migrating Ethereum Standard (ERC-1155) into Cardano

### What is ERC-1155?

ERC-1155, a multi Token standard, was proposed by [Enjin](https://enjin.io/erc-1155). This standard, from my perspective, is dedicated to serve gaming industries. This is a standard for contracts that manage multiple token types. A single deployed contract may include any combination of fungible tokens, non-fungible tokens (in-game currencies, and collectible items, i.e. weapon, knife, shield)

Existing standards like ERC-20 and ERC-721, which was proposed by Ethereum community, require a separate contract to be deployed for each token type or collection. In contrast, the ERC-1155 Multi Token Standard allows for each token ID to represent a new configurable token type, which may have its own metadata, supply and other attributes in the same contract. Thus, it reduces redundant bytecode on the Ethereum blockchain and thrives game developers solutions of creating thousands of needed token types to support them developing games on blockchain

For further information, please check out this [ERC-1155](https://eips.ethereum.org/EIPS/eip-1155)

### Challenge Description

____

- Bring the concept/standard of ERC-1155 from Ethereum to Cardano

```solidity
function safeTransferFrom(address _from, address _to, uint256 _id, uint256 _value, bytes calldata _data) external

function safeBatchTransferFrom(address _from, address _to, uint256[] calldata _ids, uint256[] calldata _values, bytes calldata _data) external;

function balanceOf(address _owner, uint256 _id) external view returns (uint256);

function balanceOfBatch(address[] calldata _owners, uint256[] calldata _ids) external view returns (uint256[] memory);

function setApprovalForAll(address _operator, bool _approved) external;

function isApprovedForAll(address _owner, address _operator) external view returns (bool);
}
```

- Logic implementations should follow this library [Openzeppelin ERC-1155](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC1155/ERC1155.sol)
- Please note that your logic is allowed to change so that it could adapt Cardano architecture and data structure layout as long as it maintains its securities and features similarly as the original library

#### Requirements

____

- Your CERC-1155 (Cardano ERC-1155) library should be deployed on Cardano network (local or public testnet)
- The program should demonstrate these three essential tasks:
  - Be able to mint NFT item
  - Balance query
  - NFT item can be transferred (in batch or single)
- Provide README to instruct on how to test/verify your submission
