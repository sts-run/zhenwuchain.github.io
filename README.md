
# Open-API

[中文文档](./README_zh.html),  [English API doc](./)

## General Info
Host: `https://wowexchange.xyz/gateway-api/`

## Order


**Address**: `/spot/open-api/v1/exchange/order`


**Method**: `POST`



**Request Content-Type**: `application/json`


**Response Content-Type**: `application/json`


**Description**:


**Request Demo**:


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


**Request Parameters**:


| Parameter name | Description | Type    | Required | Data Type | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|orderRequestDTO|Order request param|body|true|OrderRequestDTO|OrderRequestDTO|
|&emsp;&emsp;type|Order type,可用值:MARKET_PRICE,LIMIT_PRICE||true|string||
|&emsp;&emsp;amount|Buy or sell amount||true|number||
|&emsp;&emsp;symbol|symbol. format：BTC-USDT||true|string||
|&emsp;&emsp;direction|Order direction,可用值:BUY,SELL||true|string||
|&emsp;&emsp;price|price||true|number||
|&emsp;&emsp;useDiscount|Whether to use the discount,0:don't use; 1:use||true|integer(int32)||


**Response status**:


| code | Description | schema |
| -------- | -------- | ----- | 
|200|OK| |


**Response**:


| Parameter name | Description | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|msg||string||
|data||number||


**Response Demo**:
```javascript
{
	"code": 0,
	"msg": "",
	"data": 0
}
```


## Wallet Account


**Address**: `/spot/open-api/v1/wallets`


**Method**: `GET`


**Request Content-Type**: `application/x-www-form-urlencoded`


**Response Content-Type**: `application/json`


**Description**:


**Request Parameters**:


not available


**Response status**:


| Code | Description | schema |
| -------- | -------- | ----- | 
|200|OK| |


**Response**:


| Parameter name | Description | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|msg||string||
|data||number||


**Response Demo**:
```javascript
{
	"code": 0,
	"msg": "",
	"data": 0
}
```


## Get the symbol latest prices


**Address**: `/spot/open-api/v1/last-price/{symbol}`


**Method**: `GET`


**Request Content-Type**: `application/x-www-form-urlencoded`


**Response Content-Type**: `application/json`


**Description**:


**Request Parameters**:


| Parameter name | Description | Type    | Required | Data Type | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|symbol|symbol. format：BTC-USDT|path|true|string||


**Response status**:


| code | Description | schema |
| -------- | -------- | ----- | 
|200|OK| |


**Response**:


| Parameter name | Description | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|msg||string||
|data||number||


**Response Demo**:
```javascript
{
	"code": 0,
	"msg": "",
	"data": 0
}
```


## Get real-time K-line data


**Address**: `/spot/open-api/v1/k-line/{symbol}/{interval}`


**Method**: `GET`


**Request Content-Type**: `application/x-www-form-urlencoded`


**Response Content-Type**: `application/json`


**Description**:


**Request Parameters**:


| Parameter name | Description | Type    | Required | Data Type | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|symbol|symbol. format：BTC-USDT|path|true|string||
|interval|K-line interval, available: M1,M5,M15,M30,H1,H4,D1,W1,MON1|path|true|string||


**Response status**:


| code | Description | schema |
| -------- | -------- | ----- | 
|200|OK|CommonResultObject|


**Response**:


| Parameter name | Description | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|msg||string||
|data||object||


**Response Demo**:
```javascript
{
	"code": 0,
	"msg": "",
	"data": {}
}
```


## Recent Trades


**Address**: `/spot/open-api/v1/exchange/{symbol}/recent-trades`


**Method**: `GET`


**Request Content-Type**: `application/x-www-form-urlencoded`


**Response Content-Type**: `application/json`


**Description**:


**Request Parameters**:


| Parameter name | Description | Type    | Required | Data Type | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|symbol|symbol. format：BTC-USDT|path|true|string||
|count|Number of result records|query|true|integer(int32)||


**Response status**:


| code | Description | schema |
| -------- | -------- | ----- | 
|200|OK| |


**Response**:


| Parameter name | Description | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|msg||string||
|data||number||


**Response Demo**:
```javascript
{
	"code": 0,
	"msg": "",
	"data": 0
}
```


## Realtime Partial Book Depth


**Address**: `/spot/open-api/v1/exchange/{symbol}/partial`


**Method**: `GET`


**Request Content-Type**: `application/x-www-form-urlencoded`


**Response Content-Type**: `application/json`


**Description**:


**Request Parameters**:


| Parameter name | Description | Type    | Required | Data Type | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|symbol|symbol. format：BTC-USDT|path|true|string||
|depth|Count of depth|query|true|integer(int32)||


**Response status**:


| code | Description | schema |
| -------- | -------- | ----- | 
|200|OK| |


**Response**:


| Parameter name | Description | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code||integer(int32)|integer(int32)|
|msg||string||
|data||number||


**Response Demo**:
```javascript
{
	"code": 0,
	"msg": "",
	"data": 0
}
```
