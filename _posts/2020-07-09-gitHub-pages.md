---
layout: post
title:  "GitHub Pages 构建自己的网站"
categories: Web
tags: 白嫖
author: jiobxn
---

* content
{:toc}

在历经wordpress之后，终究会选择简(bai)单(piao)

> 符合习惯  
> 简约稳定



## 创建站点

* [参考](https://pages.github.com/)

## 选择主题

* [这里](https://github.com/Gaohaoyang/gaohaoyang.github.io)

## 自定义域名
* **方式一** 在项目[Settings](https://docs.github.com/en/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site)

[![domain](https://jiobxn.files.wordpress.com/2020/07/github_domain.png?w=800&h=800)](https://jiobxn.files.wordpress.com/2020/07/github_domain.png)

查看源站IP

```
dig jiobxn.github.io +nostats +nocomments +nocmd
```

****

* **方式二** 使用反向代理

```
docker run -d --restart unless-stopped --network host -v /docker/www:/www -v /docker/logs:/var/log/nginx -v /docker/nginx:/key -e PROXY_SERVER="example.com,www.example.com|example.github.io^backend_https=y,alias=/filedownload|/www,log=Y,http2=Y" --name nginx jiobxn/nginx
```

****

* [白嫖3G床图空间](https://wordpress.com/?ref=footer_website)  
* [最好的CDN/DNS服务商](https://dash.cloudflare.com/)
