**Solidity Assessment*

The goal of this assessment is to create and deploy a simple Solidity smart contract on any blockchain of your choice. Here's what we want you to do:

1. Write a Smart Contract in Solidity: Your smart contract should allow a user to deposit and withdraw ether (or equivalent currency in the chain of your choice). We want the smart contract to maintain an internal ledger of these transactions for each address. 

2. Deploy the Smart Contract: Use any development environment that you're comfortable with (e.g., Truffle, Remix) to compile and deploy the smart contract. 

3. Interact with the Smart Contract: Write a simple JavaScript script using web3.js to interact with the contract and test its functions. 

Here is a basic placeholder code snippet of a solidity contract:

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract LedgerContract {
    mapping(address => uint) public balances;

    function deposit() public payable {
        balances[msg.sender] += msg.value;
    }

    function withdraw(uint _amount) public {
        require(balances[msg.sender] >= _amount, "Insufficient balance.");
        balances[msg.sender] -= _amount;
        payable(msg.sender).transfer(_amount);
    }

    function getBalance() public view returns (uint) {
        return balances[msg.sender];
    }
}
```

**Submission Instructions:**

1. Push all your code to a public GitHub repository and include a README file with instructions on how to compile and deploy your contract. The README should also explain how to run your JavaScript script to interact with the contract. 

2. Record a short demo video (no longer than 10 minutes) that demonstrates the deployment of your smart contract and interaction with it through the script. You can upload this video to a platform of your choice (e.g., YouTube, Vimeo) and include the link in your README file. 

3. Send the link to your public GitHub repository to us by the due date.

**Review Guidelines:**

When reviewing the assessment, we will be looking at the following criteria:

1. Functionality: Does the smart contract compile without errors? Can it be deployed successfully? Does it perform the tasks as specified in the assessment?

2. Code Quality: Is the code clean, well-organized, and easy to read? Does it follow common best practices for Solidity?

3. Understanding: Does the demo video clearly demonstrate an understanding of smart contract development, deployment, and interaction?

4. Documentation: Is the README file well-written and does it clearly explain how to use the code?

Remember, there is no single correct solution to this assignment, and creativity is encouraged. We're looking forward to seeing your work!