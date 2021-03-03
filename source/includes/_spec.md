# General Info


## Futures Trading System Specification


### Contract Position Notional (CPN)

For the isolated group:

* CPN = abs(position size * mark price) for the contract in the isolated group

For the cross group: 

* CPN = sum of abs(position size * mark price) for all contracts in the cross group



### Total Margin

**For the isolated group**

Total margin is set by the user. You can find its value in the `isolatedMargin` field from the [Position](#position) endpoint. 

You can increase / decrease the total margin of the isolated margin group via the [Change Margin](#change-margin-for-isolated-positions) endpoint.


**For the cross group**

* Total Margin = sum(Asset Balance * Reference Price * Collateral Discount Factor) for each collateral asset

Discount factor can be found in the `discountFactor` field from the [Futures Collateral Asset Info](#futures-collateral-asset-info) endpoint.



### Position Initial/Maintenance Margin Rate

Initial/Maintenance Margin Rate is system-specified for each position brackets and each contract. You may refer to the `marginRequirements` 
section from the [Futures Contract Info](#futures-contracts-info) endpoint for position brackets.

You should compare [Contract Position Notional (CPN)](#contract-position-notional-cpn) with each position bracket to determine your initial and 
maintenance margin rate.



### Position Initial/Maintenance Margin

* Position Initial Margin = CPN * Initial Margin Rate
* Position Maintenance Margin = CPN * Maintenance Margin Rate



### Liquidation Price

* V = Total Margin + Unrealized Pnl - Maintenance Margin
* R = abs(position size) * (1 - maintenance margin rate)

**For Long position**

* Liquidation Price = mark price - V / R

If the calculated liquidation price is negative, the position won't be liquidation even when the price becomes zero.

**For Short Position**

* Liquidation Price = mark price + V / R
