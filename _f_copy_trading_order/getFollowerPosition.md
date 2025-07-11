---
title: Get follower position
position_number: 34
type: get
description: /future/copytrade/user/v1/copy-trade/follower-position
parameters:
    -
        name: leaderAccountId
        type: number
        mandatory: true
        default:
        description: leader accountId
        ranges: 

content_markdown: >-
    #### **Limit Flow Rules**
    
    2/s/apikey
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
                                "symbol": "", // Trading pair
                                "accountId": 0, // Copy trading account ID
                                "positionType": "", // Position type CROSSED (cross margin) ISOLATED (isolated margin)
                               "positionSide": "", // Position direction
                                "contractType": "", // Contract type: PERPETUAL (perpetual contract), PREDICT (prediction contract)
                                "positionSize": 0.0, // Position size (contracts)
                                "closeOrderSize": 0.0, // Close order size (contracts)
                                "availableCloseSize": 0.0, // Available close size (contracts)
                                "entryPrice": 0.0, // Entry average price
                                "openOrderSize": 0.0, // Open order occupied
                                "isolatedMargin": 0.0, // Isolated margin
                                "openOrderMarginFrozen": 0.0, // Open order margin occupied
                                "realizedProfit": 0.0, // Realized profit and loss
                                "autoMargin": false, // Auto add margin
                                "leverage": 0, // Leverage
                                "profitId": 0, // Take profit/stop loss ID
                                "triggerPriceType": "", // Trigger price type 1. Index price 2. Mark price (fair price) 3. Latest price
                                "triggerProfitPrice": 0.0, // Take profit trigger price
                                "triggerStopPrice": 0.0, // Stop loss trigger price
                                "profitFixedLatest": { // Latest partial position take profit/stop loss settings
                                  "profitId": 0, // Take profit/stop loss ID
                                  "triggerPriceType": "", // Trigger price type 1. Index price 2. Mark price (fair price) 3. Latest price
                                  "triggerProfitPrice": 0.0, // Take profit trigger price
                                  "triggerStopPrice": 0.0 // Stop loss trigger price
                                },
                                "profitFixedCount": 0, // Total number of partial position take profit/stop loss
                                "isWelfareAccount": false, // Is welfare account
                                "closeProfit": 0.0, // Close profit and loss
                                "totalFee": 0.0, // Fee
                                "totalFundFee": 0.0, // Funding fee
                                "reverseEntrustId": 0, // Reverse order ID
                                "reverseStopPrice": 0.0, // Reverse trigger price
                                "reverseTriggerPriceType": "", // Reverse trigger price type
                                "contractSize": 0.0, // Contract value
                                "markPrice": 0.0, // Mark price
                                "updatedTime": 0 // Update time
                              }
                            ]
                        }
        title: Response
        language: json
---
