---
title: 短链接的解决方案
sticky: 1
tags: [link]
description:
categories: [link]
cover: https://rmt.ladydaily.com/fetch/hajeekn/storage/202204171137393.png
photos: https://rmt.ladydaily.com/fetch/hajeekn/storage/202204171137393.png
abbrlink: zroitiai
date: 2022-02-03 16:40:42
copyright_author_href: https://blog.slqwq.cn
author: Hajeekn
---

本文章首发于[语雀](https://www.yuque.com/ladjeek/ygg4q6)!
通过各种高科技功能同步到[Hajeekn 的博客](https://blog.slqwq.cn)
方便跳转,所以有了短链接,这篇文章带来短链接的几个解决方案

# GitHub issues + HTML(Free)

示例: [Click Me](https://to.slqwq.cn/apg/1)

## 实现方法

进入 [Shortener](https://service-dali9563-1259647411.sh.apigw.tencentcs.com/?link=4ey4iy4iy4my2cy1hy1hy4iy49y1gy4ly4ay4ny4hy4ny1gy45y48y1hy47y4my41y1hy24&hex=24&xor=6) 的仓库
Fork 仓库
然后部署到各种平台
以 CloudFlare 为例子
进入 [CloudFlare Dashbord](https://service-dali9563-1259647411.sh.apigw.tencentcs.com/?link=a0la4la4la8la7l55l38l38la4l96l37la7l97la9la3la9l37l92l95l38l94la8l89l38l49&hex=11&xor=6)
选择 'Pages'
选择![](https://rmt.ladydaily.com/fetch/hajeekn/storage/202204171138892.png#crop=0&crop=0&crop=1&crop=1&id=cERjd&originHeight=58&originWidth=124&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)
存储库选择 Fork 的仓库
然后一直下一步,等到部署完成就可以访问了

### 添加 DNS

如果你不想要 'pages.dev' 长地址,可以自定义域名
进入刚才部署好的项目的管理页面
选择自定义域
![](https://rmt.ladydaily.com/fetch/hajeekn/storage/202204171138465.png#crop=0&crop=0&crop=1&crop=1&id=oWzXr&originHeight=434&originWidth=937&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)
添加你的域名
接着做好 CNAME 解析即可

### issues 配置

新建一个 GitHub 仓库
存放你的 issues 数据
创建好后进入 issues 选项
![](https://rmt.ladydaily.com/fetch/hajeekn/storage/202204171138152.png#crop=0&crop=0&crop=1&crop=1&id=Axdg3&originHeight=433&originWidth=937&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)
选择 New issue
标题就写想要定向的网站
内容可以记录下 ID
创建好后 issues 的 id 就是重定向的钥匙
你创建了第一个 issues
你的重定向地址就是
域名/1
记录下仓库名备用

### 请求配置

进入 Fork 的仓库
编辑 404.html
![](https://rmt.ladydaily.com/fetch/hajeekn/storage/202204171139703.png#crop=0&crop=0&crop=1&crop=1&id=PAJmp&originHeight=98&originWidth=619&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)
在此处把/repos/**\***/issues/的\*\*\*\*改为你的用户名/仓库
然后提交
等待 CloudFlare 部署完成即可
ChenYFan 666
ChenYFan yyds
![](https://rmt.ladydaily.com/fetch/hajeekn/storage/202204171139358.gif#crop=0&crop=0&crop=1&crop=1&id=a2bhR&originHeight=108&originWidth=148&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)
