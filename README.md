# DegenToken Contract

The DegenToken represents an ERC-20 token contract that facilitates the creation of redeemable tokens while incorporating standard ERC-20 functionalities. This contract is specifically designed for deployment on the Ethereum blockchain.

## Overview

The DegenToken contract incorporates the following key features:

1. **Redeemable Tokens**: Users have the ability to create redeemable tokens by specifying a name and an amount, with later redemption possible by other users.

2. **Minting**: Exclusive to the contract owner, the minting functionality provides control over the token supply.

3. **Decimals**: The token operates with 0 decimal places, functioning as a whole number.

4. **Balance Inquiry**: Users can conveniently check their Degen token balance.

5. **Token Transfer**: The contract supports the transfer of Degen tokens from one address to another.

6. **Token Burning**: Users are empowered to burn their own tokens, effectively reducing the total supply.

7. **Token Redemption**: Users can redeem tokens created by their peers.

## Contract Functions

### `createRedeem(string memory _name, uint256 _amount) external`

Empowers users to create redeemable tokens with specified names and amounts.

### `mint(address to, uint amount) public onlyOwner`

Exclusively enables the contract owner to mint new tokens and allocate them to a designated address.

### `decimals() override public pure returns (uint8)`

Overrides the ERC-20 function to specify the token's decimal places (0 in this instance).

### `getBalance() external view returns(uint256)`

Permits users to query their Degen token balance.

### `transferTokens(address _receiver, uint256 _value) external`

Facilitates the transfer of Degen tokens from one address to another.

### `burnTokens(uint amount) external`

Allows users to burn a specified amount of their own tokens.

### `redeemToken(uint8 redeemID_) external`

Enables users to redeem tokens by transferring them to their own address.

### `viewRedeemOwner(uint8 redeemID_) public view returns (address)`

Grants users the ability to view the owner of a specific redeemable token.

### `showRedeem(uint id_) public view returns (Redeemer memory)`

Provides users with the details of a particular redeemable token.

## Modifiers

### `onlyOwner`

Ensures that only the contract owner can execute specific functions.

## Usage

To deploy and engage with the DegenToken contract, adhere to these steps:

1. Deploy the contract onto the Ethereum blockchain.
2. As the owner, utilize the `mint` function to create new tokens.
3. Users can initiate the creation of redeemable tokens through the `createRedeem` function.
4. Users are free to transfer, burn, and redeem tokens according to their requirements.

Note: Utilize a compatible Ethereum wallet or development environment for seamless interaction with the contract.

## Deployment

The contract has been successfully deployed and verified at '0xC60f31334f0b52E589B0dB6BFbA33DE48046Bee2'.