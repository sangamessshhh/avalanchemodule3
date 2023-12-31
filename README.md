# Avalanche Module3

I have created a token called Sangamesh and deployed it to Hardhat Network.

## Description

In this project, I have created a token using openzeppelin where you can mint, burn, approve, check the allowance & balance, transfer, transfer ownership and more..

I have deployed this contract that i created to the hardhat network. 

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., mod3.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.9;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

contract Sangamesh is ERC20, Ownable {
    constructor() ERC20("Sangamesh", "SMG") {}

    function mint(address to, uint256 amount) public onlyOwner {
        _mint(to, amount);
    }

    function burn(uint256 amount) public {
        require(balanceOf(msg.sender) >= amount, "Insufficient balance");
        _burn(msg.sender, amount);
    }
}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.9" (or another compatible version), and then click on the "Compile mod3.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "mod3" contract from the dropdown menu, and then click on the "Deploy" button.

### Deploying to Hardhat Network

To deploy it to hardhat network: run the following commands,

```shell
npx hardhat node
```

```shell
npx hardhat run scripts/deploy.js
```


## Authors

Sangamesh Y

@sangamessshhh@gmail.com


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
