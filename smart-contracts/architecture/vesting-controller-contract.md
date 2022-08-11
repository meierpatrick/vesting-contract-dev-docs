---
description: >-
  The IBEP20 interface standard to create token contracts on Binance Smart
  Chain.
---

# Vesting Controller Contract

![](../../.gitbook/assets/vestingController.gif)

### About the Vesting Controller Contract

A token holder contract that can release its token balance gradually like a typical vesting scheme, with a cliff and vesting period. Optionally revocable by the owner.

### The Characteristics

* [x] Get funded by the [MainContract.sol](overview.md#about-the-main-contract) contract
* [x] Able to set up individual vesting schedules
* [x] Solidity best practices
* [x] Binance verified contracts

### Core: VestingController (VestingController.sol)

<mark style="color:blue;">**Modifiers:**</mark>

* [onlyOwner()](vesting-controller-contract.md#onlyowner)

<mark style="color:blue;">**Functions:**</mark>

* [constructor (beneficiary, start, cliffDuration, duration, revocable)](vesting-controller-contract.md#constructor-address-beneficiary-uint256-start-uint256-cliffduration-uint256-duration-bool-revocable)
* [beneficiary()](vesting-controller-contract.md#beneficiary-address)
* [cliff()](vesting-controller-contract.md#cliff-uint256)
* [start()](vesting-controller-contract.md#start-uint256)
* [duration()](vesting-controller-contract.md#duration-uint256)
* [revocable()](vesting-controller-contract.md#revocable-bool)
* [released(token)](vesting-controller-contract.md#released-address-token-uint256)
* [revoked(token)](vesting-controller-contract.md#revoked-address-token-bool)
* [release(token)](vesting-controller-contract.md#release-contract-ibep20-token)
* [revoke(token)](vesting-controller-contract.md#revoke-contract-ierc20-token)
* [owner()](vesting-controller-contract.md#owner-address)
* [isOwner()](vesting-controller-contract.md#isowner-bool)
* [renounceOwnership()](vesting-controller-contract.md#renounceownership)
* [transferOwnership(newOwner)](vesting-controller-contract.md#transferownership-address-newowner)

<mark style="color:blue;">**Events:**</mark>

* [TokensReleased(token, amount)](vesting-controller-contract.md#undefined)
* [TokensVestingRevoked(token)](vesting-controller-contract.md#undefined-1)
* [OwnershipTransferred(previousOwner, newOwner)](vesting-controller-contract.md#undefined-2)

<details>

<summary>onlyOwner()</summary>

Throws if called by any account other than the owner.

</details>

<details>

<summary>constructor(address beneficiary, uint256 start, uint256 cliffDuration, uint256 duration, bool revocable)</summary>

Creates a vesting contract that vests its balance of any ERC20 token to the beneficiary, gradually in a linear fashion until start + duration. By then all of the balance will have vested.

</details>

<details>

<summary>beneficiary() → address</summary>



</details>

<details>

<summary>cliff() → uint256</summary>



</details>

<details>

<summary>start() → uint256</summary>



</details>

<details>

<summary>duration() → uint256</summary>



</details>

<details>

<summary>revocable() → bool</summary>



</details>

<details>

<summary>released(address token) → uint256</summary>



</details>

<details>

<summary>revoked(address token) → bool</summary>



</details>

<details>

<summary>release(contract IBEP20 token)</summary>



</details>

<details>

<summary>revoke(contract IERC20 token)</summary>



</details>

<details>

<summary>owner() → address</summary>

Returns the address of the current owner.

</details>

<details>

<summary>isOwner() → bool</summary>

Returns true if the caller is the current owner.

</details>

<details>

<summary>renounceOwnership()</summary>



</details>

<details>

<summary>transferOwnership(address newOwner)</summary>

Transfers ownership of the contract to a new account (`newOwner`). Can only be called by the current owner.

</details>

<details>

<summary>TokensReleased(address token, uint256 amount)</summary>



</details>

<details>

<summary>TokenVestingRevoked(address token)</summary>



</details>

<details>

<summary>OwnershipTransferred(address previousOwner, address newOwner)</summary>



</details>

#### Imported & Utils Contracts

```solidity
import "./MainContract.sol";
import "@openzeppelin/contracts/access/Ownable.sol";
import "@openzeppelin/contracts/utils/math/Math.sol";
import "@openzeppelin/contracts/utils/math/SafeMath.sol";
```
