# Architecture

### Architecture

There are a few core contracts that implement the behavior specified in the EIP:

* ``[`IBEP20`](overview.md#interface-ibep20-ibep20.sol): the interface all BEP20 implementations should conform to
* ``[`BEP20`](overview.md#about-the-main-contract): the base implementation of the BEP20 interface

Additionally, there are multiple custom extensions, including:

* lock tokens during a private sale from withdrawal until the timer ends ([`PrivateSale`](private-sale-contract.md#about-the-private-sale-contract))
* can release its token balance gradually like a typical vesting scheme, with a cliff and vesting period ([`VestingController`](vesting-controller-contract.md#about-the-vesting-controller-contract))

Finally, there are some utilities to interact with BEP20 contracts in various ways.

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
