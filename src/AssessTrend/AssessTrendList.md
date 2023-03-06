# AssessTrendList
整體績效趨勢列表

### HTTP Request
```
http://59.124.100.151:8090/servlet/apiM/dashboard/V1/interfaces/AssessTrend/AssessTrendList
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
    "companyId":["1"]
    ,"depNumber":[4]
    ,"assessItem":["A"]
    ,"depType": "7"
    ,"yy": "2022"
    ,"lastYymm": "2021"
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
| depNumber | 4 | Array(Integer) | 部門代碼 | N | n/a |
| depType | 7 | String| 統計階層 | Y | n/a |
| yy | 2022 | String | 本期月份 | Y | YYYYmm |
| lastYy | 2021 | String | 上期月份 | Y | YYYYmm |

### requestBody FieldName
| FieldName | Description |
|:----------|:-------------|
| data | 欄位資料 |
| name | 欄位名稱 |
| title | 標題 |
| lastScore | 上期分數 |
| score | 這期分數 |
| lastYy | 上年度 |
| yy | 今年度 |
| allGrowRate | 成長績效比率 |

### HTTP Response when Successful
```json
{
   "responseHeader":{
      "resultMessage":"執行成功",
      "resultCode":"200"
   },
   "responseBody":{
      "title":{
         "lastScore":11.0,
         "allGrowRate":4800.0,
         "score":540.0,
         "lastYy":"2021",
         "yy":"2022"
      },
      "data":[
         {
            "DeparmentName":"總務部",
            "growRate":6000.0,
            "lastScore":0.0,
            "score":60.0
         },
         {
            "DeparmentName":"資訊部",
            "growRate":6000.0,
            "lastScore":0.0,
            "score":60.0
         },
         {
            "DeparmentName":"人力資源部",
            "growRate":6000.0,
            "lastScore":0.0,
            "score":60.0
         },
         {
            "DeparmentName":"生產組",
            "growRate":6000.0,
            "lastScore":0.0,
            "score":60.0
         },
         {
            "DeparmentName":"儲運組",
            "growRate":6000.0,
            "lastScore":0.0,
            "score":60.0
         },
         {
            "DeparmentName":"秘書室",
            "growRate":6000.0,
            "lastScore":0.0,
            "score":60.0
         },
         {
            "DeparmentName":"品保課",
            "growRate":6000.0,
            "lastScore":0.0,
            "score":60.0
         },
         {
            "DeparmentName":"中央廚房",
            "growRate":0.0,
            "lastScore":0.0,
            "score":0.0
         },
         {
            "DeparmentName":"財會部",
            "growRate":6000.0,
            "lastScore":0.0,
            "score":60.0
         },
         {
            "DeparmentName":"採購部",
            "growRate":6000.0,
            "lastScore":0.0,
            "score":60.0
         },
         {
            "DeparmentName":"總管理處",
            "growRate":0.0,
            "lastScore":0.0,
            "score":0.0
         }
      ],
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
