---
title: Get User's Step Rate
position_number: 8
type: get
description: /future/user/v1/user/step-rate
parameters:
    -
content_markdown: |-
  
              #### **Limit Flow Rules**

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
                      "specialType": false, // Is special account
                      "vipProType": true, // Is professional rate
                      "stepRateProName": "VIP_PRO_1", // Professional rate name
                      "discountLevel": 2, // Discount level
                      "makerFee": "0.0015", // Maker fee rate
                      "takerFee": "0.0025", // Taker fee rate
                      "levelReturnDay": 30, // Current level retention days
                      "totalTradeVolume": "1250000.50", // Trading volume in the past 29 days + today (updated every 10 minutes)
                      "uBasedTotalTradeVolume": "850000.75", // USDT-margined trading volume in the past 29 days + today
                      "coinBasedTotalTradeVolume": "400000.25", // Coin-margined trading volume in the past 29 days + today
                      "walletBalance": "50000.00", // Account equity (USDT, updated every 10 minutes): wallet balance + unrealized profit and loss
                      "notProfit": "1250.50", // Position unrealized profit and loss (USDT, updated every 10 minutes)
                      "nextLvTradeVolume": "1500000.00", // Next level trading volume
                      "lackTradeVolume": "250000.50", // Trading volume needed for next level
                      "nextLvWalletBalance": "75000.00", // Next level wallet balance
                      "lackWalletBalance": "25000.00", // Wallet balance needed for next level
                      "nextLvMakerFee": "0.0010", // Next level maker fee rate
                      "nextLvTakerFee": "0.0020" // Next level taker fee rate
                  },
          "returnCode": 0
        }
      title: Response
      language: json
---
