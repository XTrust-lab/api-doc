---
title: Get Current Following List
position_number: 33
type: get
description: /future/copytrade/user/v1/copy-trade/current-following-v2
parameters:
    
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
                        "error": null,
                        "result": [
                          {
                            "id": 0,
                            "tenantId": 0,
                            "leaderName": "",
                            "leaderAccountId": "",
                            "leaderUserId": "",
                            "subAccountId": 0,
                            "avatar": "",
                            "followMode": "", // Follow mode: CUSTOM, AUTO
                            "startTime": 0,
                            "endTime": 0,
                            "followAmount": 0.0, // Net follow amount
                            "followVal": 0.0, // Custom follow quantity
                            "followType": "", // Custom follow type
                            "followMargin": 0.0, // Custom follow principal
                            "profit": 0.0, // Settled profit and loss
                            "divideProfit": 0.0, // Profit sharing expenditure
                            "divideRate": 0.0, // Profit sharing rate
                            "orderList": [
                              {
                                "symbol": "",
                                "symbolName": "",
                                "positionType": "", // Position type CROSSED (cross margin) ISOLATED (isolated margin)
                                "positionSide": "", // Position direction LONG; SHORT
                                "openLeverage": 0, // Leverage
                                "id": 0,
                                "leaderAccountId": "", // Trader accountId
                                "accountId": 0, // Follower account id
                                "orderId": 0, // Order id
                                "trackNo": 0, // Follow trackNo
                                "openTime": 0, // Open time
                                "closeTime": 0, // Close time
                                "openPrice": 0.0, // Open average price
                                "closePrice": 0.0, // Close average price
                                "openMargin": 0.0, // Initial margin
                                "realizedPnl": 0.0, // Realized profit and loss
                                "profitRate": 0.0, // Profit rate, multiplied by 100
                                "openSize": 0.0, // Open position quantity
                                "closeSize": 0.0, // Closed position quantity
                                "positionSize": 0.0, // Position quantity
                                "closeOrderSize": 0.0, // Closed order occupied
                                "availableCloseSize": 0.0, // Available close quantity
                                "profitId": 0, // Take profit/stop loss id
                                "triggerPriceType": "", // Trigger price type 1 Index price 2 Mark price 3 Last price
                               "triggerProfitPrice": 0.0, // Take profit trigger price
                                "triggerStopPrice": 0.0, // Stop loss trigger price
                                "contractType": "", // Contract type PERPETUAL, PREDICT
                                "entryPrice": 0.0, // Entry average price
                                "openOrderSize": 0.0, // Open order occupied
                                "isolatedMargin": 0.0, // Isolated margin
                                "openOrderMarginFrozen": 0.0, // Open order margin occupied
                                "realizedProfit": 0.0, // Realized profit
                                "autoMargin": false, // Auto add margin
                                "leverage": 0, // Leverage multiplier
                                "closeProfit": 0.0, // Close profit and loss
                                "totalFee": 0.0, // Fee
                                "totalFundFee": 0.0 // Funding fee
                              }
                            ]
                          }
                        ]
                        }
        title: Response
        language: json
---
