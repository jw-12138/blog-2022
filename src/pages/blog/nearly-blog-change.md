---
title: 博客近期的变化
layout: '../../layouts/Post.astro'
tags: blog
date: 2019-06-11
---

### 图片 CDN 迁移到了阿里云

从上个月开始，博客的图片全部无法显示，原因是新浪微博开始防盗链了。

起初选择使用新浪微博的图床，一方面是因为不用花钱，另一方面是因为觉得自己的博客没有多少访问量，也就不折腾 CDN 了。然而这一两年我意识到，我认真写下的文字也被不少人在认真看待。趁着这个契机，就把博客的图片全部迁移到稳定的 CDN 上。

我选择了[阿里云 OSS + CDN 的方案](/link/aliyun)，我用 grep 把博客里所有的新浪图床图片找了出来，然后批量下载下来，上传到 OSS 上。

比较麻烦的是国内的 CDN 域名需要备案，除此之外，就是阿里云的一条龙服务 —— 域名可以绑定到 CDN，CDN 可以直接关联 OSS。体验还算不错。

### 全站 Cloudflare

Coding Page 的 Pages 服务在香港的腾讯云，抽风是家常便饭，无法忍受。于是接入了 Cloudflare, 现在你访问的这里就是经过 Cloudflare 加速的页面。
