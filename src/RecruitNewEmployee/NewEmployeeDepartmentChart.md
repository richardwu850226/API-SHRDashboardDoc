# NewEmployeeDepartmentChart
新進員工詳細圖表資訊

### HTTP Request
```
http://59.124.100.151:8090/servlet/apiM/dashboard/V1/interfaces/RecruitPositionResult/NewEmployeeDepartmentChart
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
| period | 本期月份 |
| lastPeriod | 上期月份 |
| periodYM | 年月 |
| series | 資料 |
| data | 數值 |
| name | 名稱 |

### HTTP Response when Successful
```json
{
   "responseHeader":{
      "resultMessage":"執行成功",
      "resultCode":"200"
   },
   "responseBody":{
      "period":{
         "periodYM":"202212",
         "series":[
            {
               "data":[
                  0,
                  8,
                  0,
                  0,
                  0,
                  0,
                  0,
                  0
               ],
               "name":"職缺人數"
            },
            {
               "data":[
                  0,
                  0,
                  0,
                  0,
                  0,
                  0,
                  0,
                  0
               ],
               "name":"錄取人數"
            },
            {
               "data":[
                  0,
                  0,
                  0,
                  0,
                  0,
                  0,
                  0,
                  0
               ],
               "name":"報到人數"
            },
            {
               "data":[
                  0,
                  0,
                  0,
                  0,
                  0,
                  0,
                  0,
                  0
               ],
               "name":"已寄送"
            },
            {
               "data":[
                  0,
                  0,
                  0,
                  0,
                  0,
                  0,
                  0,
                  0
               ],
               "name":"預計需寄送"
            }
         ],
         "xaxis":{
            "data":[
               "銷售本部",
               "人力資源部",
               "勞安部",
               "中央廚房",
               "採購部",
               "總務部",
               "開發部",
               "財會部"
            ]
         }
      },
      "lastPeriod":{
         "periodYM":"202211",
         "series":[
            {
               "data":[
                  0,
                  8,
                  0,
                  0,
                  0,
                  0,
                  0,
                  0
               ],
               "name":"職缺人數"
            },
            {
               "data":[
                  0,
                  0,
                  0,
                  0,
                  0,
                  0,
                  0,
                  0
               ],
               "name":"錄取人數"
            },
            {
               "data":[
                  0,
                  0,
                  0,
                  0,
                  0,
                  0,
                  0,
                  0
               ],
               "name":"報到人數"
            },
            {
               "data":[
                  0,
                  0,
                  0,
                  0,
                  0,
                  0,
                  0,
                  0
               ],
               "name":"已寄送"
            },
            {
               "data":[
                  0,
                  0,
                  0,
                  0,
                  0,
                  0,
                  0,
                  0
               ],
               "name":"預計需寄送"
            }
         ],
         "xaxis":{
            "data":[
               "銷售本部",
               "人力資源部",
               "勞安部",
               "中央廚房",
               "採購部",
               "總務部",
               "開發部",
               "財會部"
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
