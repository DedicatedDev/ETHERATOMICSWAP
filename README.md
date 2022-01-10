# Ethereum Atomic Swap


The Ethereum Atomic Swap library is made up of several different smart contracts that work together to implement atomic swaps. These smart contracts are used by traders after the Republic Protocol has successfully matched their orders. However, traders are not required to use the Republic Protocol to use the Ethereum Atomic Swap contracts.

1. The EtherToERC20 contract implements atomic swaps between Ether and an ERC20 token.
2. The ERC20ToERC20 contract implements atomic swaps between two ERC20 tokens.
3. The Ether contract implements cross-chain atomic swaps where Ether is being used.
4. The ERC20 contract implements cross-chain atomic swaps where an ERC20 token is being used.

None of the contract expose orders. Orders are never passed to the Republic network under any circumstances, and order fragments are never passed to the blockchain. The `_swapID` used by the contracts are only for identifying the swap, and is negotiated between traders. This maintains privacy between traders that have matched on the order book, and atomic swaps that have been executed.

## Tests

Install all NPM modules and Truffle as a global command.

```
npm install --global truffle
npm install
```

Run the `ganache` script. This script needs to continue running in the background; either run it in a separate terminal, or append the `&` symbol.

```sh
./ganache
```

Run the Truffle test suite.

```sh
truffle test
```
