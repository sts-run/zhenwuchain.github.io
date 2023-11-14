## 提单


**接口地址**:`/gateway-api/spot/spotOrder/add`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>提单</p>



**请求示例**:


```javascript
{
  "memberId": 0,
  "type": "",
  "amount": 0,
  "symbol": "BTC-USDT",
  "direction": "",
  "price": 0,
  "useDiscount": ""
}
```


**请求参数**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|orderDto|提单|body|true|OrderDto|OrderDto|
|&emsp;&emsp;memberId|||false|integer(int64)||
|&emsp;&emsp;type|挂单类型,可用值:MARKET_PRICE,LIMIT_PRICE||true|string||
|&emsp;&emsp;amount|买入或卖出量||true|number||
|&emsp;&emsp;symbol|交易对符号  格式：BTC-USDT||true|string||
|&emsp;&emsp;direction|订单方向,可用值:BUY,SELL||true|string||
|&emsp;&emsp;price|挂单价格||true|number||
|&emsp;&emsp;useDiscount|||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|CommonResultString|


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|msg||string||
|data||string||


**响应示例**:
```javascript
{
	"code": 0,
	"msg": "",
	"data": ""
}
```
