# Architecture

### Architecture

There are a few core contracts that implement the behavior specified in the EIP:

* ``[`IBEP20`](overview.md#interface-ibep20-ibep20.sol): the interface all BEP20 implementations should conform to
* ``[`BEP20`](overview.md#core-maincontract-maincontract.sol): the base implementation of the BEP20 interface

Additionally, there are multiple custom extensions, including:

* lock tokens during a private sale from withdrawal until the timer ends ([`PrivateSale`](private-sale-contract.md#about-the-private-sale-contract))
* can release its token balance gradually like a typical vesting scheme, with a cliff and vesting period ([`VestingController`](vesting-controller-contract.md#about-the-vesting-controller-contract))

Finally, there are some utilities to interact with BEP20 contracts in various ways.

* ``[`Ownable`](overview.md#about-the-main-contract) provides a basic access control mechanism, where there is an account (an owner) that can be granted exclusive access to specific functions.
* ``[`Context`](overview.md#about-the-main-contract) delivers the current execution context, including the sender of the transaction and its data.
* ``[`Math`](overview.md) brings standard math utilities missing in the Solidity language.
* ``[`SafeMath`](vesting-controller-contract.md) wraps over Solidity’s arithmetic operations with added overflow checks.
* ``[`TransparentUpgradeableProxy`](overview.md) implements a proxy that is upgradeable by an admin.

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
