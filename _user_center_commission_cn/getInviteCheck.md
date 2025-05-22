---
title: 判断是否为邀请用户
position_number: 8
type: get
description: /v4/referal/invite/check
parameters:
  -
    name: uid
    type: number
    mandatory: true
    default:
    description: 用户ID
    ranges:
content_markdown: >-

left_code_blocks:
  -
    code_block: |-
      
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
        "mc": "SUCCESS",
        "ma": [],
        "result": false             //是否为邀请用户
      }
    title: Response
    language: json
---
