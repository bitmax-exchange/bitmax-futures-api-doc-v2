### WS: Place Order 

> Request to place new order

```json
{
   "op":"req",
   "action":"place-order",
   "account":"FUTURES",
   "ac":"futures",
   "args":{
      "time":1613742809699,
      "id":"11eb9a8355fc41bd9bf5b08bc0d18f6c",
      "symbol":"BTC-PERP",
      "orderPrice":"32500",
      "orderQty":"0.12",
      "orderType":"limit",
      "side":"buy",
      "postOnly":false,
      "respInst":"ACK"
   }
}
```

> Successful ACK message

```json
{
   "ac":"FUTURES",
   "accountId":"futH9N59hR0BMVEjHnBleHLn0mfUl5lo",
   "time":1613742809754,
   "orderId":"s177ba912263U5051470287bc0d18f6c",
   "seqNum":-1,
   "orderType":"Limit",
   "execInst":"NULL_VAL",
   "side":"Buy",
   "symbol":"BTC-PERP",
   "price":"32500",
   "orderQty":"0.12",
   "stopPrice":"0",
   "stopBy":"ref-px",
   "status":"Ack",
   "lastExecTime":1613742809754,
   "lastQty":"0",
   "lastPx":"0",
   "avgFilledPx":"0",
   "cumFilledQty":"0",
   "fee":"0",
   "cumFee":"0",
   "feeAsset":"",
   "errorCode":"",
   "posStopLossPrice":"0",
   "posStopLossTrigger":"market",
   "posTakeProfitPrice":"0",
   "posTakeProfitTrigger":"market"
}
```

Place order via websocket 

**Request**

Make new order request follow the general websocket request rule, with proper place new order parameters as specified in rest api for *args* field.

see [placing order via RESTful API](#new-order).

**Response**

Respond with *m* field as *order*, and *action* field as *place-order*; *status* field to indicate if this is a successful *Ack* or failed *Err*.

*ACK* 

With *status* field as *Ack* to indicate this new order request pass some basic sanity check, and has been sent to matching engine. 

*info* field provide some detail: if you provide *id* in your request, it will be echoed back as *id* to help you identify; we also provide server side generated *orderId*, which is the id you should use for future track or action on the order.  


*ERR* 

With *status* field as *Err* to indicate there is some obvisous errors in your order. 

*info* field provide some detail: if you provide *id* in your request, it will be echoed back as *id* to help you identify; we also provide error *code*, *reason*, and *message* detail.
