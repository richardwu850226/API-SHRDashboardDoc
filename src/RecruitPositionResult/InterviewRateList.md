# InterviewRateList
甄試結果比例分析

### HTTP Request
```
http://59.124.100.151:8090/servlet/apiM/dashboard/V1/interfaces/RecruitPositionResult/InterviewRateList
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
| needPeople | 總需求人數資訊 |
| register | 報到率資訊 |
| quit | 離職率資訊 |
| invite | 應徵率資訊 |
| interview | 面試率資訊 |
| offer | 錄取率資訊 |
| title | 上升下降值 |
| period | 本期值 |
| lastPeriod | 上期值 |

### HTTP Response when Successful
```json
{
   "responseHeader":{
      "resultMessage":"執行成功",
      "resultCode":"200"
   },
   "responseBody":{
      "needPeople":{
         "title":"-3",
         "period":"11",
         "lastPeriod":"14"
      },
      "register":{
         "title":"0",
         "period":"0",
         "lastPeriod":"0"
      },
      "quit":{
         "title":"0",
         "period":"0",
         "lastPeriod":"0"
      },
      "invite":{
         "title":"0",
         "period":"0",
         "lastPeriod":"0"
      },
      "interview":{
         "title":"0",
         "period":"0",
         "lastPeriod":"0"
      },
      "offer":{
         "title":"0",
         "period":"0",
         "lastPeriod":"0"
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
