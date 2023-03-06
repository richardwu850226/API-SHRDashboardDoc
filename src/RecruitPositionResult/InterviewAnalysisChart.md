# InterviewAnalysisChart
甄試結果分析圖表

### HTTP Request
```
http://59.124.100.151:8090/servlet/apiM/dashboard/V1/interfaces/AssessAnalysis/AssessAvgList
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
| yymm | 2022 | String | 本期年月 | Y | YYYYMM |
| lastYymm | 2022 | String | 上期年月 | Y | YYYYMM |

### requestBody FieldName
| FieldName | Description |
|:----------|:-------------|
| period | 本期資訊 |
| lastPeriod | 上期資訊 |
| position | 中文職稱 |
| needPeople | 需求人數 |
| checkIn | 報到人數 |
| checkInRate | 報到率 |

### HTTP Response when Successful
```json
{
   "responseHeader":{
      "resultMessage":"執行成功",
      "resultCode":"200"
   },
   "responseBody":{
      "period":[
         {
            "position":"外場-正職人員",
            "needPeople":0,
            "checkIn":1,
            "checkInRate":0
         },
         {
            "position":"正職",
            "needPeople":3,
            "checkIn":0,
            "checkInRate":0
         },
         {
            "position":"兼職",
            "needPeople":1,
            "checkIn":0,
            "checkInRate":0
         },
         {
            "position":"兼職一級",
            "needPeople":2,
            "checkIn":0,
            "checkInRate":0
         },
         {
            "position":"兼職二級",
            "needPeople":1,
            "checkIn":0,
            "checkInRate":0
         },
         {
            "position":"資深正職",
            "needPeople":1,
            "checkIn":0,
            "checkInRate":0
         },
         {
            "position":"實習領班",
            "needPeople":2,
            "checkIn":0,
            "checkInRate":0
         },
         {
            "position":"領班",
            "needPeople":1,
            "checkIn":0,
            "checkInRate":0
         },
         {
            "position":"儲備幹部",
            "needPeople":1,
            "checkIn":0,
            "checkInRate":0
         }
      ],
      "lastPeriod":[
         {
            "position":"外場-正職人員",
            "needPeople":0,
            "checkIn":1,
            "checkInRate":0
         },
         {
            "position":"正職",
            "needPeople":2,
            "checkIn":0,
            "checkInRate":0
         },
         {
            "position":"兼職一級",
            "needPeople":4,
            "checkIn":0,
            "checkInRate":0
         },
         {
            "position":"副店主管",
            "needPeople":1,
            "checkIn":0,
            "checkInRate":0
         },
         {
            "position":"實習領班",
            "needPeople":2,
            "checkIn":0,
            "checkInRate":0
         },
         {
            "position":"儲備幹部",
            "needPeople":2,
            "checkIn":0,
            "checkInRate":0
         }
      ]
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
