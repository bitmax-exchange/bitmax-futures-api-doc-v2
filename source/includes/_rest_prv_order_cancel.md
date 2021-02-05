### Cancel Order 

> Response

```json
{
    "code": 0,
    "data": {
        "meta": {
            "action"  : "cancel-order",
            "id"      : "abcd1234abcd1234",
            "respInst": "ACCEPT"
        },
        "order": {
            "ac"          : "FUTURES",
            "accountId"   : "fut-yue-zhao-bitmax",
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
            "status"      : "Canceled",
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
    }
}
```

**HTTP Request**

<!-- 
@binance POST 
@bybit   POST 
@OKEx    POST 
-->

`POST /<grp>/api/pro/v2/futures/order`

**Prehash String**

`v2/futures/order`

**Request Parameters**

PARAMETER                           | TYPE   | REQUIRED | DESCRIPTION
----------------------------------- |--------| -------- | ------------------------------------------------------ 
id                                  | String |          | >=9 chars (letter and digit number only). Optional but recommended. We echo it back to help you match response with request. This is especially useful when you cancel in batch mode.
orderId                             | String |   Yes    | 32 chars order id. You should set the value to be the orderId of the target order you want to cancel.
symbol                              | String |   Yes    | Symbol of the order to cancel
time                                | Long   |   Yes    | milliseconds since UNIX epoch in UTC. We do not process request sent more than 30 seconds ago.
[respInst](#response-type-respinst) | ENUM   |          | `ACK` by default

**Response**



*respInst*

