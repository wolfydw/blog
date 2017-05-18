---
title: Hexo-NexT开启Disqus评论系统
data: 2017/5/19
category: [hexo]
tag: [hexo]
---



# Hexo-NexT开启Disqus评论系统

1. 到[disqus](https://disqus.com)官网注册账号并登陆，可使用facebook、twitter、google账号登录。
   选择你注册账号的用途，这里我们选`I want to install disqus on my site`
   ![disqus-signup](disqus-signup.jpg)
   填写你网站的相关信息
   ![disqus-signup1](disqus-signup1.jpg)
   选择付费套餐，这里当然是选择免费的`Basic`了
   ![disqus-signup2](disqus-signup2.jpg)

   之后的就不用选择了，已经可以使用了
2. 编辑`主题配置文件`

```
disqus:
  enable: ture   # 开启disqus
  shortname:     # 你刚注册的disqus用户名
  count: false   # 开启评论数量显示
```

