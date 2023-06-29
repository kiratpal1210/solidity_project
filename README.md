CREATING MY OWN TOKEN
The project involves the creation of a custom token using the Solidity programming language. Tokens are a fundamental aspect of the Ethereum blockchain ecosystem, representing digital assets that can be transferred and exchanged. By developing your own token, you can explore the underlying concepts of blockchain, smart contracts, and decentralized finance.

Description
This project focuses on creating a custom token using the Solidity programming language within the Remix IDE. Remix is a popular web-based development environment that provides a user-friendly interface for writing, compiling, and deploying smart contracts on the Ethereum blockchain.

Getting Started
Executing program
The project will involve the following steps:

Setting up Remix:

Open the Remix IDE in your web browser.
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.
Creating the Token Contract:
Start a new file in the code editor within Remix. Copy and paste the following code into the file:
''' // SPDX-License-Identifier: MIT pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public token_name = "Kirat";
    string public token_Abbrv = "krt";
    uint public totalSupply = 0;

   // mapping variable here
    mapping (address => uint) public balances; 

  // mint function
    function mint (address Address, uint value) public 
    {
        totalSupply += value;
        balances[Address] += value;
    }


    // burn function
    function burn (address Address, uint value) public
    {
        if (balances[Address]>= value)
        {
            totalSupply -= value;
            balances[Address] -= value;
        }
    }

}

Compiling the Contract:
Use the Remix compiler panel to compile your token contract.
Select the appropriate compiler version i.e 0.8.18.
Deploying the Contract:
Switch to the "Deploy & run transactions" tab in Remix.
Deploy the compiled contract by clicking the "Deploy" button.
Interacting with the Token:
Utilize the Remix IDE to interact with the deployed token contract.
Use the Addresstobalance, mint and burn functions in the "Deployed Contracts" section to perform actions like transferring tokens, checking balances, and burning tokens.
Input the adress and value and click on the corresponding function buttons to execute our contract.

Authors
Kiratpal Singh Kalsey
https://www.linkedin.com/in/kiratpal-singh-kalsey-a92b15230/

License
This project is licensed under the MIT License - see the LICENSE.md file for details.This code is licensed under the MIT License. You can find the license text in the SPDX-License-Identifier comment at the beginning of the contract.

Note: Ensure that you are using a compatible Solidity compiler version (0.8.18) or newer to compile and interact with this contract.
