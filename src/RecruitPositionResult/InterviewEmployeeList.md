# InterviewEmployeeList
甄試結果人員資訊

### HTTP Request
```
http://59.124.100.151:8090/servlet/apiM/dashboard/V1/interfaces/RecruitPositionResult/InterviewEmployeeList
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
| label | key值資訊 |
| labelName | 欄位中文名稱 |
| labelKey | 欄位key名稱 |
| period | 本期資訊 |
| lastPeriod | 上期資訊 |
| photo | 照片 |
| empFullName | 中文姓名 |
| age | 年齡 |
| position | 中文職稱 |
| empStatus | 狀態 |
| interviewerLink | 履歷連結 |
| pno | 單號 |

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
            "labelName":"年齡",
            "labelKey":"age"
         },
         {
            "labelName":"職位",
            "labelKey":"position"
         },
         {
            "labelName":"狀態",
            "labelKey":"empStatus"
         },
         {
            "labelName":"履歷連結",
            "labelKey":"interviewerLink"
         },
         {
            "labelName":"單號",
            "labelKey":"pno"
         }
      ],
      "period":[
         {
            "photo":"https://applv1.ecmaker-cloud.com/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f4c5d5e5d46535051635956535a4c63da8e9ad99288d79e9711630e090c07080a08070b0f0b0809600d0f0d0e120e0d120f091f0e0f600d07600c0612790f0e12db84b8db849ad8b18d114f5b591f121f7e5b505d5a1f7e5c4d505d5e4b1f6d5a5e5b5a4d1f7b7c1f17090b125d564b16114f5158",
            "empFullName":"王O献",
            "age":"35",
            "position":"內場-正職人員",
            "empStatus":"待報到",
            "interviewerLink":"",
            "pno":"002021120600001"
         },
         {
            "photo":"",
            "empFullName":"蔡O惠",
            "age":"34",
            "position":"外場-正職人員",
            "empStatus":"",
            "interviewerLink":"",
            "pno":"002021120700001"
         },
         {
            "photo":"https://applv1.ecmaker-cloud.com/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f0a5d5e5d46535051635956535a4c63da8e9ad99288d79e9711630e090c060f09090c0b0d080a0f600f060e0f090e060c0d0a11554f58",
            "empFullName":"王O華",
            "age":"34",
            "position":"外場-主管",
            "empStatus":"待報到",
            "interviewerLink":"",
            "pno":"002021121000001"
         },
         {
            "photo":"https://applv1.ecmaker-cloud.com/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f6f5d5e5d46535051635956535a4c63da8e9ad99288d79e9711630e090c060b090d0a0a0d0f0f06607d067d090a087c0f127a0b7d7c120b7a7e7d12070a0c0c120f0c7a09070f087a0a090f7e11554f5a58",
            "empFullName":"蔡O銘",
            "age":"34",
            "position":"外場-正職人員",
            "empStatus":"待報到",
            "interviewerLink":"",
            "pno":"002021121400004"
         }
      ],
      "lastPeriod":[
         {
            "photo":"https://applv1.ecmaker-cloud.com/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f725d5e5d46535051635956535a4c63da8e9ad99288d79e9711630e090c0a070e0d0f0c0c070c08606c5c4d5a5a514c57504b600d0f0d0e0e0e0f0d120f070e0f0b0e607e51467b5a4c5411554f58",
            "empFullName":"王O民",
            "age":"39",
            "position":"外場-正職人員",
            "empStatus":"待報到",
            "interviewerLink":"",
            "pno":"002021110200001"
         },
         {
            "photo":"https://applv1.ecmaker-cloud.com/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f6f5d5e5d46535051635956535a4c63da8e9ad99288d79e9711630e090c090f0f0d090b0f0e080b607e7c0a7b097a077e127a7d097c120b0e7e091207070a7912097a7c07070c077e08077e0a11554f5a58",
            "empFullName":"蔡O惠",
            "age":"34",
            "position":"實習領班",
            "empStatus":"待報到",
            "interviewerLink":"",
            "pno":"002021110400001"
         },
         {
            "photo":"",
            "empFullName":"蔡O伶",
            "age":"32",
            "position":"外場-主管",
            "empStatus":"",
            "interviewerLink":"",
            "pno":"002021110800001"
         },
         {
            "photo":"https://applv1.ecmaker-cloud.com/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f6f5d5e5d46535051635956535a4c63da8e9ad99288d79e9711630e090c09090f0e0a0e0d090b0d60067b0b7e7b0c0709127e07090c120b7a7c0a127d0e060a127e0f080e06097c06790f060a11554f5a58",
            "empFullName":"蔡O芳",
            "age":"41",
            "position":"外場-正職人員",
            "empStatus":"待報到",
            "interviewerLink":"",
            "pno":"002021111100001"
         },
         {
            "photo":"https://applv1.ecmaker-cloud.com/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f6f5d5e5d46535051635956535a4c63da8e9ad99288d79e9711630e090c09090e0e09090809060c600a0c7c08097b0e79127a7d7e0b120b087909127e7e0d7c12070c090c09077b0a0f09070f11554f5a58",
            "empFullName":"蔡O芳",
            "age":"41",
            "position":"外場-正職人員",
            "empStatus":"簽核中",
            "interviewerLink":"",
            "pno":"002021111100002"
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
