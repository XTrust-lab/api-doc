---
title: Check If The User Is Invited
position_number: 8
type: get
description: /v4/referal/invite/check
parameters:
  -
    name: uid
    type: number
    mandatory: true
    default:
    description: user ID
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
        "result": false             //is invited
      }
    title: Response
    language: json
---
