# Task 2Task-2CREATE-A-CUSTOM-ERC-20-TOKEN-USING-SOLIDITY-AND-DEPLOY-IT-ON-AN-ETHEREUM-TESTNET.
## Description
This project is part of the CodTech Blockchain Internship Task 2. It involves creating and deploying a custom ERC-20 token using Solidity and Hardhat.
## Token Details:
Token Name: MyToken

Token Symbol: MTK

Decimals: 18 (default for ERC-20)

Initial Supply: You can pass the number during deployment (e.g., 1000000)
## Contract code 

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract MyToken is ERC20 {
    constructor(uint256 initialSupply) ERC20("MyToken", "MTK") {
        _mint(msg.sender, initialSupply * (10 ** decimals()));
    }
}

## Deployment Steps
Compile the contract:
 npx hardhat compile
Run the deployment script (Hardhat in-memory testnet):

npx hardhat run scripts/deploy.js
## Deployment output
0xd8b934580fcE35a11B58C6D73aDeE468a2833fa8 
