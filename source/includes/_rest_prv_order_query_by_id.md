### Query Order By ID

> Query Orders By IDs - Request Body

```json
{
   "orderId":"a177c29e4064U0123456789dVeUxlVyA,a177c29e4064U0123456789dVeUxlVyB"
}
```

> Query Order with multiple order ids - Successful Response (Status 200, code 0)

```json
{
    "code"     : 0,
    "accountId": "sampleFuturesAccountId",
    "ac"       : "FUTURES",
    "data": [
        {
            "ac"                  : "FUTURES",
            "accountId"           : "sampleFuturesAccountId",
            "avgFilledPx"         : "0",
            "cumFee"              : "0",
            "cumFilledQty"        : "0",
            "errorCode"           : "",
            "execInst"            : "NULL_VAL",
            "fee"                 : "0",
            "feeAsset"            : "USDT",
            "lastExecTime"        : 1613877923408,
            "lastPx"              : "0",
            "lastQty"             : "0",
            "orderId"             : "a177c29e4064U0123456789dVeUxlVyA",
            "orderQty"            : "0.1",
            "orderType"           : "Limit",
            "posStopLossPrice"    : "0",
            "posStopLossTrigger"  : "None",
            "posTakeProfitPrice"  : "0",
            "posTakeProfitTrigger": "None",
            "price"               : "34000",
            "seqNum"              : 18586710,
            "side"                : "Buy",
            "status"              : "New",
            "stopBy"              : "",
            "stopPrice"           : "0",
            "symbol"              : "BTC-PERP",
            "time"                : 1613877922641
        },
{
            "ac"                  : "FUTURES",
            "accountId"           : "sampleFuturesAccountId",
            "orderId"             : "a177c29e4064U0123456789dVeUxlVyB",
            ...
        }
    ]
}
```

**HTTP Request**

`GET /<grp>/api/pro/v2/futures/order/status`

**Prehash String**

`<timestamp>+v2/futures/order/status`

**Request Parameters**

PARAMETER | TYPE      | REQUIRED | DESCRIPTION
--------- |---------- | -------- | ---------------
orderId   | String    | Yes      | a single order id, or multiple order ids separated by *,*

The API will respond with a list of objects in the data field. Each object in the list contains information of a single order.

