# PeopleList
本期/上期人員狀態資訊

### HTTP Request
```
http://59.124.100.151:8090/servlet/apiM/dashboard/V1/interfaces/RecruitEfficiency/PeopleList
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
    ,"workPlace":"TW1"
    ,"yymm":"202301"
    ,"lastYymm":"202212"
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
| companyId | 1 | Array(String) | 公司代號 | Y | n/a |
| workPlace | TW1 | String | 工作地點 | Y | n/a |
| depType | 3 | String| 統計階層 | Y | n/a |
| yymm | 202212 | String | 本期月份 | Y | YYYYmm |
| lastYymm | 202206 | String | 上期月份 | Y | YYYYmm |

### requestBody FieldName
| FieldName | Description |
|:----------|:-------------|
| label | 標題訊息 |
| period | 本期 |
| lastPeriod | 上期 |
| employeeName | 員工中文姓名 |
| employeeId | 員工編號 |
| status | 招募狀態 |
| photo | 照片 |

### HTTP Response when Successful
```json
{
   "responseHeader":{
      "resultMessage":"執行成功",
      "resultCode":"200"
   },
   "responseBody":{
      "label":[
         {
            "labelWame":"姓名",
            "labelKey":"empFulName"
         },
         {
            "labelWame":"員工編號",
            "labelKey":"employeeId"
         },
         {
            "labelName":"状態",
            "labelKey":"empStatus"
         }
      ],
      "period":[
         {
            "employeeName":"陳小美",
            "employeeId":"L12345",
            "status":"已報到",
            "photo":"https://www.yahoo.com.tw"
         }
      ],
      "lastPeriod":[
         {
            "employeeName":"陳小美",
            "employeeId":"L12345",
            "status":"已報到",
            "photo":"https://www.yahoo.com.tw"
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
