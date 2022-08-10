# Post Delivery Private Sale

The following standard defines the implementation of APIs for token smart contracts. It is proposed by deriving the ERC20 protocol of Ethereum and provides the basic functionality to transfer tokens, allow tokens to be approved so they can be spent by another on-chain third party, and transfer between Binance Chain and Binance Smart Chain.

### The Characteristics

* Lives on the Binance Smart Chain
* Adds a lot functionality and value to apps
* Does not negatively impact a mobile device’s CPU, battery, or data consumption
* Plays well with other SDKs



### PrivateSale (PrivateSale.sol)

**Functions:**

* `token()`
* `wallet()`
* `rate()`
* `weiRaised()`
* `buyTokens()`
* `preValidatePurchase()`
* `postValidatePurchase()`
* `deliverTokens()`
* `proccessPurchase()`
* `updatePurchasingState()`
* `getTokenAmount()`
* `forwardFunds()`

**Events:**

* `TokensPurchased()`

### TimedPrivateSale (TimedPrivateSale.sol)

**Functions:**

* `openingTime()`
* `closingTime()`
* `isOpen()`
* `hasClosed()`
* `preValidatePurchase()`

**Events:**

* `Transfer()`
* `Approval()`
