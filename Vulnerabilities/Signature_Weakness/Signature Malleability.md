# Signature Malleability

This weakness allows attackers to modify the signature of a transaction without invalidating it, which can be used to perform a replay attack or modify the transaction's data. To mitigate this weakness, developers should use signature schemes resistant to malleability or techniques such as signature normalization to prevent tampering.

This weakness occurs when an attacker modifies the signature from an existing transaction without invalidating it, which can be used to perform replay attacks or modify the transaction data. A well-known case is the ECRecovery library, which supports multiple valid *(r, s, v)* signatures for the same content.
The attacker can replay the signatures multiple times, causing unintended actions or draining funds from the contract.
