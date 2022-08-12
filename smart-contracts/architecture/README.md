# Architecture

### Architecture

There are a few core contracts that implement the behavior specified in the EIP:

* `IBEP20`: the interface all BEP20 implementations should conform to
* `BEP20`: the base implementation of the BEP20 interface

Additionally, there are multiple custom extensions, including:

* designation of addresses that can create token supply ([`ERC20Mintable`](https://docs.openzeppelin.com/contracts/2.x/api/token/erc20#ERC20Mintable)), with an optional maximum cap ([`ERC20Capped`](https://docs.openzeppelin.com/contracts/2.x/api/token/erc20#ERC20Capped))
* destruction of own tokens ([`ERC20Burnable`](https://docs.openzeppelin.com/contracts/2.x/api/token/erc20#ERC20Burnable))
* designation of addresses that can pause token operations for all users ([`ERC20Pausable`](https://docs.openzeppelin.com/contracts/2.x/api/token/erc20#ERC20Pausable)).

Finally, there are some utilities to interact with ERC20 contracts in various ways.

* [`SafeERC20`](https://docs.openzeppelin.com/contracts/2.x/api/token/erc20#SafeERC20) is a wrapper around the interface that eliminates the need to handle boolean return values.
* [`TokenTimelock`](https://docs.openzeppelin.com/contracts/2.x/api/token/erc20#TokenTimelock) can hold tokens for a beneficiary until a specified time.

### Building Tools

**Programming languages:**

* Solidity
* Javascript

#### Runtime environment:

* Node.js

#### Package Managers:

* NPM

#### Frameworks:

* Truffle
* OpenZeppelin

#### Testing Frameworks:

* Mocha
* Chai

#### Hosting platform:

* GitHub
