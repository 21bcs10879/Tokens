# Tokens

This Solidity program is a simple "Token" program that basically mints and burn tokens and displays the total supply and balance.

## Description
This smart contract provides basic functionality to manage a token system, including:
1.Publicly accessible details about the token (name and abbreviation).
2.A mapping to keep track of user balances.
3.Functions to mint (create) and burn (destroy) tokens, with appropriate checks to ensure balances are maintained correctly.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Tokens.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.18;

contract MyToken {
    // Public variables here
    string public tokenName = "Skyline";
    string public tokenAbbrv = "SKY";
    uint public totalSupply = 0;

    // Mapping variable here
    mapping(address => uint) public balances;

    // Mint function
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // Burn function
    function burn(address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile Tokens.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "Tokens" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by an account address and value, then simply click transact and you can check the updated balance.
## Authors

Metacrafter Learner  
https://github.com/21bcs10879


## License

This project is licensed under the MIT License - see the LICENSE.md file for details# Tokens
