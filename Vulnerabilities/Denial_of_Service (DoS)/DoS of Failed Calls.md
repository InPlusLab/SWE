# DoS of Failed Calls

DoS of failed calls is a classic DOS vulnerability. Smart contracts can interact with other contracts within a single transaction, but failed calls to other contracts can cause z the entire transaction to roll back.

When a contract invokes another contract, the execution of the first contract is suspended until the second contract returns a result. If the second contract fails to execute properly, it will also cause the first contract to fail.
Thus, an attacker creates a contract that intentionally fails when called by another contract (e, by forcing a revert in the function. if the victim contract cannot avoid calling the function, it continues to roll back and cannot continue working.

One way to mitigate this type of attack is to implement response time checks in the contract, which can ensure that calls to other contracts are handled correctly. In addition, operations related to external calls can be further decoupled from other operations to avoid affecting other contract logic due to the failed external calls.
