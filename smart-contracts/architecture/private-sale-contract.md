---
description: >-
  The IBEP20 interface standard to create token contracts on Binance Smart
  Chain.
---

# Private Sale Contract

## About the Private Sale

![](../../.gitbook/assets/privateSale.gif)

The following standard defines the implementation of APIs for token smart contracts. It is proposed by deriving the ERC20 protocol of Ethereum and provides the basic functionality to transfer tokens, allow tokens to be approved so they can be spent by another on-chain third party, and transfer between Binance Chain and Binance Smart Chain.

### The Characteristics

* [x] Lives on the Binance Smart Chain
* [x] Adds a lot functionality and value to apps
* [x] Does not negatively impact a mobile device’s CPU, battery, or data consumption
* [x] Plays well with other SDKs

### Core: PrivateSale (PrivateSale.sol)

**Functions:**

* [fallback()](private-sale-contract.md#fallback)
* [token()](private-sale-contract.md#undefined)
* [wallet()](private-sale-contract.md#undefined-1)
* [rate()](private-sale-contract.md#undefined-2)
* [weiRaised()](private-sale-contract.md#undefined-3)
* [buyTokens()](private-sale-contract.md#undefined)
* [preValidatePurchase()](private-sale-contract.md#undefined-1)
* [postValidatePurchase()](private-sale-contract.md#undefined-2)
* [deliverTokens()](private-sale-contract.md#undefined)
* [proccessPurchase()](private-sale-contract.md#undefined-1)
* [updatePurchasingState()](private-sale-contract.md#undefined-2)
* [getTokenAmount()](private-sale-contract.md#undefined-3)
* [forwardFunds()](private-sale-contract.md#undefined)

**Events:**

* [TokensPurchased()](private-sale-contract.md#undefined)

<details>

<summary>fallback()</summary>

fallback function **DO NOT OVERRIDE** Note that other contracts will transfer funds with a base gas stipend of 2300, which is not enough to call buyTokens. Consider calling buyTokens directly when purchasing tokens from a contract.

</details>

<details>

<summary>token() → contract IBEP20</summary>



</details>

<details>

<summary>wallet() → address payable</summary>



</details>

<details>

<summary>rate() → uint256</summary>



</details>

<details>

<summary>weiRaised() → uint256</summary>



</details>

<details>

<summary>buyTokens(address beneficiary)</summary>

low level token purchase **DO NOT OVERRIDE** This function has a non-reentrancy guard, so it shouldn’t be called by another `nonReentrant` function.

</details>

<details>

<summary>preValidatePurchase(address beneficiary, uint256 weiAmount)</summary>

Validation of an incoming purchase. Use require statements to revert state when conditions are not met. Use `super` in contracts that inherit from Crowdsale to extend their validations. Example from CappedCrowdsale.sol’s \_preValidatePurchase method: super.\_preValidatePurchase(beneficiary, weiAmount); require(weiRaised().add(weiAmount) ⇐ cap);

</details>

<details>

<summary>postValidatePurchase(address beneficiary, uint256 weiAmount)</summary>

Validation of an executed purchase. Observe state and use revert statements to undo rollback when valid conditions are not met.

</details>

<details>

<summary>deliverTokens(address beneficiary, uint256 tokenAmount)</summary>

Source of tokens. Override this method to modify the way in which the crowdsale ultimately gets and sends its tokens.

</details>

<details>

<summary>processPurchase(address beneficiary, uint256 tokenAmount)</summary>

Executed when a purchase has been validated and is ready to be executed. Doesn’t necessarily emit/send tokens.

</details>

<details>

<summary>updatePurchasingState(address beneficiary, uint256 weiAmount)</summary>

Override for extensions that require an internal state to check for validity (current user contributions, etc.)

</details>

<details>

<summary>getTokenAmount(uint256 weiAmount) → uint256</summary>

Override to extend the way in which ether is converted to tokens.

</details>

<details>

<summary>forwardFunds()</summary>

Determines how ETH is stored/forwarded on purchases.

</details>

<details>

<summary>TokensPurchased(address purchaser, address beneficiary, uint256 value, uint256 amount)</summary>



</details>

### Validation: TimedPrivateSale (TimedPrivateSale.sol)

**Functions:**

* [openingTime()](private-sale-contract.md#undefined)
* [closingTime()](private-sale-contract.md#undefined-1)
* [isOpen()](private-sale-contract.md#undefined-2)
* [hasClosed()](private-sale-contract.md#undefined-3)
* [preValidatePurchase()](private-sale-contract.md#undefined-4)

**Events:**

* [TimedPrivateSaleExtended(prevClosingTime, newClosingTime)](private-sale-contract.md#undefined)

<details>

<summary>openingTime () → uint256</summary>

The private sale opening time.

</details>

<details>

<summary>closingTime () → uint256</summary>

The private sale ending time (1 year).

</details>

<details>

<summary>isOpen () → bool</summary>

`true` if the private sale is open, `false` otherwise.

</details>

<details>

<summary>hasClosed () → bool</summary>

Whether private sale period has elapsed

</details>

<details>

<summary>preValidatePurchase ()</summary>

Extend parent behavior requiring to be within the contributing period

</details>

<details>

<summary>TimedPrivateSaleExtended(uint256 prevClosingTime, uint256 newClosingTime)</summary>



</details>

### Distribution: PostDelivery (PostDelivery.sol)
