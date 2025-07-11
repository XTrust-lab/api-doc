---
title: Get follower position history
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
                                  "accountId": 0, // account id
                                  "coin": "", // currency
                                  "symbol": "", // trading pair
                                  "type": "", // EXCHANGE transfer CLOSE_POSITION close profit/loss TAKE_OVER position takeover QIANG_PING_MANAGER forced liquidation management fee FUND funding fee FEE fee (open, close, forced liquidation) ADL auto-deleveraging TAKE_OVER position takeover MERGE position merge
                                  "amount": 0.0, // quantity
                                  "side": "", // ADD deposit SUB withdrawal
                                  "afterAmount": 0.0, // balance after change
                                  "createdTime": 0 // time
                                }
                              ]
                            }
                        }
        title: Response
        language: json
---
