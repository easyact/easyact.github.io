---
title: "SAASport widget设计"
date: 2024-11-03
---

# 客户集成

只需在html页面中加入下面的代码。

    <script src="https://easyact.cn/widget/widget.js"/>
    <div className="container" id="saasport" tenant="SAASport.cn"></div>

# 客户端、widget

React + Vite

## 托管：S3 + CloudFront

低延迟，配额内免费，配额外依据流量付费。

## AWS codebuild + codepipeline

这是最低基础设施和开发成本的选项。
虽然没有很酷的yml IaC代码，但是管道并不需要频繁地重建。
因此IaC的调试成本并没有很好的ROI。
手工搭建的管道的最大缺陷也就是新人很难通过代码了解管道的全貌。

# 服务端架构

APIGateway与Lambda的组合同样是低延迟，配额内免费，
并且是可伸缩的，并行化，高弹性的。

但是Lambda的冷启动问题还没有妥善解决。
导致长期闲置后，会有短时间的服务离线。

由两个微服务组成：
1. 租户信息获取：使用常规nodejs lambda
2. 支付：使用ZIO框架编译成jdk native image的lambda
