# Clarity Language

The Clarity smart contract language optimizes for predictability and security. Smart contracts allow developers to encode essential business logic on a blockchain. These contracts execute in an open, verifiable, and secure way.

**Clarity is a decidable language**. A programming language is decidable if you can know, with certainty, from the code itself what the program will do. Clarity is intentionally Turing incomplete as it avoids “Turing complexity.” This allows for complete static analysis of the entire call graph of a given smart contract. Further, our support for types and type checker can eliminate whole classes of bugs like unintended casts, reentrancy bugs, and reads of uninitialized values. Finally, you can analyze Clarity code for runtime cost and data usage. This empowers developers to predict what a given Clarity program will do, and how much it will cost.

**In addition to being a decidable language, Clarity is also interpreted**. The contract source code itself is published and executed by blockchain nodes. Removing any intermediate, compiled representation (e.g., EVM byte code for Solidity) further minimizes the surface area for introducing bugs. Publishing the contract source code also optimizes understandability. Compiler bugs are doubly damaging in blockchains because while the programmed source code may not have an error, the eventual program reaching the blockchain could have errors. Any such errors would require contentious hard forks — which are potentially infeasible — to remedy.

Clarity is currently being developed by [Blockstack](https://github.com/blockstack) and [Algorand](https://github.com/algorand), where the respective blockchains of these projects will have Clarity virtual machines (VMs).

## Language design

Clarity differs from most other smart contract languages in two essential ways:

* The language is interpreted and broadcasted on the blockchain as is (not compiled)
* The language is decidable (not Turing complete)

Using an interpreted language ensures that the executed code is human-readable and auditable. A decidable language like Clarity makes it possible to determine precisely which code is going to be executed, for any function.

A Clarity smart contract is composed of two parts — a data space and a set of functions. Only the associated smart contract may modify its corresponding data space on the blockchain. Functions may be private and thus callable only from within the smart contract, or public and thus callable from other contracts. Users call smart contracts’ public functions by broadcasting a transaction on the blockchain which invokes the public function. Contracts can also call public functions from other smart contracts.

Note some of the key Clarity language rules and limitations.

* The only primitive types are booleans, integers, buffers, and principals
* Recursion is illegal and there are no anonymous functions.
* Looping may only be performed via map, filter, or fold
* There is support for lists, however, the only variable length lists in the language appear as function inputs; There is no support for list operations like append or join.
* Variables are immutable.

## Learning Clarity

You can try a [Hello World tutorial](https://github.com/clarity-lang/overview/blob/master/tutorial-hello-world.md) or jump right into the [language reference](https://github.com/clarity-lang/reference/blob/master/reference.md).
