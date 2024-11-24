---
title: Hexo托管至Cloudflare
abbrlink: 34862
date: 2024-11-24 16:29:22
tags:
  - Hexo
  - Cloudflare
categories: 博客记录
cover: https://r2.benjamin.xin/img/posts/121a43bdac3a64ed8fae7f5e34054a58.png
---

## 托管到 Github

- 创建仓库 | Create a new repository
- 本地项目推送到远程服务器

```bash
git init
git add .
git commit -m "my blog first commit"
git remote add origin git@github.com:【你的 github 名字】/【你的 repository 名字】.git
git push -u origin master
```

# 部署到 Cloudflare

登录 Cloudflare 进入控制台页面，找到 Workers 和 Pages 并点击创建应用程序，选择 Pages ，然后选择链接到 Git

![20241124164001](https://r2.benjamin.xin/img/posts/20241124164001.png)

然后选自存储你 Hexo 项目的仓库

![20241124164051](https://r2.benjamin.xin/img/posts/20241124164051.png)

部署构建项目

使用命令：`npm install -g hexo; hexo clean; hexo generate`

构建输出命令：`public`

![20241124164334](https://r2.benjamin.xin/img/posts/20241124164334.png)

构建完成后，你就可以使用 cf 生成的 `pages.dev` 二级域名来访问自己的博客了

![20241124170623](https://r2.benjamin.xin/img/posts/20241124170623.png)

**注意：自定义域名需要你拥有一个自己的域名，同时这个域名必须由 Cloudflare 托管**

