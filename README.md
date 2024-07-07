# Solidity functions

This is a simple program that does some basic functions such as minting tokens, burning tokens, etc. This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract shows the working of a few functions. This program serves as a simple introduction on how to execute the functions on the blockchain using solidity and can be used as a stepping stone for more complex projects in the future.

## Description

For this assessment, I have created a contract that does the following functions :

1. There is a mint function that takes two parameters: an address and a value. This function is a simple demonstration of how to mint tokens.
2. The next function we have is a burn function where we burn or destroy the tokens we have. A precaution we have to take in this function is to make sure that we 
   don't burn more tokens than we have.
   
This assessment is focused on familiarising with the different functions that can be done to the tokens we have using solidity. It is one of the simplest solidity programs that helps us understand and gain knowledge about this language and about the working of tokens in the world of cryptocurrency. This is just a demonstration of minting and burning of tokens and is not the right way to do it.

## Getting Started

### Executing Program
* Running the code
  
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at (https://remix.ethereum.org/). Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (eg. Functions.sol). Copy and paste the following code into the file:
```javascript
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;



contract DemoToken {

    
  string public tName = "GLENN";
  string public tAbbrv = "GM";
  uint public tSupply = 0;

   
  mapping(address => uint) public balance;

  
  function mint (address _add, uint _val) public {
    tSupply += _val;
    balance [_add] += _val;
  }  

    
  function burn (address _add, uint _val) public {
    if (balance[_add] >= _val) {
      tSupply -= _val;
      balance[_add] -= _val;
    }  
  }  
}

```

* Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select your contract from the dropdown menu, and then click on the "Deploy" button.
* Scroll down and you will be able to see the name of your functions and your variables. Go to the "supply and "balance" variables and make sure they are 0 at the beginning of the deployment.
* Next go to the mint function and input an address (a list of random addresses with 100 ether can be found on top of the deployment page, copy paste one of those) and the number of wei to be minted. Now if you click on the "balances" and "supply" buttons you will be able to see the number of wei which you have minted.
* Then go to the burn function and input the same address used for mint function and the number of wei to be burned. After you transact this and see the "balances" and "supply" you will see that the number of leftover wei would have reduced by the same number of wei that you burned.
* Now to make sure that the program is working completely just try burning more wei than you have balance. You will see there is no change in the "balance" and "supply".

## Author

[@GlennMicheal](https://github.com/fortune-rider)
