# Unsafe Type Conversion
Solidity supports explicit type conversion, allowing for the conversion of variables from one type to another (e.g., converting a uint8 variable to a uint16 variable). However, it is essential to note that performing variable conversions can pose safety risks in certain situations. 

There are two major types of risky situations. 

(1) Conversion from a signed number to an unsigned number (e.g., converting int256 to uint256). Signed numbers comprise a sign bit and a value bit, where the sign bit indicates positive or negative. In contrast, unsigned numbers contain only a value bit. The sign bit is incorrectly converted to a value bit when converting to unsigned numbers, resulting in incorrect values. 

(2) Conversion from an integer type with more bits to an integer type with fewer bits(e.g., converting uint256 to uint128). In this situation, the corresponding higher bits of the original integer will be discarded, and the converted integer will be smaller than the expected value.
