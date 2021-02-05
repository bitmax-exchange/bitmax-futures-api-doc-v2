### Change Margin (for Isolated Positions)

> Successful Response

```json
{
    "code": 0
}
```

You can only change margin for isolated margin positions.

See [Free Margin](#free-margin) on the maximum amount you can increase / decrease the isolated margin.

**HTTP Request**

<!-- 
@binance POST /fapi/v1/positionMargin
@bybit   POST /position/change-position-margin
@OKEx    POST ?
-->

`POST /<grp>/api/pro/v2/futures/isolated-position-margin`

**Prehash String**

`v2/futures/isolated-position-margin`


**Request Parameters**

PARAMETER  | TYPE   | REQUIRED | DESCRIPTION
---------- |--------| -------- | ---------------
symbol     | String |  Yes     | e.g. `BTC-PERP`
amount     | String |  Yes     | margin amount in string type, e.g. "100". Set `amount` to positive will increase the isolated margin; set `amount` 
to a negative number will decrease the isolated margin. 
