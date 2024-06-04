// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // Public variables to store the details about the coin
    string public n;
    string public s;
    uint256 public t;

    // Mapping of addresses to balances
    mapping(address => uint256) public balances;

    // Constructor to initialize the token name, symbol, and initial supply
    constructor(string memory _name, string memory _symbol, uint256 _initialSupply) {
        n = _name;
        t = _initialSupply;
        s = _symbol;
        balances[msg.sender] = _initialSupply;
    }

    // Mint function to increase total supply and balance of an address
    function mint(address _to, uint256 _value) public {
        t += _value;
        balances[_to] += _value;
    }

    // Burn function to decrease total supply and balance of an address
    function burn(address _from, uint256 _value) public {
        require(balances[_from] >= _value, "Insufficient balance to burn");
        t -= _value;
        balances[_from] -= _value;
    }
}
