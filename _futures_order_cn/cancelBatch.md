---
title: 批量撤销订单
position_number: 7
type: post
description: /future/trade/v1/order/cancel-batch
remark: Content-Type = application/x-www-form-urlencoded && application/json
parameters:
  - name: orderIds
    type: string
    mandatory: true
    default:
    description: order IDs (逗号分隔)
    ranges:
content_markdown: |-

                #### **限流规则**

                200/s/apikey
right_code_blocks:
  - code_block: |-
      {
        "error": {
          "code": "",
          "msg": ""
        },
        "msgInfo": "",
        "result": true,
        "returnCode": 0
      }
    title: Response
    language: json
---