### Futures Pricing Data


> Requesting pricing data for all futures contract

```json
{
  "code": 0,
  "data": {
    "contracts": [
      {
        "time"           : 1609368616960,       // server time (UTC timestamp in milliseconds)
        "symbol"         : "BTC-PERP",          // contract symbol
        "markPrice"      : "28097.526022138",   // market price of the contract
        "indexPrice"     : "28768.535",         // price of the underlying index
        "fundingRate"    : "-0.005",            // funding rate
        "nextFundingTime": 1609372800000        // next funding time (UTC timestamp in milliseconds)
      }
    ],
    "collaterals": [
      {
        "asset"         : "USDTR",
        "referencePrice": "1"        // reference price (quote in USDT)
      },
      {
        "asset"         : "USDC",
        "referencePrice": "0.9996"
      },
      {
        "asset"         : "ETH",
        "referencePrice": "747.945"
      },
      {
        "asset"         : "PAX",
        "referencePrice": "0.9995"
      },
      {
        "asset"         : "BTC",
        "referencePrice": "28761.985"
      },
      {
        "asset"         : "USDT",
        "referencePrice": "1"
      }
    ]
  }
}
```

Get pricing data for all futures contracts. 

**HTTP Request**

`GET /api/pro/v2/futures/pricing-data`

