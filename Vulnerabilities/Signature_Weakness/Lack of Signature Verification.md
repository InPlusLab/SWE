# Lack of Signature Verification

This weakness occurs when the smart contract does not properly verify the signature sender, allowing attackers to execute unauthorized transactions. A famous example is relying on *msg.sender* to identify the signature creator. However, transactions can be created from a proxy contract, meaning the contract can not assume the *msg.sender* signed the signature.
