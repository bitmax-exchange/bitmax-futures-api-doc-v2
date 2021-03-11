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
    "ac": "FUTURES",
    "accountId": "sample-futures-account-id",
    "action": "close-all-position",
    "code": 0,
    "info": {
        "cancelOpen": true,
        "symbol": ""
    }
}
```

> Error Response

```json
{
    "ac": "FUTURES",
    "accountId": "sample-futures-account-id",
    "action": "close-all-position",
    "code": 300012,
    "info": {
        "cancelOpen": true,
        "symbol": "ABC-PERP"
    },
    "message": "Invalid Product Symbol",
    "reason": "INVALID_PRODUCT"
}
```

