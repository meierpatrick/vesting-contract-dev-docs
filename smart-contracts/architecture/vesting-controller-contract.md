---
description: >-
  The IBEP20 interface standard to create token contracts on Binance Smart
  Chain.
---

# Vesting Controller Contract

![](../../.gitbook/assets/vestingController.gif)

### About the Vesting Controller Contract

We have followed general OpenZeppelin guidelines: functions revert instead of returning `false` on failure. This behavior is nonetheless conventional and does not conflict with the expectations of ERC20 applications.

Additionally, an [`Approval`](https://docs.openzeppelin.com/contracts/2.x/api/token/erc20#IERC20-Approval-address-address-uint256-) event is emitted on calls to [`transferFrom`](https://docs.openzeppelin.com/contracts/2.x/api/token/erc20#ERC20-transferFrom-address-address-uint256-). This allows applications to reconstruct the allowance for all accounts just by listening to said events. Other implementations of the EIP may not emit these events, as it isn’t required by the specification.

Finally, the non-standard [`decreaseAllowance`](https://docs.openzeppelin.com/contracts/2.x/api/token/erc20#ERC20-decreaseAllowance-address-uint256-) and [`increaseAllowance`](https://docs.openzeppelin.com/contracts/2.x/api/token/erc20#ERC20-increaseAllowance-address-uint256-) functions have been added to mitigate the well-known issues around setting allowances. See [`IERC20.approve`](https://docs.openzeppelin.com/contracts/2.x/api/token/erc20#IERC20-approve-address-uint256-).

### The Characteristics

* [x] Easy to use by other developers
* [x] Adds a lot functionality and value to apps
* [x] Does not negatively impact a mobile device’s CPU, battery, or data consumption
* [x] Plays well with other SDKs

{% hint style="info" %}
I have followed general OpenZepellin guidelines to build the contracts.
{% endhint %}

<mark style="color:blue;">**Modifiers:**</mark>

* onlyOwner()

<mark style="color:blue;">**Functions:**</mark>

* <mark style="color:blue;">****</mark>[`constructor(beneficiaryAddress, startTimestamp, durationSeconds)`](https://docs.openzeppelin.com/contracts/4.x/api/finance#VestingWallet-constructor-address-uint64-uint64-)
* [`receive()`](https://docs.openzeppelin.com/contracts/4.x/api/finance#VestingWallet-receive--)
* [`beneficiary()`](https://docs.openzeppelin.com/contracts/4.x/api/finance#VestingWallet-beneficiary--)
* [`start()`](https://docs.openzeppelin.com/contracts/4.x/api/finance#VestingWallet-start--)
* [`duration()`](https://docs.openzeppelin.com/contracts/4.x/api/finance#VestingWallet-duration--)
* [`released()`](https://docs.openzeppelin.com/contracts/4.x/api/finance#VestingWallet-released--)
* [`released(token)`](https://docs.openzeppelin.com/contracts/4.x/api/finance#VestingWallet-released-address-)
* [`release()`](https://docs.openzeppelin.com/contracts/4.x/api/finance#VestingWallet-release--)
* [`release(token)`](https://docs.openzeppelin.com/contracts/4.x/api/finance#VestingWallet-release-address-)
* [`vestedAmount(timestamp)`](https://docs.openzeppelin.com/contracts/4.x/api/finance#VestingWallet-vestedAmount-uint64-)
* [`vestedAmount(token, timestamp)`](https://docs.openzeppelin.com/contracts/4.x/api/finance#VestingWallet-vestedAmount-address-uint64-)
* [`_vestingSchedule(totalAllocation, timestamp)`](https://docs.openzeppelin.com/contracts/4.x/api/finance#VestingWallet-\_vestingSchedule-uint256-uint64-)

<mark style="color:blue;">**Events:**</mark>

* <mark style="color:blue;">****</mark>[`EtherReleased(amount)`](https://docs.openzeppelin.com/contracts/4.x/api/finance#VestingWallet-EtherReleased-uint256-)
* [`ERC20Released(token, amount)`](https://docs.openzeppelin.com/contracts/4.x/api/finance#VestingWallet-ERC20Released-address-uint256-)

