### Futures Contracts Info

> Response - Futures Contracts Info

```json
{
    "code": 0,
    "data": [
        {
            "symbol"          : "BTC-PERP",
            "status"          : "Normal",
            "displayName"     : "BTCUSDT",      // the name displayed on the webpage
            "baseAsset"       : "BTCP",
            "quoteAsset"      : "USDT",
            "underlying"      : "BTC/USDT",
            "tradingStartTime": 1579701600000,
            "collapseDecimals": "1,0.1,0.01",
            "priceFilter": {
                "minPrice"  : "0.25",
                "maxPrice"  : "1000000",
                "tickSize"  : "0.25",
                "priceScale": 2
            },
            "lotSizeFilter": {
                "minQty"  : "0.0001",
                "maxQty"  : "1000000000",
                "lotSize" : "0.0001",
                "qtyScale": 4
            },
            "marginRequirements": [
                {
                    "positionLB"           : "0",     // position lower bound
                    "positionUB"           : "50000", // position upper bound
                    "initialMarginRate"    : "0.01",  // initial margin rate
                    "maintenanceMarginRate": "0.006"  // maintenance margin rate
                },
                {
                    "positionLB"           : "50000",
                    "positionUB"           : "200000",
                    "initialMarginRate"    : "0.02",
                    "maintenanceMarginRate": "0.012"
                }
            ]
        }
    ]
}
```

Get information for all futures contracts.

**HTTP Request**

`GET /api/pro/v2/futures/contract`

**Response**




### Futures Collateral Asset Info

> Response - Futures Collateral Asset Info

```json
{
    "code": 0,
    "data": [
        {
            "asset"           : "BTC",
            "assetName"       : "Bitcoin",
            "conversionFactor": "0.995",
            "discountFactor"  : "0.98",
            "displayName"     : "BTC",
            "statusCode"      : "Normal"
        },
        {
            "asset"           : "USDT",
            "assetName"       : "Tether",
            "conversionFactor": "1",
            "discountFactor"  : "1",
            "displayName"     : "USDT",
            "statusCode"      : "Normal"
        },
        {
            "asset"           : "USDTR",
            "assetName"       : "Futures Reward Token",
            "conversionFactor": "1",
            "discountFactor"  : "1",
            "displayName"     : "USDTR",
            "statusCode"      : "NoTransaction"
        }
    ]
}
```

Get information for all futures collateral assets.

**HTTP Request**

`GET /api/pro/v2/futures/collateral`
