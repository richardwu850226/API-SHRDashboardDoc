# AssessEmployeeList
人員考核分數成長比率列表

### HTTP Request
```
http://59.124.100.151:8090/servlet/apiM/dashboard/V1/interfaces/AssessTrend/AssessEmployeeList
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
    ,"depNumber":[4]
    ,"assessItem":["A"]
    ,"depType": "7"
    ,"yy": "2022"
    ,"lastYymm": "2021"
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
| depNumber | 4 | Array(Integer) | 部門代碼 | N | n/a |
| depType | 7 | String| 統計階層 | Y | n/a |
| yy | 2022 | String | 本期月份 | Y | YYYYmm |
| lastYy | 2021 | String | 上期月份 | Y | YYYYmm |

### requestBody FieldName
| FieldName | Description |
|:----------|:-------------|
| data | 欄位資料 |
| name | 欄位名稱 |
| title | 標題 |
| lastScore | 上期分數 |
| score | 這期分數 |
| lastYy | 上年度 |
| yy | 今年度 |
| allGrowRate | 成長績效比率 |

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
            "photo":"https://applv1.ecmaker-cloud.com/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f3a090f110f0f",
            "employeeName":"王O足",
            "employeeId":"10009002",
            "inDate":"20110901",
            "experience":10.8,
            "growRate":"6000",
            "companyName":"總務部"
         },
         {
            "photo":"https://applv1.ecmaker-cloud.com/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f3a090f110f0f",
            "employeeName":"王O新",
            "employeeId":"10808055",
            "inDate":"20190811",
            "experience":2.8,
            "growRate":"6000",
            "companyName":"儲運組"
         },
         {
            "photo":"https://applv1.ecmaker-cloud.com/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f3a090f110f0f",
            "employeeName":"蔡O宇",
            "employeeId":"10808081",
            "inDate":"20190826",
            "experience":2.8,
            "growRate":"6000",
            "companyName":"採購部"
         },
         {
            "photo":"https://applv1.ecmaker-cloud.com/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f3a090f110f0f",
            "employeeName":"王O秋",
            "employeeId":"11105073",
            "inDate":"20220516",
            "experience":0.1,
            "growRate":"6000",
            "companyName":"人力資源部"
         },
         {
            "photo":"https://applv1.ecmaker-cloud.com/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f3a090f110f0f",
            "employeeName":"王O蓉",
            "employeeId":"11105074",
            "inDate":"20220516",
            "experience":0.1,
            "growRate":"6000",
            "companyName":"總務部"
         },
         {
            "photo":"https://applv1.ecmaker-cloud.com/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f3a090f110f0f",
            "employeeName":"王O新",
            "employeeId":"11105112",
            "inDate":"20220501",
            "experience":0.1,
            "growRate":"6000",
            "companyName":"秘書室"
         },
         {
            "photo":"https://applv1.ecmaker-cloud.com/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f3a090f110f0f",
            "employeeName":"王O幹",
            "employeeId":"8703007",
            "inDate":"19980315",
            "experience":24.2,
            "growRate":"6000",
            "companyName":"生產組"
         },
         {
            "photo":"https://applv1.ecmaker-cloud.com/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f3a090f110f0f",
            "employeeName":"王O芳",
            "employeeId":"8712001",
            "inDate":"19981204",
            "experience":23.5,
            "growRate":"6000",
            "companyName":"總務部"
         },
         {
            "photo":"https://applv1.ecmaker-cloud.com/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f3a090f110f0f",
            "employeeName":"王O婉",
            "employeeId":"8806004",
            "inDate":"19990629",
            "experience":22.9,
            "growRate":"6000",
            "companyName":"儲運組"
         },
         {
            "photo":"https://applv1.ecmaker-cloud.com/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f3a090f110f0f",
            "employeeName":"王O燕",
            "employeeId":"9403012",
            "inDate":"20050309",
            "experience":17.3,
            "growRate":"6000",
            "companyName":"人力資源部"
         },
         {
            "photo":"https://applv1.ecmaker-cloud.com/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f3a090f110f0f",
            "employeeName":"王O廷",
            "employeeId":"9707001",
            "inDate":"20080701",
            "experience":13.9,
            "growRate":"6000",
            "companyName":"儲運組"
         },
         {
            "photo":"https://applv1.ecmaker-cloud.com/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f3a090f110f0f",
            "employeeName":"蔡O沁",
            "employeeId":"9708045",
            "inDate":"20080815",
            "experience":13.8,
            "growRate":"6000",
            "companyName":"財會部"
         },
         {
            "photo":"https://applv1.ecmaker-cloud.com/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f3a090f110f0f",
            "employeeName":"王O如",
            "employeeId":"9912073",
            "inDate":"20101230",
            "experience":11.4,
            "growRate":"6000",
            "companyName":"財會部"
         },
         {
            "photo":"https://applv1.ecmaker-cloud.com/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f3a090f110f0f",
            "employeeName":"TOS",
            "employeeId":"TESTL91004",
            "inDate":"20200501",
            "experience":2.1,
            "growRate":"6000",
            "companyName":"總管理處"
         }
      ],
      "label":[
         {
            "lableName":"",
            "lableKey":"photo"
         },
         {
            "lableName":"姓名",
            "lableKey":"employeeName"
         },
         {
            "lableName":"員工編號",
            "lableKey":"employeeId"
         },
         {
            "lableName":"到職日期",
            "lableKey":"inDate"
         },
         {
            "lableName":"年資",
            "lableKey":"experience"
         },
         {
            "lableName":"成長比率",
            "lableKey":"growRate"
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
