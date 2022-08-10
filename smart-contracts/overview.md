---
description: >-
  The IBEP20 interface standard to create token contracts on Binance Smart
  Chain.
---

# Main Contract

The following standard defines the implementation of APIs for token smart contracts. It is proposed by deriving the ERC20 protocol of Ethereum and provides the basic functionality to transfer tokens, allow tokens to be approved so they can be spent by another on-chain third party, and transfer between Binance Chain and Binance Smart Chain.

### The Characteristics

* [x] Lives on the Binance Smart Chain
* [x] Upgradeable
* [x] Does not negatively impact a mobile device’s CPU, battery, or data consumption
* [x] Plays well with other SDKs

### MainContract (MainContract.sol)

<mark style="color:blue;">**Functions:**</mark>

* ``[`name()`](overview.md#symbol-string)``
* `symbol()`
* `decimals()`
* `totalSupply()`
* `balanceOf()`
* `getOwner()`
* `transfer()`
* `transferFrom()`
* `approve()`
* `alllowance()`

<mark style="color:blue;">**Events:**</mark>

* `Transfer()`
* `Approval()`

<details>

<summary>name () → string </summary>

Returns the name of the token - e.g. "MyToken".

</details>

<details>

<summary>symbol () → string </summary>



</details>
