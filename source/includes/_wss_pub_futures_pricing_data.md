### Channel: Futures Pricing Data

> Sample Futures Pricing Data Message

```json
{
    "m": "futures-pricing-data",
    "con": [  // all contracts
        {
            "s": "BTC-PERP",          // symbol
            "t": 1609371076960,       // data time
            "mp": "28142.586177036",  // mark price
            "ip": "28838.695",        // index price
            "r": "-0.005",            // funding rate 
            "f": 1609372800000        // next funding time
        }
    ],
    "col": [  // all collaterals
        {
            "a": "USDTR",   // asset
            "p": "1"        // reference price
        },
        {
            "a": "USDC",
            "p": "0.9996"
        },
        {
            "a": "ETH",
            "p": "749.82"
        },
        {
            "a": "PAX",
            "p": "1.0002"
        },
        {
            "a": "BTC",
            "p": "28834.165"
        },
        {
            "a": "USDT",
            "p": "1"
        }
    ]
}
```


**Subscribe to the Channel**

`{"op":"sub", "id":"sample-id", "ch":"futures-pricing-data"}`

