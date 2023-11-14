
# Open-API


## Order


**接口地址**:`/spot/open-api/v1/exchange/order`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "type": "",
  "amount": 0,
  "symbol": "BTC-USDT",
  "direction": "",
  "price": 0,
  "useDiscount": 0
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|orderRequestDTO|Order request param|body|true|OrderRequestDTO|OrderRequestDTO|
|&emsp;&emsp;type|Order type,可用值:MARKET_PRICE,LIMIT_PRICE||true|string||
|&emsp;&emsp;amount|Buy or sell amount||true|number||
|&emsp;&emsp;symbol|symbol. format：BTC-USDT||true|string||
|&emsp;&emsp;direction|Order direction,可用值:BUY,SELL||true|string||
|&emsp;&emsp;price|price||true|number||
|&emsp;&emsp;useDiscount|Whether to use the discount,0:don't use; 1:use||true|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|CommonResultBigDecimal|


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|msg||string||
|data||number||


**响应示例**:
```javascript
{
	"code": 0,
	"msg": "",
	"data": 0
}
```


## Wallet Account


**接口地址**:`/spot/open-api/v1/wallets`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|CommonResultBigDecimal|


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|msg||string||
|data||number||


**响应示例**:
```javascript
{
	"code": 0,
	"msg": "",
	"data": 0
}
```


## Get the symbol latest prices


**接口地址**:`/spot/open-api/v1/last-price/{symbol}`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|symbol|symbol. format：BTC-USDT|path|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|CommonResultBigDecimal|


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|msg||string||
|data||number||


**响应示例**:
```javascript
{
	"code": 0,
	"msg": "",
	"data": 0
}
```


## Get real-time K-line data


**接口地址**:`/spot/open-api/v1/k-line/{symbol}/{interval}`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|symbol|symbol. format：BTC-USDT|path|true|string||
|interval|K-line interval, available: M1,M5,M15,M30,H1,H4,D1,W1,MON1|path|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|CommonResultObject|


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|msg||string||
|data||object||


**响应示例**:
```javascript
{
	"code": 0,
	"msg": "",
	"data": {}
}
```


## Recent Trades


**接口地址**:`/spot/open-api/v1/exchange/{symbol}/recent-trades`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|symbol|symbol. format：BTC-USDT|path|true|string||
|count|Number of result records|query|true|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|CommonResultBigDecimal|


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|msg||string||
|data||number||


**响应示例**:
```javascript
{
	"code": 0,
	"msg": "",
	"data": 0
}
```


## Realtime Partial Book Depth


**接口地址**:`/spot/open-api/v1/exchange/{symbol}/partial`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|symbol|symbol. format：BTC-USDT|path|true|string||
|depth|Count of depth|query|true|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|CommonResultBigDecimal|


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|msg||string||
|data||number||


**响应示例**:
```javascript
{
	"code": 0,
	"msg": "",
	"data": 0
}
```
