# RecruitPeopleChart
本期/上期年月 招募效率分析圖表

### HTTP Request
```
http://59.124.100.151:8090/servlet/apiM/dashboard/V1/interfaces/RecruitEfficiency/RecruitPeopleChart
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
    ,"workPlace":"TW1"
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
| companyId | 1 | Array(String) | 公司代號 | N | n/a |
| workPlace | TW1 | String | 部門代碼 | N | n/a |
| depType | 3 | String| 統計階層 | Y | n/a |
| yymm | 202301 | String) | 本期月份 | Y | YYYYmm |
| lastYymm | 202112 | String | 上期月份 | Y | YYYYmm |

### requestBody FieldName
| FieldName | Description |
|:----------|:-------------|
| data | 欄位資料 |
| name | 欄位名稱 |

### HTTP Response when Successful
```json
{
    "responseHeader": {
        "resultMessage": "執行成功",
        "resultCode": "200"
    },
    "responseBody": {
        "series": [
            {
                "data": [
                    "0",
                    "0",
                    "0",
                    "0"
                ],
                "name": "202112"
            },
            {
                "data": [
                    "36",
                    "0",
                    "1",
                    "1"
                ],
                "name": "202301"
            }
        ],
        "xaxis": {
            "data": [
                "邀約面試人數",
                "錄取人數",
                "報到人數",
                "離職人數"
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
