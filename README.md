##METACRAFTERS
##CREATING A TOKEN

“This Solidity program demonstrates the basic syntax and functionality of CREATING A TOKEN. This is a starting point for those new to Solidity  to understand how it works. The purpose of this program is to generate tokens and knowledge about the Solidity programming language."

#Explanation

This Solidity program is the main contract written for smart contracts on the Ethereum blockchain. It contains variables such as public and mapping as well as minting and burning functions. This program provides an excellent introduction to Solidity programming and provides a simple understanding of the syntax. It serves as a springboard for beginners and provides them with a foundation for tackling more complex projects in the future.

#Beginning

Implementation of Use Remix, Solidity's web IDE. First go to the Remix website at https://remix.ethereum.org/ and start the program there.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:

//SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

// public variables here
string public tokenname = "BETA";
string public tokenabbrv = "BTA";
uint public totalsupply = 0;

// mapping variable here
mapping(address => uint) public balances;

// mint function
function mint (address _address, uint _value) public {
    totalsupply += _value;
    balances[_address] += _value;
}

// burn function
function burn (address _address, uint _value) public {
    if (balances[_address] >= _value) {
    totalsupply -= _value;
    balances[_address] -= _value;
    }
}
}

To compile the code, click  the Solidity Compiler tab in the left sidebar. Make sure the “Compiler” option is set to “0.8.4”. (or another compatible version) and then click  the “Compile MyToken.sol” button. Button.

Once the code is compiled, you can deploy the contract by clicking  the “Deploy &” button. “. Perform Operations” in the left sidebar. Select the “My Token” contract from the drop-down menu and then click  the “Deploy” button.

Once the contract is deployed, you can interact with it by accessing the Mint and Burn functions. Click “MyToken” contract in the left sidebar and click token name, tokenabbrv, totelsupply and then click “mint” button to trade. Finally, click on the “Transaction” button. Click on the button to execute the function and  mint coins. Similarly, click the “burn” button to remove some coins.


#License

This project is licensed under SPDX-License-Identifier: MIT
