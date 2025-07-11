---
title: Get follower position history
position_number: 35
type: get
description: /future/copytrade/user/v1/copy-trade/follower-position-history
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
                            "error": null,
                            "result": {
                              "hasPrev": false,
                              "hasNext": false,
                              "items": [
                                {
                                  "orderId": 0, // order id
                                  "clientOrderId": "", // custom order id
                                  "symbol": "", // trading pair
                                  "orderType": "", // order type
                                  "orderSide": "", // buy/sell direction
                                  "positionSide": "", // position direction
                                  "positionType": "", // position type
                                  "timeInForce": "", // validity type
                                  "closePosition": false, // conditional close all positions
                                  "price": 0.0, // order price
                                  "origQty": 0.0, // quantity (contracts)
                                  "openSize": 0.0, // open position quantity
                                  "closeSize": 0.0, // close position quantity
                                  "avgPrice": 0.0, // average transaction price
                                  "closePrice": 0.0, // close position price
                                  "executedQty": 0.0, // executed quantity (contracts)
                                  "marginFrozen": 0.0, // margin occupied
                                  "remark": "", // remark
                                  "sourceId": 0, // associated trader order id
                                  "sourceType": "", // source type
                                  "forceClose": false, // forced liquidation order
                                  "leverage": 0, // leverage at order, 0 means historical data, no leverage stored
                                  "openPrice": 0.0, // open position price, calculated from close average price
                                  "closeProfit": 0.0, // close position profit and loss
                                  "realizedPnl": 0.0, // realized profit and loss
                                  "state": "", // order status NEW new order (not filled) PARTIALLY_FILLED partially filled PARTIALLY_CANCELED partially canceled FILLED fully filled CANCELED canceled REJECTED order failed EXPIRED expired
                                  "createdTime": 0, // creation time
                                  "updatedTime": 0, // update time
                                  "isProfit": false, // on transaction, whether triggered take profit/stop loss order, if copy trading, set corresponding price directly, do not set isProfit
                                  "triggerPriceType": "", // trigger price type INDEX_PRICE index price MARK_PRICE mark price LATEST_PRICE latest price
                                  "triggerProfitPrice": 0.0, // take profit trigger price
                                  "profitDelegateOrderType": "", // take profit delegate order type LIMIT MARKET
                                  "profitDelegateTimeInForce": "", // take profit delegate validity type 1 GTC 2 FOK 3 IOC 4 GTX
                                  "profitDelegatePrice": 0.0, // take profit delegate order price
                                  "triggerStopPrice": 0.0, // stop loss trigger price
                                  "stopDelegateOrderType": "", // stop loss delegate order type LIMIT MARKET
                                  "stopDelegateTimeInForce": "", // stop loss delegate validity type 1 GTC 2 FOK 3 IOC 4 GTX
                                  "stopDelegatePrice": 0.0, // stop loss delegate price
                                  "claimAmount": 0.0, // compensation amount
                                  "claimCurrency": "", // compensation currency
                                  "couponId": 0 // compensation coupon ID
                                }
                              ]
                            }
                        }
        title: Response
        language: json
---
