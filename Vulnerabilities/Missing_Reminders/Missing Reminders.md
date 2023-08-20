# Missing Reminders

This weakness occurs when the contract fails to notify relevant parties of critical operations such as token transfers or changes in contract ownership. Smart contracts are often used for financial transactions and can hold significant value. 
In Solidity, the contract can emit a message by invoking the *emit()* function. In addition, the *require()* function also supports a string parameter to emit an exception message. 
Any changes to the contract state can significantly impact the stakeholders of the smart contract.

For example, when a token transfer is executed, the contract should emit a message for both the sender and the recipient. This notification is important as it provides proof of the transfer and allows parties to track their transactions. 
If the contract fails to provide these notices or alerts, there is potential confusion and disputes between the parties involved. In addition, the lack of alerts may make it more difficult for contract owners to detect hacking transactions and even miss out on time to recoup losses.
