# AssessGradeExperienceChart
考核等級平均年資

### HTTP Request
```
http://59.124.100.151:8090/servlet/apiM/dashboard/V1/interfaces/AssessDistribution/AssessGradeExperienceChart
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
    ,"assessItem":["A","B"]
    ,"depNumber":[1,2,3,4]
    ,"depType": "3"
    ,"yy": "2022"
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
| assessItem | A,B | Array(String) | 考核項目 | Y | n/a |
| depNumber | 1,2,3,4 | Array(Integer) | 部門代碼 | N | n/a |
| depType | 3 | String| 統計階層 | Y | n/a |
| yy | 2022 | String | 本期月份 | Y | YYYYmm |

### requestBody FieldName
| FieldName | Description |
|:----------|:-------------|
| data | 考核等級資料列表 |
| series | 平均年資列表 |


### HTTP Response when Successful
```json
{
   "responseHeader":{
      "resultMessage":"執行成功",
      "resultCode":"200"
   },
   "responseBody":{
      "series":[
         "4"
      ],
      "xaxis":{
         "data":[
            "考核等級A"
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
