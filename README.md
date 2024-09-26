Solidity Intermediate Assessment First Module project
This project Base on solidity.

Description
This project implement three statements revert(),assert(),require() in Smart contract.
These statements used for validating conditins and handling exceptions in smart contracts.

Getting Started
Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org.
Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar.
Save the file with a .sol extension (e.g., solidity.sol). Copy the code form Function.sol into the file and paste in Remix.
There are three function in this contract setValue, deposit and withdraw they have require(), assert() and revert() statement respectively.
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile solidity.sol" button.
Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar.
Then click the "Deploy" button.
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.18;

contract OwnershipContract {
    address public owner;

    constructor() {
        owner = msg.sender;
    }

    function onlyOwner() public view {
        require(msg.sender == owner, "Only the owner can call this function.");
    }

    function onwerHere() public view {
        if(msg.sender!= owner){
            revert("The caller is not the owner.");
        }
    }

    function Owner() public view {
        assert(msg.sender == owner);
    }
}
