# NewEmployeeRateList
新進員工比例資訊

### HTTP Request
```
http://59.124.100.151:8090/servlet/apiM/dashboard/V1/interfaces/RecruitPositionResult/NewEmployeeRateList
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
    "companyId":[1,2]
    ,"lastYymm":"202211"
    ,"yymm": "202212"
    ,"depNumber":[]
    ,"depType": 8
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
| companyId | 1 | Array(String) | 公司代號 | N | n/a |
| depNumber | [] | Array(Integer) | 部門代碼 | N | n/a |
| depType | 8 | Integer | 統計階層 | Y | n/a |
| yymm | 202212 | String | 本期年月 | Y | YYYYMM |
| lastYymm | 202211 | String | 上期年月 | Y | YYYYMM |

### requestBody FieldName
| FieldName | Description |
|:----------|:-------------|
| opening | 錄取資訊 |
| offer | 報到資訊 |
| register | 職缺資訊 |
| send | 已寄送資訊 |
| receive | 預計寄送資訊 |
| title | 上升下降比例 |
| periodYymm | 本期月份 |
| periodEndYymm | 上期月份 |
| period | 本期數值 |
| lastPeriod | 上期數值 |



### HTTP Response when Successful
```json
{
   "responseHeader":{
      "resultMessage":"執行成功",
      "resultCode":"200"
   },
   "responseBody":{
      "opening":{
         "title":"-1",
         "periodYymm":"202112",
         "periodEndYymm":"202111",
         "period":8.0,
         "lastPeriod":9.0
      },
      "offer":{
         "title":"0",
         "periodYymm":"202112",
         "periodEndYymm":"202111",
         "period":0.0,
         "lastPeriod":0.0
      },
      "register":{
         "title":"-13",
         "periodYymm":"202112",
         "periodEndYymm":"202111",
         "startPno":8,
         "lastPno":9
      },
      "send":{
         "title":"-0",
         "periodYymm":"202112",
         "periodEndYymm":"202111",
         "startPno":0,
         "lastPno":0
      },
      "receive":{
         "title":"-0",
         "periodYymm":"202112",
         "periodEndYymm":"202111",
         "startPno":0,
         "lastPno":0
      }
   }
}
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
