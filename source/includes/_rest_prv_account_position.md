### Position

> Response

```json
{
    "code": 0,
    "data": {
        "accountCategory": "FUTURES",
        "accountId"      : "fut-yue-zhao-bitmax",
        "collaterals": [
            {
                "asset"         : "ETH",
                "balance"       : "100",
                "discountFactor": "0.95",
                "referencePrice": "481.79793092"
            },
            {
                "asset"         : "BTC",
                "balance"       : "10",
                "discountFactor": "0.98",
                "referencePrice": "17600.095"
            },
            {
                "asset"         : "USDT",
                "balance"       : "10000",
                "discountFactor": "1",
                "referencePrice": "1"
            }
        ],
        "contracts": [
            {
                "symbol"               : "BTC-PERP",
                "position"             : "0.5",
                "avgOpenPrice"         : "0",
                "indexPrice"           : "17600.095",
                "isolatedMargin"       : "0",
                "leverage"             : "10",
                "marginType"           : "CrossMargin",
                "markPrice"            : "-1",
                "realizedPnl"          : "0",
                "side"                 : "LONG",
                "stopLossPrice"        : "-1",
                "stopLossTrigger"      : "refpx",
                "takeProfitPrice"      : "-1",
                "takeProfitTrigger"    : "ref-px",
                "unrealizedPnl"        : "0",
                "buyOpenOrderNotional" : "1362.419625",
                "sellOpenOrderNotional": "0"
            }
        ]
    }
}
```

Get current position data - a full snapshot of your futures account. 

**HTTP Request**

<!-- 
@binance GET /fapi/v2/balance
@bybit   GET /v2/private/position/list
@OKEx    GET /api/futures/v3/position
-->

`GET /<grp>/api/pro/v2/futures/position`

**Prehash String**

`v2/futures/position`


