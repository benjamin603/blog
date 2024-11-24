---
title: VSCode插件vs美化
tags: VSCode
categories: 软件工具
abbrlink: 29598
date: 2024-11-24 17:38:16
cover: https://r2.benjamin.xin/img/posts/569cdf1b00dc0736d44db3758dccece0.webp
---

作为目前主力开发以及编辑工具，VSCode每天都在使用，下面列举本人为了方便开发而使用安装的一些插件以及美化。

## 插件

### [Git Emoji Commit 中文版](https://marketplace.visualstudio.com/items?itemName=maixiaojie.git-emoji-zh)

在现代软件开发流程中，Git 已成为版本控制的主流工具，而良好的 Git 提交消息规范不仅能提升代码库的可读性，还能加强团队间的协作效率。Git Git Emoji Commit 中文版是一个专为中文开发者设计的 Git 提交信息增强工具，它提供了一套清晰易懂、富有表现力的 emoji 算法，以助于提升你的 Git 提交体验。

**BUG解决**

该软件目前有个BUG：

![20241124174424](https://r2.benjamin.xin/img/posts/20241124174424.png)

解决方案（Windows)：

1. 打开文件夹：`C:\Users\用户名\.vscode\extensions`，进入带插件名以及版本号的文件夹；
2. 打开并编辑`./out/extension.js`文件第23行左右；
3. 替换下面代码保存并重启 VSCode 即可：

查找：

```bash
 return repository.rootUri.path === uri._rootUri.path;
```

替换：

```bash
 return repository.rootUri.path === uri.rootUri.path;
```



