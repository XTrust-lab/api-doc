---
title: 获取用户当前跟随的交易员列表
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
                            "leaderName": "",//带单员name
                            "leaderAccountId": "",//带单员accountId
                            "leaderUserId": "",//带单员userId
                            "subAccountId": 0,//智能跟单子账号
                            "avatar": "",//头像
                            "followMode": "",//跟随模式:CUSTOM,AUTO
                            "startTime": 0,//跟单开始时间
                            "endTime": 0,//跟单结束时间
                            "followAmount": 0.0,//智能跟单净跟单金额
                            "followVal": 0.0,//custom 跟单数量
                            "followType": "",//custom 跟单方式
                            "followMargin": 0.0,//custom 跟随本金
                            "profit": 0.0,//已结盈亏
                            "divideProfit": 0.0,//分润支出
                            "divideRate": 0.0,//分润比例
                            "orderList": [//汇总/当前跟单
                              {
                                "symbol": "",//交易对
                                "symbolName": "",//交易对
                                "positionType": "",//仓位类型:CROSSED(全仓);ISOLATED(逐仓)
                                "positionSide": "",//持仓方向:LONG;SHORT
                                "openLeverage": 0,//杠杆
                                "id": 0,
                                "leaderAccountId": "",//交易员 accountId
                                "accountId": 0,//跟随者账号 id
                                "orderId": 0,//订单 id
                                "trackNo": 0,//跟单trackNo
                                "openTime": 0,//开仓时间
                                "closeTime": 0,//平仓时间
                                "openPrice": 0.0,//开仓均价
                                "closePrice": 0.0,//平仓均价
                                "openMargin": 0.0,//开仓初始保证金
                                "realizedPnl": 0.0,//已实现盈亏
                                "profitRate": 0.0,//收益率,已乘100。
                                "openSize": 0.0,//开仓仓位数量
                                "closeSize": 0.0,//平仓仓位数量(已平仓位数量)
                                "positionSize": 0.0,//持仓数量
                                "closeOrderSize": 0.0,//平仓订单占用
                                "availableCloseSize": 0.0,//可平数量
                                "profitId": 0,//止盈止损id
                                "triggerPriceType": "",//触发价格类型 1、指数价格 2：标记价格（合理价格）；3：最新价',
                                "triggerProfitPrice": 0.0,//止盈触发价
                                "triggerStopPrice": 0.0,//止损触发价
                                "contractType": "",//合约类型：PERPETUAL(永续合约)、PREDICT(预测合约)
                                "entryPrice": 0.0,//开仓均价
                                "openOrderSize": 0.0,//开仓订单占用
                                "isolatedMargin": 0.0,//逐仓保证金
                                "openOrderMarginFrozen": 0.0,//开仓订单保证金占用
                                "realizedProfit": 0.0,//已实现盈亏
                                "autoMargin": false,//是否自动追加保证金
                                "leverage": 0,//杠杆倍数
                                "closeProfit": 0.0,//平仓盈亏
                                "totalFee": 0.0,//手续费
                                "totalFundFee": 0.0//资金费用
                              }
                            ]
                          }
                        ]
                    }
        title: Response
        language: json
---
