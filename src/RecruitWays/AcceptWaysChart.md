# AcceptWaysChart
指定月份 錄取管道資訊

### HTTP Request
```
http://59.124.100.151:8090/servlet/apiM/dashboard/V1/interfaces/RecruitWays/AcceptWaysChart
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
    ,"depNumber":[1,2,3,4]
    ,"yymm":"202111"
    ,"lastYymm":"202110"
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
| companyId | 1 | Array(String) | 公司代號 | N | n/a |
| depNumber | 1,2,3,4 | Array(Integer) | 部門代碼 | N | n/a |
| depType | 3 | String| 統計階層 | Y | n/a |
| yymm | 202212 | String | 本期月份 | Y | YYYYmm |
| lastYymm | 202206 | String | 上期月份 | Y | YYYYmm |

### requestBody FieldName
| FieldName | Description |
|:----------|:-------------|
| data | 欄位資料 |
| name | 欄位名稱 |

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
            "data":[
               "59",
               "1",
               "28",
               "6",
               "1"
            ],
            "name":"202110"
         },
         {
            "data":[
               "68",
               "0",
               "24",
               "13",
               "3"
            ],
            "name":"202111"
         }
      ],
      "xaxis":{
         "data":[
            "104人力銀行",
            "公司網站",
            "A",
            "內部同仁推薦",
            "無填寫管道"
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
