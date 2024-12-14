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

## S3 + CloudFront
## AWS codebuild + codepipeline
这是最低基础设施和开发成本的选项。
虽然没有很酷的yml IaC代码，但是管道并不需要频繁地重建。
因此IaC的调试成本并没有很好的ROI。
手工搭建的管道的最大缺陷也就是新人很难通过代码了解管道的全貌。

# 服务端架构

