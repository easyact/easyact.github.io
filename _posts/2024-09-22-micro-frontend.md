---
title: "What is SAASport?"
date: 2024-09-08
---
⼀⾏代码开启全端互联⽹SaaS计费⽀付。
# 效益
云计算和SaaS等类型企业的计费服务越来越复杂。自建成本也会增加。而且由于开发团队的领域偏好，计费服务往往被边缘化。并且由于计费的严肃性和繁琐性，导致计费领域的自动化一直不够完美，甚至妨碍运营。
因此作为微服务理念的延伸，SaaS成为一个强大的替代项。
# 安全
1. 仅仅共享用户id和昵称，而非用户详情。
2. 保密协议
# 技术架构
## Dashboard租户后台
Next.js
## Widget
React.js + Vite
## 支付API
Scala zio-lambda. Alipay 只提供Java SDK
## 价格API
APIGateway REST + lambda node