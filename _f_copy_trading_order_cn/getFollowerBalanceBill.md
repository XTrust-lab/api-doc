---
title: 获取跟单资金流水
position_number: 36
type: get
description: /future/copytrade/user/v1/copy-trade/follower-balance-bill
parameters:
      -
        name: leaderAccountId
        type: number
        mandatory: true
        default:
        description: leader accountId
        ranges:
      -
        name: symbol
        type: string
        mandatory: false
        default:
        description: symbol
        ranges:
      -
        name: direction
        type: string
        mandatory: false
        default:
        description: direction
        ranges: NEXT, PREV
      -
        name: limit
        type: number
        mandatory: false
        default:
        description: page size
        ranges: 10
      -
        name: id
        type: number
        mandatory: false
        default:
        description: id
        ranges:

content_markdown: >-
    #### **Limit Flow Rules**
  
left_code_blocks:
    -
        code_block:
        title: Java
        language: java
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                        {
                            "returnCode": 0,
                            "msgInfo": "",
                            "error": {
                              "code": "",
                              "msg": "",
                              "args": [
                                {}
                              ]
                            },
                            "result": {
                              "hasPrev": false,
                              "hasNext": false,
                              "items": [
                                {
                                  "id": 0,
                                  "accountId": 0,//帐户id
                                  "coin": "",//币种
                                  "symbol": "",//交易对
                                  "type": "",//EXCHANGE 划转;CLOSE_POSITION:平仓盈亏;TAKE_OVER:仓位接管;QIANG_PING_MANAGER:强平管理费（手续费）;FUND:资金费用;FEE:手续费 (开仓、平仓、强平);ADL:自动减仓;TAKE_OVER:仓位接管MERGE:仓位合并
                                  "amount": 0.0,//数量
                                  "side": "",//ADD:划入; SUB:转出
                                  "afterAmount": 0.0,//变动后余额
                                  "createdTime": 0//时间
                                }
                              ]
                            }
                        }
        title: Response
        language: json
---
