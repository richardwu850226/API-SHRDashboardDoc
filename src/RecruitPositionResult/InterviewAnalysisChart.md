# InterviewAnalysisChart
甄試結果分析圖表

### HTTP Request
```
http://59.124.100.151:8090/servlet/apiM/dashboard/V1/interfaces/RecruitPositionResult/InterviewAnalysisChart
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
    ,"lastYymm":"202111"
    ,"yymm": "202112"
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
| yymm | 202112 | String | 本期年月 | Y | YYYYMM |
| lastYymm | 202111 | String | 上期年月 | Y | YYYYMM |

### requestBody FieldName
| FieldName | Description |
|:----------|:-------------|
| period | 本期資訊 |
| lastPeriod | 上期資訊 |
| periodYM | 年月 |
| series | 資料 |
| data | 數值 |
| xaxis | x軸 |

### HTTP Response when Successful
```json
{
   "responseHeader":{
      "resultMessage":"執行成功",
      "resultCode":"200"
   },
   "responseBody":{
      "period":{
         "periodYM":"202112",
         "series":[
            {
               "data":[
                  6,
                  6,
                  0,
                  0,
                  1,
                  1
               ]
            }
         ]
      },
      "lastPeriod":{
         "periodYM":"202111",
         "series":[
            {
               "data":[
                  9,
                  9,
                  0,
                  0,
                  1,
                  1
               ]
            }
         ],
         "xaxis":{
            "data":[
               "總履歷筆數",
               "總邀約人數",
               "總面試人數",
               "總錄取人數",
               "總實際報到人數",
               "總離職人數"
            ]
         }
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
