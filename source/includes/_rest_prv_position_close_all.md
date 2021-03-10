### Close All Position

To close position of all or specific symbol with option of cancel open orders

**HTTP Request**

`DELETE /<grp>/api/pro/v2/futures/position/all`

**Request Parameters**

PARAMETER | TYPE    | REQUIRED | DESCRIPTION
--------- |-------- | -------- | ------------------------------------------------------ 
symbol    | String  |   No     | Specify the symbol to close position, default ALL symbols
cancelOpen| Boolean |   No     | To cancel all open orders, default *True*


**Prehash String**

`<timestamp>+v2/futures/position/all`

> Successful Response

```json
{
   "ac":"FUTURES",
   "accountId":"sample-futures-account-id",
   "action":"close-all-position",
   "status":"ACK",
   "info":{
      "symbol": "BTC-PERP",
      "cancelOpen":true
   }
}
```
