## Challenge 1: Migrating Ethereum Standard (ERC-20) into Cardano

### What is ERC-20?

ETH, as we know, is a native token of Ethereum blockchain platform. In supporting organizations as well as flourishing its ecosystem, Ethereum has introduced the concept of Token which can represent virtually anything in Ethereum:

- lottery tickets
- financial assets like a bond/share in a company
- a mapping 1-1 of fiat currency, i.e. Tether USD (USDT) or USD Coin (USDC)

That's exactly where the ERC-20 plays its role. The Ethereum introduces a standard (ERC-20) for Fungible Tokens. It means that these Tokens have a property that makes each of them, both type and value, be exactly the same as others. The standard provides developers a solution of building token applications that are interoperablly exchanged with other products and services.

For further information, please check out this [ERC-20](https://ethereum.org/en/developers/docs/standards/tokens/erc-20/)

### Challenge Description

____

- Bring the concept/standard of ERC-20 from Ethereum to Cardano

```solidity
function name() public view returns (string)

function symbol() public view returns (string)

function decimals() public view returns (uint8)

function totalSupply() public view returns (uint256)

function balanceOf(address _owner) public view returns (uint256 balance)

function transfer(address _to, uint256 _value) public returns (bool success)

function transferFrom(address _from, address _to, uint256 _value) public returns (bool success)

function approve(address _spender, uint256 _value) public returns (bool success)

function allowance(address _owner, address _spender) public view returns (uint256 remaining)
```

- Logic implementations should follow this library [Openzeppelin ERC-20](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/ERC20.sol)
- Please note that your logic is allowed to change so that it could adapt Cardano architecture and data structure layout as long as it maintains its securities and features similarly as the original library

#### Requirements

____

- Your CERC-20 (Cardano ERC-20) library should be deployed on Cardano network (local or public testnet)
- The program should demonstrate these three essential tasks:
  - Token minting
  - Balance query
  - Token transfer
- Provide README to instruct on how to test/verify your submission
