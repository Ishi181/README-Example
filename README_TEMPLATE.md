# Project Title

CREATE A TOKEN

## Description

    1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
    2. Your contract will have a mapping of addresses to balances (address => uint)
    3. You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the “sender” address by that amount
    4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the “sender”.
    5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
       to the amount that is supposed to be burned.



## Getting Started

ENVIRONMENT

This code we are running on the online Solidity IDE that is https://remix.ethereum.org/ here we'll perform the code. as we are on the remix website just by clicking on the start coding we'll able to do coding in Solidity.

### Executing program

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;
contract MyToken {

    // public variables here
     string public tokenName = "Ishi Singla";
     string public tokenAbbrv = "I S";
     uint public totalSupply = 0;
    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address , uint _value) public {
        
          totalSupply += _value;
          balances[_address] += _value;
        }
     // burn function
    function burn (address _address , uint _value) public {
        if(balances[_address] >= _value) {
        totalSupply -= _value;
        balances[_address] -= _value;

       } else {
       revert("Insufficient balance to burn");
    }
    }
}

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the ("Compile "the name of the file" ") for ex. comple first.sol button. Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "first.sol" contract from the dropdown menu, and then click on the "Deploy" button. then u can see a the below of the option ' Deployed/Unpinned Contracts ' expand it and balances mint burn etc and now u can see our code is ready to run .

## Authors

Contributed by name : Ishi Singla
Email ID : ishisingla181@gmail.com

GITHUB Link :
https://github.com/Ishi181/ETH-assesment/blob/main/README.md%20ETH

Loom Video link :
https://www.loom.com/share/3df26fe8605046518e33c9f13a1cfa5d


## License

This project is licensed under the  MIT License License - see the LICENSE.md file for details
