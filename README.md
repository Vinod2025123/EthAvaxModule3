# CustomToken Solidity Smart Contract

## Overview

This Solidity smart contract implements a custom ERC20 token named CustomToken. It allows for minting, transferring, and burning of tokens, with functionality restricted to the contract owner.

## Installation

1. Ensure you have a compatible development environment with Solidity compiler version ^0.8.0.
2. Install OpenZeppelin library:


3. Deploy the contract to your desired Ethereum network.

## Contract Details

- **Name**: CustomToken
- **Inherits from**: ERC20
- **License**: MIT

## Usage

1. **Constructor**:

Initialize the contract with the desired name and symbol. Only the contract creator becomes the owner.

```solidity
constructor(string memory _name, string memory _symbol) ERC20(_name, _symbol)
function mint(address _to, uint256 _amount) public onlyOwner
function transferTokens(address _to, uint256 _amount) public
function burnTokens(uint256 _amount) public



constructor(string memory _name, string memory _symbol) ERC20(_name, _symbol)
Modifiers:

onlyOwner: Restricts access to certain functions only to the owner.
Functions:

## Functions:

- mint: Mint new tokens and assign them to a specified address.
  function mint(address _to, uint256 _amount) public onlyOwner
-`transferTokens: Transfer tokens from the sender's address to the specified address.`

- `function transferTokens(address _to, uint256 _amount) public`
burnTokens: Burn tokens from the sender's address.
- `function burnTokens(uint256 _amount) public`

## Security Considerations

- Ensure that only trusted entities are designated as owners to prevent unauthorized access to critical functions.
- Exercise caution when minting and burning tokens, as these actions can affect token supply and user balances.

## License

- This smart contract is licensed under the MIT License. See the LICENSE file for details.
