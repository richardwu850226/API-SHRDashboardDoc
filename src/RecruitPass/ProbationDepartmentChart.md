# ProbationDepartmentChart
人數詳細圖表資訊

### HTTP Request
```
http://59.124.100.151:8090/servlet/apiM/dashboard/V1/interfaces/RecruitPass/ProbationDepartmentChart
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
    ,"depNumber":[16]
    ,"depType": "8"
    ,"yymm": "202212"
    ,"lastYymm": "202206"
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
| companyId | TW | Array(String) | 公司代號 | N | n/a |
| depNumber | 17 | Array(Integer) | 部門代碼 | N | n/a |
| depType | 8 | String| 統計階層 | Y | n/a |
| depNumber | 17 | Array(Integer) | 部門代碼 | Y | n/a |
| yymm | 202212 | Array(Integer) | 本期月份 | Y | YYYYmm |
| lastYymm | 202206 | String | 上期月份 | Y | YYYYmm |

### requestBody FieldName
| FieldName | Description |
|:----------|:-------------|
| data | 欄位資料 |
| name | 欄位名稱 |
| periodYM | 期數月份 |

### HTTP Response when Successful
```json
{
    "responseHeader": {
        "resultMessage": "執行成功",
        "resultCode": "200"
    },
    "responseBody": {
        "period": {
            "periodYM": "202212",
            "series": [
                {
                    "data": [
                        0
                    ],
                    "name": "報到人數"
                },
                {
                    "data": [
                        0
                    ],
                    "name": "通過人數"
                },
                {
                    "data": [
                        0
                    ],
                    "name": "離職人數"
                },
                {
                    "data": [
                        0
                    ],
                    "name": "七日內離職人數"
                }
            ],
            "xaxis": {
                "data": [
                    "樂樂復興店外場"
                ]
            }
        },
        "lastPeriod": {
            "periodYM": "202206",
            "series": [
                {
                    "data": [
                        0
                    ],
                    "name": "報到人數"
                },
                {
                    "data": [
                        0
                    ],
                    "name": "通過人數"
                },
                {
                    "data": [
                        0
                    ],
                    "name": "離職人數"
                },
                {
                    "data": [
                        0
                    ],
                    "name": "七日內離職人數"
                }
            ],
            "xaxis": {
                "data": [
                    "樂樂復興店外場"
                ]
            }
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
