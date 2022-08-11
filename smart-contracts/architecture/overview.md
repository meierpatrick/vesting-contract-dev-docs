---
description: >-
  The IBEP20 interface standard to create token contracts on Binance Smart
  Chain.
---

# Main Contract

## About the Main Contract

![](../../.gitbook/assets/home.gif)

The following standard defines the implementation of APIs for token smart contracts. It is proposed by deriving the ERC20 protocol of Ethereum and provides the basic functionality to transfer tokens, allow tokens to be approved so they can be spent by another on-chain third party, and transfer between Binance Chain and Binance Smart Chain.

### The Characteristics

* [x] BEP20 standard that implements the interface IBEP20
* [x] Upgradeable contract using initializers​
* [x] Solidity best practices
* [x] Binance verified contracts

### MainContract (MainContract.sol)

<mark style="color:blue;">**Functions:**</mark>

* [name()](overview.md#name-string)
* [symbol()](overview.md#symbol-string)
* [decimals()](overview.md#decimals-uint8)
* [totalSupply()](overview.md#undefined)
* [balanceOf(account)](overview.md#undefined-1)
* [getOwner()](overview.md#undefined-2)
* [transfer(to, amount)](overview.md#transferfrom-address-from-address-to-uint256-amount-bool)
* [transferFrom(from, to, amount)](overview.md#undefined)
* [approve(spender, amount)](overview.md#undefined-1)
* [alllowance(owner, spender)](overview.md#undefined-2)

<mark style="color:blue;">**Events:**</mark>

* [Transfer()](overview.md#transfer-address-from-address-to-uint256-value)
* [Approval()](overview.md#approval-address-owner-address-spender-uint256-value)

<details>

<summary>name () → string</summary>

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

<details>

<summary>totalSupply () → uint256</summary>



</details>

<details>

<summary>balanceOf (address account) → uint256</summary>

See [`IERC20.balanceOf`](https://docs.openzeppelin.com/contracts/4.x/api/token/erc20#IERC20-balanceOf-address-).

</details>

<details>

<summary>getOwner () → uint256</summary>

Returns the bep20 token owner which is necessary for binding with bep2 token.

</details>

<details>

<summary>transfer (address to, uint256 amount) → bool</summary>

Moves `amount` tokens from the caller’s account to `to`.

Returns a boolean value indicating whether the operation succeeded.

Emits a [`Transfer`](https://docs.openzeppelin.com/contracts/4.x/api/token/erc20#IERC20-Transfer-address-address-uint256-) event.

</details>

<details>

<summary>transferFrom (address from, address to, uint256 amount) → bool</summary>

Emits an [`Approval`](https://docs.openzeppelin.com/contracts/4.x/api/token/erc20#IERC20-Approval-address-address-uint256-) event indicating the updated allowance. This is not required by the EIP. See the note at the beginning of [`ERC20`](https://docs.openzeppelin.com/contracts/4.x/api/token/erc20#ERC20).

</details>

<details>

<summary>approve (address spender, uint256 amount) → bool</summary>

If `amount` is the maximum `uint256`, the allowance is not updated on `transferFrom`. This is semantically equivalent to an infinite approval.

</details>

<details>

<summary>allowance (address owner, address spender) → uint256</summary>

See [`IERC20.allowance`](https://docs.openzeppelin.com/contracts/4.x/api/token/erc20#IERC20-allowance-address-address-).

</details>

<details>

<summary>Transfer (address from, address to, uint256 value)</summary>

Emitted when `value` tokens are moved from one account (`from`) to another (`to`).

Note that `value` may be zero.

</details>

<details>

<summary>Approval (address owner, address spender, uint256 value)</summary>

Emitted when the allowance of a `spender` for an `owner` is set by a call to [`approve`](https://docs.openzeppelin.com/contracts/4.x/api/token/erc20#IERC20-approve-address-uint256-). `value` is the new allowance.

</details>

### Utils Contracts

```solidity
import "./IBEP20.sol";
import "./PrivateSale.sol";
import "./VestingController.sol";
import "@openzeppelin/contracts/utils/math/SafeMath.sol";
import "@openzeppelin/contracts/access/Ownable.sol";
import "@openzeppelin/contracts/utils/Context.sol";
```
