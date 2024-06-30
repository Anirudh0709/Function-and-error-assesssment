## Alpha Contract
The AplhaContract project is a simple Solidity-based smart contract. This Solidity smart contract demonstrates the use of require(), assert(), and revert() statements to handle different conditions and errors effectively. It includes functions that validate inputs, ensure internal invariants, and manage complex conditions to ensure robust and predictable contract behavior
## Description
This Solidity smart contract is designed to illustrate the practical use of the require(), assert(), and revert() statements for error handling and validation. It contains functions to set, double, and reset a number, showcasing how require() is used for input validation, assert() ensures internal correctness, and revert() manages complex conditions. Additionally, a function demonstrating multiple checks and conditional reversion is included, highlighting the robustness and predictability these statements bring to smart contract development.
## Getting Started
### Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.
Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Create function.sol). Copy and paste the following code into the file:

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract AplhaContract {
  
    uint256 public number;

   
    function setNumber(uint256 _number) public {
    
        require(_number > 0, "Number must be greater than zero");
        number = _number;
    }

   
    function doubleNumber() public {
        
        assert(number > 0);
        number *= 2;
    }


    function resetNumber() public {

        if (number % 2 != 0) {
            revert("Number must be even to reset");
        }
        number = 0;
    }
    function complexFunction(uint256 _a, uint256 _b) public pure returns (uint256) {
        require(_a > 0, "First parameter must be greater than zero");
        require(_b > 0, "Second parameter must be greater than zero");

        uint256 result = _a + _b;

        if (result % 2 != 0) {
            revert("The result must be an even number");
        }

        return result;
    }
}


## Help
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.0" (or another compatible version), and then click on the "Compile Create function.sol" button.
Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. 

## Authors
Anirudh
@ anirudhgahlawat80@gmail.com
## License
This project is licensed under the MIT License - see the LICENSE.md file for details
