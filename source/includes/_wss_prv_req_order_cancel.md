### WS: Cancel Order

> Request to cancel existing open order

```json
{
   "op":"req",
   "action":"cancel-order",
   "account":"futures",
   "ac":"futures",
   "args":{
      "time":1613744943323,
      "orderId":"s177bab1b474U5051470287bbtcpKiOR",
      "symbol":"BTC-PERP"
   }
}
```

> Successful ACK message

```json
{
   "ac":"FUTURES",
   "accountId":"futH9N59hR0BMVEjHnBleHLn0mfUl5lo",
   "time":1613744944323,
   "orderId":"s177bab1b474U5051470287bbtcpKiOR",
   "seqNum":552,
   "orderType":"Limit",
   "execInst":"NULL_VAL",
   "side":"Buy",
   "symbol":"BTC-PERP",
   "price":"32400",
   "orderQty":"0.12",
   "stopPrice":"0",
   "stopBy":"",
   "status":"New",
   "lastExecTime":1613744944330,
   "lastQty":"0",
   "lastPx":"0",
   "avgFilledPx":"0",
   "cumFilledQty":"0",
   "fee":"0",
   "cumFee":"0",
   "feeAsset":"USDT",
   "errorCode":"",
   "posStopLossPrice":"0",
   "posStopLossTrigger":"market",
   "posTakeProfitPrice":"0",
   "posTakeProfitTrigger":"market"
}
```

> Error response message

```json
{
  "accountId": "futH9N59hR0BMVEjHnBleHLn0mfUl5lo",
  "ac": "FUTURES",
  "action": "cancel-order",
  "status": "Ack",
  "info": {
    "code":     300006,
    "id":      "x@fabs",
    "message": "Invalid Client Order Id: x@fabs",
    "symbol":  "BTC-PERP",
    "reason":  "INVALID_ORDER_ID"
  }
}
```

Cancel an existing open order via websocket 

**Request**

Make order cancelling request follow the general websocket request rule by setting `action` to be `cancel-orde`, with proper cancel order parameters as specified in rest api for *args* field.

**Response**

*ACK* 

With *status* field as *Ack* to indicate this cancel order request pass some basic sanity check, and has been sent to matching engine. 

*info* field provide some detail: if you provide *id* in your request, it will be echoed back as *id* to help you idintify; we also echo back target *orderId* to be cancelled.  

*Err*

With *status* field as *Err* to indicate there is some obvisous errors in your cancel order request. 

*info* field provide some detail: if you provide *id* in your request, it will be echoed back as *id* to help you identify; we also provide error *code*, *reason*, and *message* detail.
