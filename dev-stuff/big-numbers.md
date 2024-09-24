# Big Numbers

Some confusion exists when it comes to the numeric type in an EVM blockchain and JavaScript libraries interacting with EVM contracts.

EVM blockchains uses unsigned integer: 

- `uint` and `unit256` : 256 bits of storage
- `uint8` : 8 bits of storage
- `uint16` : ditto with 16 bits

Since Solidity versions `0.8.0` numeric overflows triggers a revert of the transaction.

### BigInt Java Script

- BigInt 
- a = 123n
- Operations: 23n*1928N
- Often used with JavaScript contract libraries

### BigNumber: @ethersproject/bignumber

- used bn.js
- no decimals


### Web3

- https://docs.web3js.org/
