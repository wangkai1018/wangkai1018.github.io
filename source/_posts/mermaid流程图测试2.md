---
title: mermaid流程图测试2
tags:
  - 第一个标签
  - 第二个标签
date: 2021-11-08 02:11:57
---
## 概要
在这里填写博客内容



```mermaid
graph TB
start(开始)-->inputA[输入用户名密码]
inputA-->opA{数据库查询子类}
opA-->conditionA{是否有此用户}
conditionA--yes-->conditionB{密码是否正确}
conditionA--no-->inputA
conditionB--yes-->opB[读入用户信息]
conditionB--no-->inputA
opB-->en(登录)
```

