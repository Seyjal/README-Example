# Project Title

The provided Solidity code defines a contract named "transactionLimit" .It includes a private variable named "limit" and the three functions: checkRequire, checkAssert, and checkRevert, all aiming to achieve the same result but using different syntax .

## Description

Within a blockchain network, the code defines a smart contract called transactionLimit that sets a limit on transaction quantities. This contract makes use of three fundamental functions: checkRequire, checkAssert, and checkRevert. Each of these functions uses a unique strategy to accomplish the same goal, which is to make sure that transactions stay under a predetermined limit.
All three functions accomplish the same goal of limiting the transaction amount, but they handle violations differently. 

## Getting Started

### Installing

* How/where to download your program
* Any modifications needed to be made to files/folders

### Executing program
Let's examine each role in more detail:

check_require: This function mimics the use of a require statement, a popular smart contract condition enforcement mechanism. A ValueError exception is raised by the function if the amount supplied in exceeds the limit. The transaction is stopped by this exception, which also keeps it from being carried out on the blockchain.

check_assert: This function, mimics an assert statement. It verifies whether the amount is less than or equal to the limit, just like require. On the other hand, it throws an AssertionError if the condition is not met. Assertions, in contrast to require, are typically used for development and may be turned off in production settings to prevent transactions from stopping

check_revert: a more versatile method of reversing transactions in Solidity. It performs a similar amount check to the other functions. It prints a notice indicating that the transaction is reverted if it exceeds the limit, and it then mimics the halting behavior of a revert in Solidity using a return statement.

In conclusion, while addressing violations is accomplished through various ways, all three operations have the same goal of enforcing the transaction limit. Smart contracts in production usually employ require and reverse, whereas assert is primarily used for development and testing.


## Result Analysis

Based on the amount given, the functions would react as follows:

value within limit: All three functions (checkRequire, checkAssert, and checkRevert) would return "completed," signifying a successful verification, if the transaction value was less than or equal to the provided limit (default 10).

Amount surpasses the limit:
verifyRequire: If this function were to execute, the transaction would not be able to proceed since a ValueError exception would be raised with the message "Amount Greater than limit".
verifyAssert: In certain cases (based on the environment), this function might raise an AssertionError and stop the transaction from being executed.
verifyRevert: To essentially halt the transaction, this function would print "Transaction reverted: Amount Greater than limit" and mimic a transaction revert.

## Authors

Metacrafter 
Seyjal 



