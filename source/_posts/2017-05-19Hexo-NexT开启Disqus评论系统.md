---
title: Hexo-NexT开启Disqus评论系统
comments: ture
category:
  - hexo
  - next
tag:
  - hexo
abbrlink: 4c30fb3d
data: 2017-05-19 00:00:00
updated:
---



Hexo-NexT开启Disqus评论系统

<!--more-->

1. 到[disqus](https://disqus.com)官网注册账号并登陆，可使用facebook、twitter、google账号登录。
   选择你注册账号的用途，这里我们选`I want to install disqus on my site`
   ![disqus-signup](C:\Users\wolfydw\blog\source\_posts\2017-05-19Hexo-NexT开启Disqus评论系统\disqus-signup.jpg)
   填写你网站的相关信息
   ![disqus-signup1](C:\Users\wolfydw\blog\source\_posts\2017-05-19Hexo-NexT开启Disqus评论系统\disqus-signup1.jpg)
   选择付费套餐，这里当然是选择免费的`Basic`了
   ![disqus-signup2](C:\Users\wolfydw\blog\source\_posts\2017-05-19Hexo-NexT开启Disqus评论系统\disqus-signup2.jpg)

   之后的就不用选择了，已经可以使用了
2. 编辑`主题配置文件`

```
disqus:
  enable: ture   # 开启disqus
  shortname:     # 你刚注册的disqus用户名
  count: false   # 开启评论数量显示
```

