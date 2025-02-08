---
title: "GithubPages个人博客创建指南"
excerpt: "如何简单快捷地利用GitHubPages创建个人博客"
header:
  overlay_image: /assets/images/post-banner.jpg

  overlay_filter: 0.5
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
categories:
  - 技术
tags:
  - GithubPages
  - Jekyll
  - Minimal Mistakes
  - 个人博客

toc: true
toc_sticky: true
classes: wide centered
gallery:
  - url: /assets/images/unsplash-gallery-image-1.jpg
    image_path: /assets/images/unsplash-gallery-image-1-th.jpg
    alt: "placeholder image 1"
    title: "Image 1 title"
  - url: /assets/images/unsplash-gallery-image-2.jpg
    image_path: /assets/images/unsplash-gallery-image-2-th.jpg
    alt: "placeholder image 2"
    title: "Image 2 title"
--- 

# 使用 GitHub Pages、Jekyll 和 Minimal Mistakes 创建个人博客的详细指南

## 一、准备工作

1. **注册 GitHub 账号**
   - 如果你还没有 GitHub 账号，前往 [GitHub 官网](https://github.com) 进行注册
   - 按照提示填写用户名、邮箱和密码等信息

2. **安装 Git**
   - Git 是一个分布式版本控制系统，用于与 GitHub 进行交互
   - 前往 [Git 官网](https://git-scm.com/) 下载适合你操作系统的安装包
   - 安装过程中保持默认设置即可
   - 安装完成后，在命令行中输入 `git --version` 检查是否安装成功

## 二、了解 GitHub Pages

GitHub Pages 是 GitHub 提供的静态网站托管服务。你可以通过它将存储在 GitHub 仓库中的文件以网页的形式展示出来。它支持多种静态网站生成器，其中 Jekyll 是 GitHub 官方推荐的。

## 三、安装 Jekyll

1. **安装 Ruby**
   - Jekyll 基于 Ruby 语言开发，需要先安装 Ruby
   - Windows：通过 [RubyInstaller](https://rubyinstaller.org/) 下载安装包
   - Mac：使用 [Homebrew](https://brew.sh/) 安装，命令为 `brew install ruby`
   - 安装完成后，在命令行输入 `ruby -v` 检查安装版本

2. **安装 Jekyll 和 Bundle**
   ```bash
   gem install jekyll bundler
   jekyll -v  # 检查 Jekyll 版本
   bundle -v  # 检查 Bundle 版本
   ```

## 四、选择并下载 Minimal Mistakes 主题

1. **找到 Minimal Mistakes 仓库**
   - 在 [GitHub](https://github.com) 上搜索 Minimal Mistakes
   - 进入其官方仓库页面

2. **下载仓库**
   - 点击绿色的 "Code" 按钮
   - 选择 "Download ZIP" 下载整个仓库的压缩包
   - 下载完成后解压到你方便操作的文件夹

## 五、初始化项目并配置

1. **进入解压后的文件夹**
   ```bash
   cd ~/Desktop/minimal-mistakes  # 示例路径
   ```

2. **安装依赖**
   ```bash
   bundle install
   ```

3. **配置 `_config.yml` 文件**
   ```yaml
   title: 你的博客标题
   description: 你的博客描述
   author: 你的名字
   ```

## 六、创建并发布到 GitHub Pages

1. **在 GitHub 上创建新仓库**
   - 登录 GitHub，点击页面右上角的 "+" 号
   - 选择 "New repository"
   - 仓库名为 `你的用户名.github.io`

2. **将本地项目关联到 GitHub 仓库**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/你的用户名/你的用户名.github.io.git
   git push -u origin master
   ```

3. **等待部署并访问博客**
   - GitHub 会自动检测到项目中的 Jekyll 文件并进行部署
   - 部署完成后，访问 `https://你的用户名.github.io`

## 七、日常使用与更新

1. **本地修改与测试**
   ```bash
   bundle exec jekyll serve  # 启动本地服务器
   # 在浏览器中访问 http://127.0.0.1:4000 查看效果
   ```

2. **同步到 GitHub**
   ```bash
   git add .
   git commit -m "你的修改说明"
   git push origin master
   ```

---

以上就是利用 GitHub Pages、Jekyll 和 Minimal Mistakes 创建个人博客的全部步骤。如果你在操作过程中有任何疑问，比如遇到安装错误、配置文件修改不生效等问题，都可以随时跟我说，我帮你一起解决。
