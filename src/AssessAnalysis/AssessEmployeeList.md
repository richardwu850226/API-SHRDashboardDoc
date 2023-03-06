# AssessEmployeeList
人員考核資訊列表

### HTTP Request
```
http://59.124.100.151:8090/servlet/apiM/dashboard/V1/interfaces/AssessAnalysis/AssessEmployeeList
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
| label | 欄位資訊 |
| labelName | 中文名稱 |
| labelKey | 欄位key名稱 |
| data | 資料 |
| photo | 照片 |
| empFullName | 中文姓名 |
| employee | 員工編號 |
| departmentName | 部門名稱 |
| assessScore | 考核分數 |
| workYears | 年資 |
| inDate | 到職日期 |

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
            "labelName":"",
            "labelKey":"photo"
         },
         {
            "labelName":"姓名",
            "labelKey":"empFullName"
         },
         {
            "labelName":"員工編號",
            "labelKey":"employee"
         },
         {
            "labelName":"部門",
            "labelKey":"departmentName"
         },
         {
            "labelName":"考核分數",
            "labelKey":"assessScore"
         },
         {
            "labelName":"年資",
            "labelKey":"workYears"
         },
         {
            "labelName":"到職日期",
            "labelKey":"inDate"
         }
      ],
      "data":[
         {
            "photo":"babylon\\\\files\\\\履歷表.\\\\1612422826425_FF06C9BA-F491-4DE4-A926-044846627EC7.jpeg",
            "empFullName":"王O彬",
            "employee":"11002058",
            "departmentName":"友善外場",
            "assessScore":"60.00",
            "workYears":"1.39",
            "inDate":"20210208"
         },
         {
            "photo":"",
            "empFullName":"王O英",
            "employee":"10206047",
            "departmentName":"人力資源部",
            "assessScore":"60.00",
            "workYears":"9.02",
            "inDate":"20130624"
         },
         {
            "photo":"",
            "empFullName":"王O嘉",
            "employee":"10802031",
            "departmentName":"勞安部",
            "assessScore":"60.00",
            "workYears":"3.38",
            "inDate":"20190211"
         },
         {
            "photo":"",
            "empFullName":"王O涵",
            "employee":"11005049",
            "departmentName":"秘書室",
            "assessScore":"60.00",
            "workYears":"1.10",
            "inDate":"20210524"
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
