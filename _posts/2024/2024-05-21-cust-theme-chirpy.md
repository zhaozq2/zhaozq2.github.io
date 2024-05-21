---
title:      "利用chirpy主题搭建个人博客的过程"
date:       2024-05-21
categories: [blog]
tag: [chirpy, 个人博客]
math: true
description: 使用chirpy搭建个人博客的详细过程.
comments: true
---
## 1. 前言
这几天一直在搭建自己的个人博客，经过几天的努力，我的个人博客[zhaozq2的博客](https://zhaozq2.github.io/)也终于和大家见面了,欢迎大家来访，也请大家多提宝贵意见。

搭建过程经历初步熟悉，寻找确定主题，自定义主题三个阶段，我把整个过程记录下，一方面是自己的总结，另一方面也方便大家搭建自己博客参考
## 2.步骤
1. 确认技术 github Pages和Jekyll
2. 注册[Github](https://github.com/) 帐号
3. 通过[阮一峰 搭建一个免费的，无限流量的Blog](https://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html)初步体验建博过程
4. 选择符合自己的博客主题，可从[Jekyll 主题资源](https://jekyllrb.com/resources/)选择，也可从[Github](https://github.com/)寻找
5. 确实主题 我选择使用[chirpy](https://github.com/cotes2020/jekyll-theme-chirpy) 作为个人博客主题
6. 定制化主题。
## 3.增加评论区
 评论区，模板作者已经将相关功能封装好了，目前支持disqus | utterances | giscus三种，在 _config.yml 文件中填上个人信息即可，我选择使用giscus.
 giscus 配置过程详见[giscus](https://giscus.app/zh-CN),根据流程一部分一部分来即可
 ## 4.增加站点统计
   使用[不蒜子](https://busuanzi.ibruce.info/)进行UV,PV统计分两步
   1. 直接将_includes/footer.html文件拷贝到你的代码项目对应的位置，在文件中间插入
   ```html
   <p> 
  {% include footer-busuanzi.html %}
</p>
   ```
   2. 新建_includes/footer-busuanzi.html，写入内容
   ```html
   <script async src="//busuanzi.ibruce.info/busuanzi/2.3/busuanzi.pure.mini.js"></script>
    <span id="busuanzi_container_site_pv">本站总访问量<span id="busuanzi_value_site_pv"></span>次</span>
   ```
 ## 5.修改 favicons
 assets/favicons/下创建各种png，ico文件。具体可以根据[教程](https://chirpy.cotes.page/posts/customize-the-favicon/)创建，然后拷贝到对应位置 
