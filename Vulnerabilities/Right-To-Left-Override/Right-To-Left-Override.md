# Right-To-Left-Override

The presence of the right-to-left-override control character (U+202E) in smart contracts creates a weakness that malicious actors can exploit. By using Unicode characters that cover from right to left, these actors can force the rendering of RTL text, leading users to misunderstand the true purpose of the contract. Given that the U+202E character has very few legitimate uses, it should not be present in the source code of smart contracts.
