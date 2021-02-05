### Channel: Account Update

```json
{
    "m"     : "futures-account-update",
    "e"     : "ExecutionReport",
    "t"     : 1606083071535,
    "acc"   : "fut-yue-zhao-bitmax",
    "at"    : "FUTURES",
    "execId": 82,
    "col": [
        {
            "a": "ETH",
            "b": "100",
            "f": "0.95"
        },
        {
            "a": "BTC",
            "b": "10",
            "f": "0.98"
        },
        {
            "a": "USDT",
            "b": "10000",
            "f": "1"
        }
    ],
    "pos": [
        {
            "s"  : "BTCP",
            "sd" : "NULL_VAL",
            "pos": "0",
            "up" : "0",
            "rp" : "0",
            "aop": "0",
            "mt" : "IsolatedMargin",
            "lev": "10",
            "iw" : "0",
            "tp" : "0",
            "tpt": "ref-px",
            "sl" : "0",
            "slt": "ref-px"
        }
    ]
}
```


**Subscribe to the Channel**

`{"op":"sub", "id":"sample-id", "ch":"futures-account-update"}`
