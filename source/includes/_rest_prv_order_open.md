### List Open Orders

> Response

```json
{
    "code": 0,
    "data": [
        {
            "ac"          : "FUTURES",
            "accountId"   : "sample-futures-account-id",
            "seqNum"      : 14,
            "time"        : 1605677683714,
            "orderId"     : "a175d9d90643U68469127074abcd1234",
            "orderType"   : "Limit",
            "side"        : "Buy",
            "symbol"      : "BTC-PERP",
            "price"       : "9500",
            "orderQty"    : "0.1",
            "stopPrice"   : "0",
            "stopBy"      : "_NOT_IMPLEMENTED_",
            "status"      : "New",
            "lastExecTime": 1605677684479,
            "lastPx"      : "0",
            "lastQty"     : "0",
            "avgFilledPx" : "0",
            "cumFilledQty": "0",
            "fee"         : "0",
            "cumFee"      : "0",
            "feeAsset"    : "USDT",
            "errorCode"   : "",
        }
    ]
}
```

**HTTP Request**

`POST /<grp>/api/pro/v2/futures/order/open`

**Prehash String**

`v2/futures/order/open`


