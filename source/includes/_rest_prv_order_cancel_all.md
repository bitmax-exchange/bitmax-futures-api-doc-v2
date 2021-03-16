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
    "code": 0,
    "data": {
        "ac": "FUTURES",
        "accountId": "sample-futures-account-id",
        "action": "cancel-all",
        "info": {
            "symbol": "BTC-PERP"
                }
            }
}
```
> Error Response

```json
{
    "code": 300012,
    "message": "Invalid Product Symbol",
    "reason": "INVALID_PRODUCT",
    "data": {
        "ac": "FUTURES",
        "accountId": "sample-futures-account-id",
        "action": "cancel-all",
        "info": {
            "symbol": "ABC-PERP"
                }
        }
}
```
