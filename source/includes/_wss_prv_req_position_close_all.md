### WS: Close All Position

> Request to close all position 

```json
{
   "op":"req",
   "action":"close-all-position",
   "ac":"futures",
   "id":"sampleRequestId",
   "args":{
      "cancelOpen":true
   }
}
```

> Request to close all position related to symbol "BTC-PERP"

```json
{
   "op":"req",
   "action":"close-all-position",
   "ac":"futures",
   "id":"sampleRequestId",
   "args":{
      "symbol":"BTC-PERP",
      "cancelOpen":true
   }
}
```

> Successful ACK message

```json
{
   "m":"position",
   "id":"sampleRequestId",
   "action":"close-all-position",
   "ac":"FUTURES",
   "code":0,
   "info":{
      "cancelOpen":true
   }
}
```

> Error response message

```json
{
   "m":"order",
   "id":"sampleRequestId",
   "action":"close-all-position",
   "ac":"FUTURES",
   "code":100006,
   "info":{
      "symbol":"",
      "reason":"INVALID_ARGUMENT",
      "errorMsg":"Required argument missing or type-mismatched (expecting boolean): cancelOpen"
   }
}
```

Close all position on account level via websocket with optional symbol and open order cancellation flag.

**Request**

Make general websocket request with `action` field as `close-all-position` and set proper `ac` value(`futures`), and provide *symbol* 
and *cancelOpen* value in *args* optionally.

**Response**

With *code* field as *zero* to indicate this close all position request has been received by server and sent to matching engine. 

*info* field provide some detail: if you provide *symbol* and *cancelOpen* in your request to close position.

With *code* field as *non-zero* to indicate there are some errors in your request. 

*info* field provide some detail: we also provide error *reason* and *errorMsg* detail.
