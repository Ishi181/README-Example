Create a Token

Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
Your contract will have a mapping of addresses to balances (address => uint)
You will have a mint function that takes two parameters: an address and a value. The function then increases the total supply by that number and increases the balance of the address by that amount.
Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. It will take an address and value just like the mint functions. It will then deduct the value from the total supply and from the balance of the address.
Lastly, your burn function should have conditionals to make sure the balance of account is greater than or equal to the amount that is supposed to be burned.

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

/*
       REQUIREMENTS
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
*/

contract MyToken {

    // public variables here

    // mapping variable here

    // mint function

    // burn function

}


# ETH-assesment
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
## Help

Any advise for common problems or issues.
```
command to run if program contains helper info
```

## Authors

Contributors names and contact info

GITHUB Link :
https://github.com/Ishi181/ETH-assesment/blob/main/README.md%20ETH

Loom Video link :
https://www.loom.com/share/3df26fe8605046518e33c9f13a1cfa5d


## License

This project is licensed under the // SPDX-License-Identifier: MIT License - see the LICENSE.md file for details
