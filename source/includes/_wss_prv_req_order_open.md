### WS: Query Open Orders on Symbol

> Requesting open orders on symbol BTC-PERP

```json
{
   "op"    : "req",
   "id"    : "abc123456",
   "action": "futures-open-orders",
   "args":{
      "symbol":"BTC-PERP"
   }
}
```

> Open orders response

```json
[
   {
      "m"      : "futures-order",
      "sn"     : 553,
      "e"      : "ExecutionReport",
      "a"      : "futH9N59hR0BMVEjHnBleHLn0mfUl5lo",
      "ac"     : "FUTURES",
      "t"      : 1613745075540,
      "ct"     : 1613745075533,
      "orderId": "s177bab3b501U5051470287bc0d18f6c",
      "sd"     : "Buy",
      "ot"     : "Limit",
      "ei"     : "NULL_VAL",
      "q"      : "0.12",
      "p"      : "32400",
      "sp"     : "0",
      "spb"    : "",
      "s"      : "BTC-PERP",
      "st"     : "New",
      "err"    : "",
      "lp"     : "0",
      "lq"     : "0",
      "ap"     : "0",
      "cfq"    : "0",
      "f"      : "0",
      "cf"     : "0",
      "fa"     : "USDT",
      "psl"    : "0",
      "pslt"   : "market",
      "ptp"    : "0",
      "ptpt"   : "market"
   }
]
```

You can request the open order via websocket by a `futures-open-orders` action. 

The request schema:

 Name          | Data Type           | Description                
-------------- | ------------------- | -------------------------- 
 op            | String              | `req`                      
 action        | String              | `futures-open-orders`  
 id            | String              | for result match purpose       
 args:symbols  | Optional[String]    | add the (optional) symbol filter, see below for details.

The `symbols` key in the `args` map allows you to customize the symbol filter in a flexible way:

* to query open orders of the **a specific symbol**, set `symbols` to a valid symbol code. For instance, `{"symbols": "BTC-PERP"}`
* to query open orders of **multiple symbols**, set `symbols` to comma separated string of valid symbol codes. For instance, `{"symbols": "BTC-PERP,ETH-PERP"}` allows you to query open orders of both `BTC-PERP` and `ETH-PERP` at the same time.
* to query **all open orders**, you may either use the wild card (`{"symbols": "*"}`) or simply omit the `symbols` key (`{}`). 

   
