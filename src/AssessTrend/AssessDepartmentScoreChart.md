# AssessDepartmentScoreChart
整體績效趨勢列表

### HTTP Request
```
http://59.124.100.151:8090/servlet/apiM/dashboard/V1/interfaces/AssessTrend/AssessDepartmentScoreChart
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
| name | 年度 |
| series | 年度資料 |
| xaxis | 部門資料 |

### HTTP Response when Successful
```json
{
   "responseHeader":{
      "resultMessage":"執行成功",
      "resultCode":"200"
   },
   "responseBody":{
      "series":[
         {
            "name":"2022",
            "data":[
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "0",
               "60.0",
               "60.0",
               "0"
            ]
         },
         {
            "name":"2021",
            "data":[
               "0",
               "0",
               "0",
               "0",
               "0",
               "0",
               "0",
               "0",
               "0",
               "0",
               "0"
            ]
         }
      ],
      "xaxis":{
         "data":[
            "總務部",
            "資訊部",
            "人力資源部",
            "生產組",
            "儲運組",
            "秘書室",
            "品保課",
            "中央廚房",
            "財會部",
            "採購部",
            "總管理處"
         ]
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
