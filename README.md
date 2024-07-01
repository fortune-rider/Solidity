# Solidity functions

This is a simple program that shows the working of some basic solidity functions. This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract shows the working of a few inbuilt solidity functions. This program serves as a simple and straightforward introduction to Solidity programming, and can be used as a stepping stone for more complex projects in the future.

# Description

For this assessment, I have created a contract to fulfill the following requirements:

1. The contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
2. The contract will have a mapping of addresses to balances (address => uint)
3. There will be a mint function that takes two parameters: an address and a value. The function then increases the total supply by that number and increases the balance of the address by that amount.
4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. It will take an address and value just like the mint functions. It will then deduct the value 
   from the total supply and from the balance of the address.
5. Lastly, your burn function should have conditionals to make sure the balance of account is greater than or equal to the amount that is supposed to be burned.
