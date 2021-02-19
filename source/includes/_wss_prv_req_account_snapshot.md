### WS: Query Futures Account Asset Snapshot

> Requesting Futures Account Asset Snapshot

```json
{
   "op":"req",
   "id":"abc123456",
   "action":"futures-account-snapshot"
}
```

> Futures Account Asset Snapshot response

```json
{
   "m":"futures-account-snapshot",
   "id":"abc123456",
   "e":"ClientRequest",
   "t":1613748277356,
   "acc":"futH9N59hR0BMVEjHnBleHLn0mfUl5lo",
   "ac":"FUTURES",
   "sn":-1,
   "col":[
      {
         "a":"ETH",
         "b":"500",
         "f":"0.95"
      },
      {
         "a":"BTC",
         "b":"100",
         "f":"0.98"
      },
      {
         "a":"USDT",
         "b":"1000000",
         "f":"1"
      }
   ],
   "pos":[
      {
         "s":"BTC-PERP",
         "sd":"NULL_VAL",
         "pos":"0",
         "rc":"0",
         "up":"0",
         "rp":"0",
         "aop":"0",
         "boon":"0",
         "soon":"0",
         "mt":"crossed",
         "lev":"10",
         "iw":"0",
         "tp":"0",
         "tpt":"market",
         "sl":"0",
         "slt":"market"
      }
   ]
}
```

You can request the futures account asset snapshot via websocket by a `futures-account-snapshot` action. 

The request schema:

 Name          | Data Type           | Description                
-------------- | ------------------- | -------------------------- 
 `op`          | `String`            | `req`                      
 `action`      | `String`            | `futures-account-snapshot`  
 `id`          | `String`            | for result match purpose       



    
