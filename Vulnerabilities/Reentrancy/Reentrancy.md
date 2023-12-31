# Reentrancy
Reentrancy is a common weakness in smart contracts.

This weakness is related to the fallback mechanism of Ether and other tokens. 
The fallback mechanism allows the executed contract to switch contexts to other external contracts after performing some specific operations (e.g., ether/token transfer).

For example, a smart contract can define an anonymous fallback function that will be automatically executed when the contract receives Ethers. By re-invoking the external function in the fallback function, a malicious contract can circularly execute the transfer logic in the external function.
Notably, the fallback function is executed immediately after the transfer rather than after the entire external function has been executed. 
Hence, if the victim contract only updates the important variables (e.g., recording and limiting the transfer amount) after the transfer operation, the malicious contract can successfully execute multiple unchecked transfer operations before the contract state changes. Similar to Ether transfer, reentrancy attacks can also occur in token contracts, and developers should pay attention to functions with fallback-like execution conditions.

Checks Effects Interactions pattern is a method to avoid this weakness. The CEI pattern involves structuring smart contracts into three processes: checks, effects, and interactions. In the checks process, the smart contract verifies that the input parameters are valid and that the caller has the necessary permissions to execute the function. In the effects process, the smart contract updates the state of the contract and performs any necessary calculations or data transformations (e.g., recording and limiting the transfer amount). Finally, the smart contract transfers Ether to other accounts in the interactions phase. As the transfer behavior is executed after checks and effects, the malicious re-invoke via the fallback function can not bypass the necessary checks as the contract state has changed.
