# MyToken 

This is a Solidity Project "MyToken" program in which we have created to a specific address.

## Description

This project creates a token that may be burned and minted. We can mint new tokens to a specific address to increase the Total supply of the "META" token (MTA)," or burn existing tokens from that address to reduce the total supply.

## Getting Started

### Executing program

To run the program use Remix IDE, we have used an Online Platform https://remix.ethereum.org/.

Once you are on the Remix website, create a new file and save the file with a .sol extension (like MyToken.sol). Copy and paste the code into the file:
```javascript
// SPDX-License-Identifier: MIT
pragma solidity 0.8.25;

contract MyToken {

    // public variables here
    string public tokenName = "META";
    string public tokenAbbrv = "MTA";
    uint public totalSupply = 0;
    // mapping variable here
    mapping(address => uint) public balances;
    // mint function
function mint (address _address, uint _value) public{
  totalSupply += _value;
  balances[_address] +=_value;
}

    // burn function
function burn (address _address, uint _value) public{
  if (balances[_address] >= _value) {
      totalSupply -= _value;
      balances[_address] -= _value;
   }
 }

## Authors

Himanshu

### License

This project is licensed under the MIT License - see the LICENSE.md file for details
