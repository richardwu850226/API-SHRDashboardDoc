# AssessAvgList
性別考核資訊

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
    "companyId":["1"]
    ,"assessItem":["A","B"]
    ,"depNumber":[7,13,14,16]
    ,"yy": "2022"
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
| depNumber | 7,13,14,16 | Array(Integer) | 部門代碼 | N | n/a |
| yy | 2022 | String | 年分 | Y | YYYY |
| assessItem | A,B | Array(String) | 考核項目 | Y | n/a |
| depType | 8 | Integer | 統計階層 | Y | n/a |

### requestBody FieldName
| FieldName | Description |
|:----------|:-------------|
| totlePeople | 總人數資料 |
| assessAvg | 考核平均分數資料 |
| ageAvg | 年資資料 |
| title | 總人數 |
| boyList | 男生人數 |
| girlList | 女生人數 |

### HTTP Response when Successful
```json
{
   "responseHeader":{
      "resultMessage":"執行成功",
      "resultCode":"200"
   },
   "responseBody":{
      "totlePeople":{
         "title":"4",
         "boyList":"2",
         "girlList":"2"
      },
      "assessAvg":{
         "title":"120.00",
         "boyList":"60.00",
         "girlList":"60.00"
      },
      "ageAvg":{
         "title":"7.45",
         "boyList":"5.06",
         "girlList":"2.39"
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
