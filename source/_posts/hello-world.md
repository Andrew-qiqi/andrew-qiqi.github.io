---
title: Hello World
---
Welcome to [Hexo](https://hexo.io/)! This is your very first post. Check [documentation](https://hexo.io/docs/) for more info. If you get any problems when using Hexo, you can find the answer in [troubleshooting](https://hexo.io/docs/troubleshooting.html) or you can ask me on [GitHub](https://github.com/hexojs/hexo/issues).

## Quick Start

### Create a new post

``` bash
$ hexo new "My New Post"
```

More info: [Writing](https://hexo.io/docs/writing.html)

### Run server

``` bash
$ hexo server
```

More info: [Server](https://hexo.io/docs/server.html)

### Generate static files

``` bash
$ hexo generate
```

More info: [Generating](https://hexo.io/docs/generating.html)

### Deploy to remote sites

``` bash
$ hexo deploy
```

More info: [Deployment](https://hexo.io/docs/one-command-deployment.html)

---
# 🚀 Andrew's Blog 维护指南

这是我的 Hexo 博客源码仓库。为了实现 Win & Mac 多设备同步，请务必遵循以下“双轨”操作流程。

---

## 📅 日常写作流程

### 1. 同步云端进度 (开工前)
在开始写博客之前，拉取另一台设备的最新原稿：
- 执行命令：`git pull origin source`
- 或在 VS Code 点击左下角 **刷新图标**。

### 2. 本地预览
- 生成并启动：`hexo s`
- 预览地址：[http://localhost:4000](http://localhost:4000)

### 3. 发布网页 (让读者看到)
在终端依次执行（Windows 用户建议分开执行）：
1. `hexo clean` (清理缓存)
2. `hexo g`     (生成静态文件)
3. `hexo d`     (部署到 main 分支)

### 4. 备份源码 (让另一台电脑能接着写)
**这是最重要的步骤！** 只有完成这一步，你的 Markdown 原稿才会同步：
- 进入 VS Code **Source Control (Git)** 面板。
- 输入 Commit 信息（如 "update: 新增文章"）。
- 点击 **Commit**，然后点击 **Sync Changes** 推送到 `source` 分支。

---

## ⚠️ 注意事项
- **分支说明**：`source` 分支存原稿，`main` 分支由 Hexo 自动部署（切勿手动修改 main）。
- **图片处理**：建议使用图床，保持仓库体积轻量。
- **环境一致**：Win/Mac 建议安装相同版本的 Node.js。

## 🔍 解释
1. 修改博客后，用hexo clean ; hexo g ; hexo d后，github上的main分支中的网页会更新，但是source还没更新
2. 然后在vscode上用commit和Sync Changes后，source才会更新