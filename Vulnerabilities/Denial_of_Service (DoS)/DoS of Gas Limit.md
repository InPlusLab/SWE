# DoS of Gas Limit

DoS with gas limitation is another type of DoS weakness. Contract developers may construct loops in the contracts that contain large amounts of gas, and attackers can deplete the gas consumption by increasing the round of the loops. Some operations with high gas consumption (e.g., storing data, encrypting data, external calls, etc.) should be carefully avoided for multiple executions. Saving gas or decoupling high-gas operations to multiple transactions can mitigate this weakness.
