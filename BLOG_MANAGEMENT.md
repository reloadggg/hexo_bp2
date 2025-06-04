# 📝 Hexo博客维护操作文档 (升级版)

## 🚀 项目信息

- **Hexo版本**: 7.3.0 (最新版)
- **主题**: Diaspora
- **仓库地址**: https://github.com/reloadggg/hexo_bp2.git
- **网站地址**: https://reloadggg.github.io/hexo_bp2/
- **特色**: 保持原有内容和格式，升级到最新Hexo版本

## 🔄 在新电脑上设置博客环境

### 1. 环境准备

#### 1.1 安装必要软件
```bash
# 安装Node.js (推荐LTS版本)
# 从 https://nodejs.org/ 下载并安装

# 验证安装
node --version
npm --version

# 安装Git
# 从 https://git-scm.com/ 下载并安装

# 验证安装
git --version
```

#### 1.2 配置Git
```bash
# 设置用户信息
git config --global user.name "你的用户名"
git config --global user.email "你的邮箱"

# 配置GitHub认证（推荐使用Personal Access Token）
# 在GitHub Settings → Developer settings → Personal access tokens 创建token
```

### 2. 克隆博客仓库

```bash
# 克隆仓库到本地
git clone https://github.com/reloadggg/hexo_bp2.git
cd hexo_bp2

# 安装依赖
npm install
# 或者使用pnpm（推荐）
pnpm install
```

### 3. 验证环境

```bash
# 清理缓存
npx hexo clean

# 生成静态文件
npx hexo generate

# 启动本地服务器
npx hexo server

# 访问 http://localhost:4000/hexo_bp2/ 查看博客
```

---

## ✍️ 日常博客管理

### 1. 创建新文章

#### 1.1 基本创建命令
```bash
# 创建新文章
npx hexo new "文章标题"

# 创建草稿
npx hexo new draft "草稿标题"

# 创建页面
npx hexo new page "页面名称"
```

#### 1.2 文章模板示例
创建文章后，编辑 `source/_posts/文章标题.md`：

```markdown
---
title: 我的新文章
date: 2025-06-04 10:00:00
tags: [标签1, 标签2, 标签3]
categories: [分类名称]
description: 文章简短描述
---

# 文章标题

这里是文章内容...

## 二级标题

### 三级标题

- 列表项1
- 列表项2

**粗体文字**
*斜体文字*

```代码块```

> 引用内容

[链接文字](https://example.com)

![图片描述](/hexo_bp2/img/图片名.jpg)
```

### 2. 图片和资源管理

#### 2.1 图片存放
```bash
# 将图片放入source/img文件夹
# 在文章中引用：![描述](/hexo_bp2/img/图片名.jpg)
```

#### 2.2 Diaspora主题特色功能
- **封面图片**: 支持文章封面图片
- **音乐播放**: 支持背景音乐播放
- **图片画廊**: 支持PhotoSwipe图片浏览
- **一言功能**: 支持随机显示一言
- **响应式设计**: 完美适配移动设备

---

## 🔄 更新和发布流程

### 1. 本地预览

```bash
# 清理缓存
npx hexo clean

# 生成静态文件
npx hexo generate

# 启动本地服务器
npx hexo server

# 在浏览器访问 http://localhost:4000/hexo_bp2/ 预览
```

### 2. 发布到GitHub Pages

#### 2.1 提交源码
```bash
# 添加所有更改
git add .

# 提交更改
git commit -m "添加新文章：文章标题"

# 推送到GitHub
git push origin main
```

#### 2.2 部署到GitHub Pages
```bash
# 生成并部署
npx hexo clean
npx hexo generate
npx hexo deploy

# 或者一条命令
npx hexo clean && npx hexo g -d
```

### 3. 验证部署

访问 https://reloadggg.github.io/hexo_bp2/ 查看更新效果

---

## 🎨 Diaspora主题配置

### 1. 主题配置文件位置
- 主配置: `themes/diaspora/_config.yml`
- 自定义CSS: `themes/diaspora/source/css/diaspora.css`
- 自定义JS: `themes/diaspora/source/js/diaspora.js`

### 2. 常用配置项

#### 2.1 菜单配置
```yaml
# themes/diaspora/_config.yml
menu:
  首页: /
  分类: /categories
  标签: /tags
  归档: /archives  
  关于: /about
```

#### 2.2 封面图配置
```yaml
# 首页封面图
welcome_cover: /img/welcome-cover.jpg

# 默认文章封面图
cover: 
  - /img/cover.jpg
  - /img/welcome-cover.jpg
```

#### 2.3 社交链接配置
```yaml
links:
    facebook: /
    twitter: /
    github: /
    wechat: /img/logo.png
    email: mailto:xxxx@gmail.com
```

---

## 📋 常用命令速查

### Hexo命令
```bash
# 创建新文章
npx hexo new "标题"

# 生成静态文件
npx hexo generate
npx hexo g

# 启动本地服务器
npx hexo server
npx hexo s

# 部署
npx hexo deploy
npx hexo d

# 清理
npx hexo clean

# 组合命令
npx hexo clean && npx hexo g -d
```

### Git命令
```bash
# 查看状态
git status

# 添加文件
git add .

# 提交
git commit -m "提交信息"

# 推送
git push

# 拉取最新代码
git pull
```

---

## 🌟 项目特色

### 1. 技术升级
- ✅ **Hexo 7.3.0** - 最新稳定版本
- ✅ **Node.js兼容** - 支持最新Node.js版本
- ✅ **性能优化** - 更快的生成速度
- ✅ **安全更新** - 最新的安全补丁

### 2. 内容保持
- ✅ **原有文章** - 完整保留"前言"和"Hello World"文章
- ✅ **图片资源** - 所有原有图片资源
- ✅ **主题风格** - 保持Diaspora主题的视觉效果
- ✅ **配置设置** - 保持原有的网站配置

### 3. 部署优化
- ✅ **GitHub Pages** - 自动部署到gh-pages分支
- ✅ **CDN加速** - 利用GitHub的全球CDN
- ✅ **HTTPS支持** - 自动启用HTTPS
- ✅ **自定义域名** - 支持绑定自定义域名

---

*这是升级版的Hexo博客，在保持原有内容和风格的基础上，升级到了最新的技术栈！* 🚀
