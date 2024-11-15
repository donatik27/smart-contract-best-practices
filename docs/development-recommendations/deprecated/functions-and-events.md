!!! tip

    For comprehensive insights into secure development practices, consider visiting the [Development Recommendations](https://scsfg.io/developers/) section of the Smart Contract Security Field Guide. This resource provides in-depth articles to guide you in developing robust and secure smart contracts.

### Differentiate functions and events (Solidity \< 0.4.21)

Favor capitalization and a prefix in front of events (we suggest *Log*), to prevent the risk of
confusion between functions and events. For functions, always start with a lowercase letter, except
for the a constructor.

```solidity
// bad
event Transfer() {}
function transfer() {}

// good
event LogTransfer() {}
function transfer() external {}
```

!!! Note
    In [v0.4.21](https://github.com/ethereum/solidity/blob/develop/Changelog.md#0421-2018-03-07) Solidity
    introduced the `emit` keyword to indicate an event `emit EventName();`. As of 0.5.0, it is
    required.
