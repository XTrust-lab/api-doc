---
title: Query trade
position_number: 1
type: get
description: /v4/trade
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: Trading pair, if not filled in, represents all
        ranges:
    -
        name: bizType
        type: string
        mandatory: false
        default:
        description: "SPOT, LEVER"
        ranges:
    -
        name: orderSide
        type: string
        mandatory: false
        default:
        description: BUY,SELL
        ranges:
    -
        name: orderType
        type: string
        mandatory: false
        default:
        description: LIMIT, MARKET
        ranges:
    -
        name: orderId
        type: number
        mandatory: false
        default:
        description: 
        ranges:
    -
        name: fromId
        type: number
        mandatory: false
        default:
        description: start id
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default:
        description: query direction:PREV, NEXT
        ranges:
    -
        name: limit
        type: number
        mandatory: false
        default: '20'
        description: Limit number, max 100
        ranges:
    -
        name: startTime
        type: number
        mandatory: false
        default:
        description: start time eg:1657682804112
        ranges:
    -
        name: endTime
        type: number
        mandatory: false
        default:
        description: 
        ranges:
content_markdown:
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
                    "rc": 0,
                    "mc": "string",
                    "ma": [
                      {}
                        ],
                        "result": {
                          "hasPrev": true,
                          "hasNext": true,
                          "items": [
                            {
                              "symbol": "BTC_USDT",               // Trading pair
                              "tradeId": "6316559590087222001",   // Trade ID
                              "orderId": "6216559590087220004",   // Order ID
                              "orderSide": "BUY",                 // Order direction
                              "orderType": "LIMIT",               // Order type
                              "bizType": "SPOT",                  // Business type
                              "time": 1655958915583,              // Trade time
                              "price": "40000",                   // Trade price
                              "quantity": "1.2",                  // Trade quantity
                              "quoteQty": "48000",                // Trade amount
                              "baseCurrency": "BTC",              // Base currency type
                              "quoteCurrency": "USDT",            // Quote currency type
                              "takerMaker": "taker",              // Taker/Maker
                    
                              "deductType": "COUPON",             // Fee deduction type: COUPON - coupon, PLATFORM_CURRENCY - platform currency deduction, null - no deduction. Coupons and platform currency deductions cannot be used simultaneously, coupons are prioritized. When using platform currency deduction, the fee will either be fully deducted or not deducted at all, partial deduction is not possible.
                              "deductFee": "0.003",               // If the deduction type is COUPON, this is the amount of fee deducted using the coupon, in the original fee currency unit; otherwise, null.
                    
                              "fee": "0.5",                       // Fee asset amount. If using platform currency deduction, this is the amount of platform currency used; otherwise, the original fee amount.
                              "feeCurrency": "USDT",              // Fee asset type, corresponding to the fee currency.
                    
                              "couponAmount": "0.002",            // If the deduction type is COUPON, this is the amount of coupon currency used; otherwise, null.
                              "couponCurrency": "usdt"            // If the deduction type is COUPON, this is the coupon currency.
                            }
                          ]
                        }
                    }
        title: Response
        language: json
---

