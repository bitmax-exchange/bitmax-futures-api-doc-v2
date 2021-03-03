# General Info

## Futures Trading System Specification

### Contract Position Notional (CPN)

For the isolated group, CPN is the absolute value of `position size * mark price` of the contract.

For the cross group, CPN is the sum of absolute value of `position size * mark price` of all contracts in cross mode. 


### Position Initial/Maintenance Margin Rate

Initial/Maintenance Margin Rate is system-specified for each position brackets and each contract. You may refer to the `marginRequirements` 
section from the [Futures Contract Info](#futures-contracts-info) endpoint for position brackets.

You should compare [Contract Position Notional](#contract-position-notional) with each position bracket to determine your initial and 
maintenance margin rate.


### Position Initial/Maintenance Margin

Position Initial Margin = CPN * Initial Margin Rate

Position Maintenance Margin = CPN * Maintenance Margin Rate


### Liquidation Price

**For Long position**

V = Total Margin + Unrealized Pnl

Liquidation Price = mark price - (V - Maintenance Margin) / abs(position size * (1 - maintenance margin rate))

If the calculated liquidation price is negative, the position won't be liquidation even when the price becomes zero.


**For Short Position**

V = Total Margin + Unrealized Pnl 

Liquidation Price = mark price + (V - Maintenance Margin) / abs(position size * (1 - maintenance margin rate))