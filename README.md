# Clarity Language

The Clarity smart contract language optimizes for predictability and security. Smart contracts allow developers to encode essential business logic on a blockchain. These contracts execute in an open, verifiable, and secure way.

**Clarity is a decidable language**. A programming language is decidable if you can know, with certainty, from the code itself what the program will do. Clarity is intentionally Turing incomplete as it avoids “Turing complexity.” This allows for complete static analysis of the entire call graph of a given smart contract. Further, our support for types and type checker can eliminate whole classes of bugs like unintended casts, reentrancy bugs, and reads of uninitialized values. Finally, you can analyze Clarity code for runtime cost and data usage. This empowers developers to predict what a given Clarity program will do, and how much it will cost.

**In addition to being a decidable language, Clarity is also interpreted**. The contract source code itself is published and executed by blockchain nodes. Removing any intermediate, compiled representation (e.g., EVM byte code for Solidity) further minimizes the surface area for introducing bugs. Publishing the contract source code also optimizes understandability. Compiler bugs are doubly damaging in blockchains because while the programmed source code may not have an error, the eventual program reaching the blockchain could have errors. Any such errors would require contentious hard forks — which are potentially infeasible — to remedy.

Clarity is currently being developed by [Blockstack](https://github.com/blockstack) and [Algorand](https://github.com/algorand), where the respective blockchains of these projects will have Clarity virtual machines (VMs).
