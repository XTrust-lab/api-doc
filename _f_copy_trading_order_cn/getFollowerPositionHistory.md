---
title: 获取历史跟单持仓
position_number: 35
type: get
description: /future/copytrade/order/copy-trade/follower-position-history
parameters:
      -
        name: leaderAccountId
        type: number
        mandatory: true
        default:
        description: 交易员accountId
        ranges:
      -
        name: symbol
        type: string
        mandatory: false
        default:
        description: 交易对
        ranges:
      -
        name: direction
        type: string
        mandatory: false
        default:
        description: 方向(NEXT, PREV)
        ranges: NEXT, PREV
      -
        name: limit
        type: number
        mandatory: false
        default:
        description: 翻页大小
        ranges: 10
      -
        name: id
        type: number
        mandatory: false
        default:
        description: id,排序ID，用于翻页
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
                              "orderId": 0,//订单id
                              "clientOrderId": "",//自定义订单id
                              "symbol": "",//交易对
                              "orderType": "",//订单类型
                              "orderSide": "",//买卖方向
                              "positionSide": "",//持仓方向
                              "positionType": "",//仓位类型
                              "timeInForce": "",//有效类型
                              "closePosition": false,//是否条件全平仓
                              "price": 0.0,//委托价格
                              "origQty": 0.0,//数量（张）
                              "openSize": 0.0,//开仓数量
                              "closeSize": 0.0,//平仓数量
                              "avgPrice": 0.0,//成交均价
                              "closePrice": 0.0,//平仓价格
                              "executedQty": 0.0,//已成交数量（张）
                              "marginFrozen": 0.0,//占用保证金
                              "remark": "",//备注
                              "sourceId": 0,//关联交易员订单 id
                              "sourceType": "",//来源类型
                              "forceClose": false,//是否是强平订单
                              "leverage": 0,//下单时杠杠, 0 则是历史数据，没有存杠杠
                              "openPrice": 0.0,//开仓价格，根据平仓均价价格计算的
                              "closeProfit": 0.0,//平仓盈亏
                              "realizedPnl": 0.0,//平仓盈亏
                              "state": "",//订单状态 NEW：新建订单（未成交）；PARTIALLY_FILLED：部分成交；PARTIALLY_CANCELED：部分撤销；FILLED：全部成交；CANCELED：已撤销；REJECTED：下单失败；EXPIRED：已过期
                              "createdTime": 0,//创建时间
                              "updatedTime": 0,//更新时间
                              "isProfit": false,//成交时，是否触发止盈止损订单，如若是''跟单''，请直接设置对应价格，不设置isProfit
                              "triggerPriceType": "",//触发价格类型：INDEX_PRICE(指数价格); MARK_PRICE(标记价格)；LATEST_PRICE(最新价格)
                              "triggerProfitPrice": 0.0,//止盈触发价
                              "profitDelegateOrderType": "",//止损委托订单类型:LIMIT、MARKET
                              "profitDelegateTimeInForce": "",//止盈委托有效方式：1 GTC、2 FOK、3 IOC 4 GTX
                              "profitDelegatePrice": 0.0,//止盈委托委托价格
                              "triggerStopPrice": 0.0,//止损触发价
                              "stopDelegateOrderType": "",//止损委托订单类型:LIMIT、MARKET
                              "stopDelegateTimeInForce": "",//止损委托有效方式：1 GTC、2 FOK、3 IOC 4 GTX
                              "stopDelegatePrice": 0.0,//止损委托价格
                              "claimAmount": 0.0,//赔付金额
                              "claimCurrency": "",//赔付币种
                              "couponId": 0//包赔券ID
                            }
                          ]
                        }
                    }
        title: Response
        language: json
---
