 # Strict assert()

 The *assert()* is similar to the *require()* in that it checks for certain conditions before executing the rest of the code. However, unlike *require()*, *assert()* throws an invalid opcode exception when the condition is met, which permanently stops and invalidates the contract. Therefore, *assert()* is often used to check whether the state of a contract is normal, and developers should use *assert()* more carefully.
