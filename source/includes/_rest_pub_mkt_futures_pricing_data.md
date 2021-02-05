### Futures Pricing Data


> Requesting pricing data for all futures contract

```json
{
  "code": 0,
  "data": {
    "contracts": [
      {
        "time"           : 1609368616960,
        "symbol"         : "BTC-PERP",
        "markPrice"      : "28097.526022138",
        "indexPrice"     : "28768.535",
        "fundingRate"    : "-0.005",
        "nextFundingTime": 1609329600000
      }
    ],
    "collaterals": [
      {
        "asset"         : "USDTR",
        "referencePrice": "1"
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

