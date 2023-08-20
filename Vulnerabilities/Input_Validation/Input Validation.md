# Input Validation

Input validation is a method to protect contract functions from being invoked appropriately. Due to different business scenarios, real-world contracts are heterogeneous regarding input checks. We illustrate this weakness through a classic attack mentioned in three papers, i.e. the short address attack. For example, *transfer(address _to, uint256 _value)* is a standard function in ERC20 token contract. If the address variable *_to* is less than 32 bytes, such as 30 bytes, the entire binary input will left-shift by 2 bytes, and the missing byte on the right side will be completed by 2 zero bytes, which means the second variable *_value* will be multiplied by 4. If input validation is lacking, hackers can transfer tokens than expected.