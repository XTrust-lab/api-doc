---
title: 获取当前跟单持仓
position_number: 34
type: get
description: /future/copytrade/order/copy-trade/follower-position
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
                                "symbol": "",//交易对
                                "accountId": 0,//跟单账号id
                                "positionType": "",//仓位类型:CROSSED(全仓);ISOLATED(逐仓)
                                "positionSide": "",//持仓方向
                                "contractType": "",//合约类型：PERPETUAL(永续合约)、PREDICT(预测合约)
                                "positionSize": 0.0,//持仓数量（张）
                                "closeOrderSize": 0.0,//平仓挂单数量（张）
                                "availableCloseSize": 0.0,//可平仓数量（张）
                                "entryPrice": 0.0,//开仓均价
                                "openOrderSize": 0.0,//开仓订单占用
                                "isolatedMargin": 0.0,//逐仓保证金
                                "openOrderMarginFrozen": 0.0,//开仓订单保证金占用
                                "realizedProfit": 0.0,//已实现盈亏
                                "autoMargin": false,//是否自动追加保证金
                                "leverage": 0,//杠杆倍数
                                "profitId": 0,//止盈止损id
                                "triggerPriceType": "",//触发价格类型 1、指数价格 2：标记价格（合理价格）；3：最新价',
                                "triggerProfitPrice": 0.0,//止盈触发价
                                "triggerStopPrice": 0.0,//止损触发价
                                "profitFixedLatest": {//最新设置的部分仓位止盈止损
                                  "profitId": 0,//止盈止损id
                                  "triggerPriceType": "",//触发价格类型 1、指数价格 2：标记价格（合理价格）；3：最新价',
                                  "triggerProfitPrice": 0.0,//止盈触发价
                                  "triggerStopPrice": 0.0//止损触发价
                                },
                                "profitFixedCount": 0,//部分仓位止盈止损总数
                                "isWelfareAccount": false,//是否是体验金账户
                                "closeProfit": 0.0,//平仓盈亏
                                "totalFee": 0.0,//手续费
                                "totalFundFee": 0.0,//资金费用
                                "reverseEntrustId": 0,//反手委托id
                                "reverseStopPrice": 0.0,//反手触发价格
                                "reverseTriggerPriceType": "",//反手触发价格类型
                                "contractSize": 0.0,//合约面值
                                "markPrice": 0.0,//标记价
                                "updatedTime": 0//更新时间
                              }
                            ]
                        }
        title: Response
        language: json
---
