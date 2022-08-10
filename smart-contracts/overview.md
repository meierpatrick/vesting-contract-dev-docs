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

* ``[`name()`](overview.md#name-string)``
* ``[`symbol()`](overview.md#symbol-string)``
* ``[`decimals()`](overview.md#decimals-uint8)``
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

Returns the symbol of the token, usually a shorter version of the name.

</details>

<details>

<summary>decimals () → uint8</summary>

Returns the number of decimals used to get its user representation. For example, if `decimals` equals `2`, a balance of `505` tokens should be displayed to a user as `5.05` (`505 / 10 ** 2`).

Tokens usually opt for a value of 18, imitating the relationship between Ether and Wei. This is the value [`ERC20`](https://docs.openzeppelin.com/contracts/4.x/api/token/erc20#ERC20) uses, unless this function is overridden.

</details>
