# Hardcoded Gas Limit

In Solidity, a hardcoded gas limit refers to explicitly setting a specific gas limit for the function execution. Although these gas limits can work properly in the present, a potential hard fork in the future may cause gas consumption to rise for operations within certain functions. Therefore, it is not recommended to use functions with hard-coded gas limits (e.g., the transfer() and send() functions forward a fixed amount of 2300 gas), and base statements such as call should be used directly whenever possible.
