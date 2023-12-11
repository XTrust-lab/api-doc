---
title: Transactions
position_number: 9
type:
description: 

parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
  subscribe:
  ```js
    {
       "method": "SUBSCRIBE/UNSUBSCRIBE",
       "params": [
           "{trade}@{listenKey}",
        ],
       "id": "{id}"
    }
  ```

left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
            {
                "topic": "trade", 
                "event": "trade@123456", 
                "data": {
                        "orderId":"12312312",  // Order ID
                        "price":"34244",  // Price
                        "quantity":"123", // Quantity
                        "marginUnfrozen":"123", // Quantity of unfrozen margin
                        "timestamp":1731231231 // Timestamp
                   }
            }
        title: Response
        language: json
---
