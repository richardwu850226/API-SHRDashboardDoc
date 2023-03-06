# RateList
本期/上期各項招募比較分析

### HTTP Request
```
http://59.124.100.151:8090/servlet/apiM/dashboard/V1/interfaces/RecruitEfficiency/RateList
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
    ,"workPlace":"TW6"
    ,"depType": "3"
    ,"yymm": "202301"
    ,"lastYymm": "202212"
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
| workPlace | TW6 | String | 部門代碼 | N | n/a |
| depType | 3 | String| 統計階層 | Y | n/a |
| yymm | 202301 | String | 本期月份 | Y | YYYYmm |
| lastYymm | 202112 | String | 上期月份 | Y | YYYYmm |

### requestBody FieldName
| FieldName | Description |
|:----------|:-------------|
| data | 欄位資料 |
| itemName | 招募人數項目 |
| percent | 各項人數百分比 |

### HTTP Response when Successful
```json
{
   "responseHeader":{
      "resultMessage":"執行成功",
      "resultCode":"200"
   },
   "responseBody":{
      "data":[
         {
            "itemName":"邀約面試人數",
            "percent":240
         },
         {
            "itemName":"錄取人數",
            "percent":0
         },
         {
            "itemName":"報到人數",
            "percent":100
         },
         {
            "itemName":"離職人數",
            "percent":0
         },
         {
            "itemName":"面談率提升",
            "percent":0
         },
         {
            "itemName":"本期面談率",
            "percent":0
         },
         {
            "itemName":"上期面談率",
            "percent":0
         },
         {
            "itemName":"報到率提升",
            "percent":35
         },
         {
            "itemName":"本期報到率",
            "percent":35
         },
         {
            "itemName":"上期報到率",
            "percent":0
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
