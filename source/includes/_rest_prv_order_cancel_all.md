### Cancel All Open Orders

**HTTP Request**

`DELETE /<grp>/api/pro/v2/futures/order/all`

**Prehash String**

`<timestamp>+v2/futures/order/all`

**Request Parameters**

PARAMETER | TYPE   | REQUIRED | DESCRIPTION
--------- |--------| -------- | ------------------------------------------------------ 
symbol    | String |   No     | the optional symbol filter


> Successful Response

```json
{
    "ac": "FUTURES",
    "accountId": "sample-futures-account-id",
    "action": "cancel-all",
    "code": 0,
    "info": {
        "symbol": ""
    }
}
```
> Error Response

```json
{
    "ac": "FUTURES",
    "accountId": "sample-futures-account-id",
    "action": "cancel-all",
    "code": 300012,
    "info": {
        "symbol": "ABC-PERP"
    },
    "message": "Invalid Product Symbol",
    "reason": "INVALID_PRODUCT"
}
```
