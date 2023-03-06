# AssessGradeEmployeeList
職員考核資訊

### HTTP Request
```
http://59.124.100.151:8090/servlet/apiM/dashboard/V1/interfaces/AssessDistribution/AssessGradeEmployeeList
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
    ,"depNumber":[4]
    ,"depType": "7"
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
| depNumber | 4 | Array(Integer) | 部門代碼 | N | n/a |
| depType | 7 | String| 統計階層 | Y | n/a |
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
      "data":[
         {
            "photo":"",
            "employeeName":"王O萱",
            "departmentName":"秘書室",
            "inDate":"20210217",
            "experience":2.0,
            "grade":"優等",
            "pass":true
         },
         {
            "photo":"",
            "employeeName":"王O琪",
            "departmentName":"品保課",
            "inDate":"20210504",
            "experience":1.8,
            "grade":"優等",
            "pass":true
         },
         {
            "photo":"",
            "employeeName":"王O涵",
            "departmentName":"秘書室",
            "inDate":"20210524",
            "experience":1.8,
            "grade":"優等",
            "pass":true
         },
         {
            "photo":"https://applv1.ecmaker-cloud.com/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f1110574d520b104f57504b50100e090a0d09070a0e0d0a0d0b08600d0f0f0b0f0e0d0e0d08120e1f170d1611554f58",
            "employeeName":"王O霜",
            "departmentName":"財會部",
            "inDate":"20210628",
            "experience":1.7,
            "grade":"優等",
            "pass":true
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
