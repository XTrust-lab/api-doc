---
title: 获取用户阶梯费率
position_number: 8
type: get
description: /future/user/v1/user/step-rate
parameters:
    -
content_markdown: |-

               #### **限流规则**

               200/s/apikey
left_code_blocks:
    -
        code_block: "public void getStepRate() {\r\n\tString text = HttpUtil.get(URL + \"/future/user/v1/user/step-rate\");\r\n\tSystem.out.println(text);\r\n}"
        title: Java
        language: java
right_code_blocks:
    - code_block: |-
        {
          "error": {
            "code": "",
            "msg": ""
          },
          "msgInfo": "success",
          "result": {
                "specialType": false, // 是否是特殊帐号
                "vipProType": true, // 是否是专业费率
                "stepRateProName": "VIP_PRO_1", // 专业费率名称
                "discountLevel": 2, // 折扣等级
                "makerFee": "0.0015", // maker费率
                "takerFee": "0.0025", // taker费率
                "levelReturnDay": 30, // 当前等级保留天数
                "totalTradeVolume": "1250000.50", // 近29天+今天, 交易量(10分钟更新)
                "uBasedTotalTradeVolume": "850000.75", // 近29天+今天, U本位交易量
                "coinBasedTotalTradeVolume": "400000.25", // 近29天+今天, 币本位交易量
                "walletBalance": "50000.00", // 账户权益(USDT, 10分钟更新）：钱包余额+未实现盈亏
                "notProfit": "1250.50", // 仓位未实现盈亏(USDT, 10分钟更新)
                "nextLvTradeVolume": "1500000.00", // 下一个等级交易量
                "lackTradeVolume": "250000.50", // 下一个等级相差的交易量
                "nextLvWalletBalance": "75000.00", // 下一个等级钱包余额
                "lackWalletBalance": "25000.00", // 下一个等级相差的钱包余额
                "nextLvMakerFee": "0.0010", // 下一个等级Maker费率
                "nextLvTakerFee": "0.0020" // 下一个等级Taker费率
          },
          "returnCode": 0
        }
      title: Response
      language: json
---
