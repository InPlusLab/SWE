# Missing Return Value

This weakness occurs when a function is expected to return a value but returns nothing, which may lead to some unexpected contract behaviors. For example, suppose a function is designed to return a boolean value indicating whether a transaction was successful or not, but the function fails to return anything. In that case, the caller will get the return value from an invalid location. Since the contract cannot judge the result of an external call, this can potentially allow an attacker to exploit the contract.
