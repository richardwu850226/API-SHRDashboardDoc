# AssessEmployeeScoreChart
部門人員考核分數年度比較

### HTTP Request
```
http://59.124.100.151:8090/servlet/apiM/dashboard/V1/interfaces/AssessTrend/AssessEmployeeScoreChart
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
| series | 年度分數資料陣列 |
| filterIndex | 部門塞選對照KEY |
| years | 年度 |
| scores | 分數 |
| xaxis | 姓名 |
### HTTP Response when Successful
```json
{
   "responseHeader":{
      "resultMessage":"執行成功",
      "resultCode":"200"
   },
   "responseBody":{
      "filterIndex":{
         "data":[
            "22",
            "22",
            "22",
            "22",
            "20",
            "13",
            "13",
            "13",
            "18",
            "18",
            "18",
            "18",
            "18",
            "18",
            "18",
            "18",
            "18",
            "18",
            "18",
            "18",
            "18",
            "18",
            "18",
            "18",
            "18",
            "17",
            "17",
            "17",
            "17",
            "17",
            "17",
            "17",
            "19",
            "19",
            "19",
            "19",
            "19",
            "15",
            "6",
            "6",
            "6",
            "21"
         ]
      },
      "series":[
         {
            "years":"2022",
            "scores":[
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0",
               "60.0"
            ]
         },
         {
            "years":"2021",
            "scores":[
               
            ]
         }
      ],
      "xaxis":{
         "data":[
            "王O真",
            "蔡O芬",
            "王O蓉",
            "王O芳",
            "王O菱",
            "王O婷",
            "王O秋",
            "王O燕",
            "蔡O萍",
            "蔡O高",
            "TOT",
            "TOK",
            "MOS",
            "IOA",
            "王O祐",
            "王O洋",
            "王O銘",
            "王O峰",
            "王O明",
            "王O雄",
            "YOL",
            "LOS",
            "DOW",
            "JOL",
            "王O幹",
            "王O能",
            "蔡O賢",
            "王O香",
            "王O高",
            "王O新",
            "王O婉",
            "王O廷",
            "王O澕",
            "王O萱",
            "王O涵",
            "蔡O萍",
            "王O新",
            "王O琪",
            "王O霜",
            "蔡O沁",
            "王O如",
            "蔡O琳"
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
