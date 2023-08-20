# Unsafe Constructor

Before Solidity 0.4.22, developers could only define a constructor by declaring a function with the same name as the contract. This function is executed during deployment. However, if the developer mistakenly declared the function with an incorrect name, it would not be recognized as a constructor. Instead, it would become an unprotected public function.

To mitigate this issue, one suggested defense method is to update the Solidity version to 0.4.22 or higher. Starting from that version, developers can use the constructor keyword to explicitly define a constructor function.
