---
title: mermaid流程图测试2
tags:
  - 第一个标签
  - 第二个标签
date: 2021-11-08 02:11:57
---
## 概要
在这里填写博客内容



```flow
st=>start: Start
op=>operation: 王凯
cond=>condition: Yes or No?
e=>end

st->op->cond
cond(yes)->e
cond(no)->op
```
```sequence
participant Client
participant Server

Note left of Client:SYN_SENT
Client->Server:SYN=1 seq=x
Note right of Server:SYN_RCVD
Server->Client:SYN=1 seq=y ACK=x+1
Note left of Client:ESTABLISHED
Client->Server:ACK=y+1
Note right of Server:ESTABLISHED
```

