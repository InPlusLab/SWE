# High Gas Consumption Data

In solidity, some data types may cost more gas in smart contracts. For example, *bytes* and *byte[]* are both dynamically-sized byte arrays, but *byte[]* cost more gas than *bytes*, as it is not tightly packed in calldata and allocate 32 bytes for each element, which means a great waste of memory. In contrast, *bytes* is packed tightly in calldata, meaning less gas cost and memory usage.
