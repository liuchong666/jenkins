## 1、资产接口文档
### 1、划转资产

**请求url**：`http://yopon.ingoodfund.com/tradebibi/api/UserAsset/Transfer`

**请求方法**：`POST`

**请求头**

| 名称          | 类型   | 是否必须 |
| ------------- | ------ | -------- |
| Authorization | string | 是       |

​             

**请求参数**

```json
[{
    "FromAccount": 1,
    "ToAccount": 2,
    "Coin": "USDT",
    "Amount": 0.1
}]
```



| 名称        | 类型    | 是否必须 | 描述                                                       |
| ----------- | ------- | -------- | ---------------------------------------------------------- |
| FromAccount | int     | 是       | 出账账户类型，钱包=2，币币=4，信用=8，云算力=16，交易=1025 |
| ToAccount   | int     | 是       | 入账账户类型，钱包=2，币币=4，信用=8，云算力=16，交易=1025 |
| Coin        | string  | 是       | 币种简称                                                   |
| Amount      | decimal | 是       | 划转金额                                                   |



**返回结果**

```
{
	code=200
}
```



### 2、提交提币单

**请求url**：`http://yopon.ingoodfund.com/tradebibi/api/UserAsset/WithdrawSubmit`

**请求方法**：`POST`

**请求头**

| 名称          | 类型   | 是否必须 |
| ------------- | ------ | -------- |
| Authorization | string | 是       |

​             

**请求参数**
```php
function getAdder(int $x): int 
{
    return 123;
}
```

```json, webmanifest
[
    {
        "LinkName": "ETH",
        "Coin": "USDT",
        "Address": "0xc1b3ed7d3b9Ff30bDf36c252ea994ACD0b988Cfe",
        "Password": "111111",
        "Amount": 0.01,
        "Type": 2
    }
]
```



| 名称     | 类型    | 是否必须 | 描述                                                  |
| -------- | ------- | -------- | ----------------------------------------------------- |
| LinkName | string  | 是       | 提币链                                                |
| Address  | string  | 是       | 提币地址                                              |
| Coin     | string  | 是       | 币种简称                                              |
| Amount   | decimal | 是       | 提币金额                                              |
| Password | string  | 是       | 密码                                                  |
| Type     | int     | 是       | 提币账户 钱包=2，币币=4，信用=8，云算力=16，交易=1025 |



**返回结果**

```json
{
	code=200
}
```

