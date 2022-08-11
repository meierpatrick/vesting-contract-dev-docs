---
description: >-
  The IBEP20 interface standard to create token contracts on Binance Smart
  Chain.
---

# Vesting Controller Contract

## About the Vesting Controller

![](../../.gitbook/assets/vestingController.gif)

Welcome to the Share V1 SDK. Here you can find everything related to our SDK. For deeper dives, we recommend referencing the [**SDK Github**](https://www.github.com) repo directly.

The latest version of the SDK is used in production in the Share Interface, but it is considered Alpha software and may contain bugs or change significantly between patch versions. If you have questions about how to use the SDK, please reach out. Pull requests welcome!

### The Characteristics

* Easy to use by other developers
* Adds a lot functionality and value to apps
* Does not negatively impact a mobile device’s CPU, battery, or data consumption
* Plays well with other SDKs



Functions:

* [`constructor(beneficiaryAddress, startTimestamp, durationSeconds)`](https://docs.openzeppelin.com/contracts/4.x/api/finance#VestingWallet-constructor-address-uint64-uint64-)
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

Events:

* [`EtherReleased(amount)`](https://docs.openzeppelin.com/contracts/4.x/api/finance#VestingWallet-EtherReleased-uint256-)
* [`ERC20Released(token, amount)`](https://docs.openzeppelin.com/contracts/4.x/api/finance#VestingWallet-ERC20Released-address-uint256-)

