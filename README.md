---
description: >-
  This documentation will guide you through the process of creating a
  decentralized protocol that implements a post delivery private sale and
  secured vesting scheme.
---

# Overview

![](.gitbook/assets/home.gif)

### About this Documentation

This documentation shows how I use a set of helpful software-building tools to build a custom BEP20 token with a post delivery private sale, and a vesting controller that can handle scheduled vesting periods. Through this documentation, I'll explain things in more detail.

In the **Backend - Architecture** section, we start by going over each smart contract that is included with the protocol, as well as all the functions, modifiers, and events which are implemented.

In the **Frontend - Architecture** section, we start by going over how we can interact with the deployed smart contracts via ABI, call functions, and build a dapp using React.

### Recap of brief

> Sendable Receivable Interact with dapps // Pancakeswap metamask etc Lockable for Vesting Period Direct creation of max supply(no stacking, no mining e.g.) Lockable vesting Period explain: There will be a private sale. After the Private sale it should be possible for me to distribute the token thrue //send or smartcontract, but this token should be somehow or over a dapp or any idea what coming locked for a 1 year period. The 1 year locking period should be only for the private sale tokens. Maybe we could define a second wallet where the tokens when send from (not creating contract) the tokens will be locked for xy time amount.(Just a idea)
