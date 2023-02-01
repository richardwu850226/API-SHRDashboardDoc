# AcceptWaysChart
當月/前月 錄取管道分析圖表

### HTTP Request
```
http://59.124.100.151:8090/servlet/apiM/shiftAPP/V1/interfaces/AcceptWaysChart
```

### HTTP Request Mehod
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過apiLogin取得
| right | 51341911904173543336756162544864820 | String | 需透過apiLogin取得 |

### JSON representation
Here is a JSON representation of request.
```json
{
  "requestHeader": {
  },
  "requestBody": {
    "companyId":"1"
    ,"depNumber":[1,2,3,4]
    ,"yymm": "202301"
    ,"lastYymm":"202302"
    ,"depType":3
  },
  "uid":"98599308101484732326",
  "right":"51341911904173543336756162544864820"
}
```

### Properties
| Property | Type | Description |
|:---------|:-----|:------------|
| requestHeader | Object | 要求本文 |
| requestBody | Object | 要求本文 |

### requestBody Properties
| Key | Value | Type | Description | Required | Format |
|:----------|:-------------|:-----|:------------|:------------|:------------|
| companyId | TW | String | 公司別代碼 | Y | n/a |
| depNumber | 17 | Array(Integer) | 部門代碼 | Y | n/a |
| yymm | 202301 | String | 下期年度 | Y | n/a |
| lastYymm | 202302 | String | 上期年度 | Y | n/a |
| depType | 3 | Integer | 部門階級 | Y | n/a |

### requestBody FieldName
| FieldName | Description |
|:----------|:-------------|
| resultMessage | 結果訊息 |
| resultCode | 結果代號 |
| message | 訊息 |

### HTTP Response when Successful

```json

```

### HTTP Response when No Data
此程式不會有查無資料發生

### HTTP Response when Failed
```json
{
    "responseHeader": {
        "resultMessage": "xxxxx",
        "resultCode": "500"
    },
    "responseBody": {
    }
}
```

### HTTP Response when Exception
```json
{
    "responseHeader": {
        "resultMessage": "xxxxx",
        "resultCode": "406"
    },
    "responseBody": {
    }
}
```
