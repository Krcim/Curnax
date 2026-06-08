# Curnax统一链接管理 (Curnax-Link Manager)

## 简介

Curnax-Link Manager是一款轻量级的外链管理系统，专注于资源的上传、存储、管理与外链分发。采用纯 PHP + JSON 文件存储架构，无需 MySQL 数据库，部署简单，开箱即用。

适用于个人博客图床、小型站点静态资源托管、Markdown 写作配图管理、图文内容创作辅助等场景。

---

## 核心功能

### 📁 文件夹分类
- 支持多级文件夹组织图片，自由创建/重命名/删除文件夹
- 文件夹内图片数量实时统计

### 🔗 外链生成
- 一键生成直链，支持 Markdown / HTML / BBCode 多格式复制
- 批量勾选图片生成链接列表

### 🖼️ 缩略图缓存
- 列表视图提供缩略图预览（36×36）
- 支持选中/全量刷新缩略图缓存，存储于 Stock/ico 目录

### 📊 存储监控
- 仪表板展示缓存空间用量（Stock 目录）
- 下载临时目录监控（10240MB 上限，过期 48h 自动清理）
- 总图片数 & 总链接数实时统计

### 🔍 链接检测
- 批量检测外链有效性
- 标注失效链接，支持按状态筛选

### ⚡ 快速访问
- 自定义 URL 一键打开
- FTP 快速连接（支持保存配置）

### 🎨 主题自定义
- 登录页背景主题：默认/暗色/渐变可选
- 登录页背景图片自定义上传

### 👤 用户管理
- 管理员账号注册与密码修改
- 用户昵称自定义

### 📤 远程下载
- 支持粘贴远程图片 URL 批量下载到本地
- 下载进度实时反馈

---

## 技术架构

| 层级 | 技术 |
|------|------|
| 后端 | PHP 7.4+ |
| 存储 | JSON 文件 (data/*.json) |
| 前端 | 原生 HTML + CSS + JavaScript |
| 部署 | 任意 PHP 运行环境（宝塔 / Apache / Nginx） |

---

## 目录结构

```
pic-link-manager/
├── index.php          # 登录 / 注册页
├── dashboard.php      # 仪表板主页
├── user.php           # 用户管理
├── settings.php       # 系统设置
├── install.php        # 安装向导
├── config.php         # 全局配置
├── about.md           # 本说明文档
├── logo.ico           # 网站图标
├── api/               # API 接口
├── includes/          # 核心类库 (Auth / Storage)
├── data/              # JSON 数据存储
│   ├── users.json
│   ├── images.json
│   ├── links.json
│   ├── folders.json
│   └── settings.json
├── Stock/             # 缓存 & 临时文件
│   ├── ico/           # 缩略图缓存
│   ├── temp/          # 临时上传
│   └── down/          # 下载缓存
└── assets/            # 静态资源
```

---

## 开源计划

本项目开源至 GitHub，支持社区贡献与二次开发。

计划内容包括：
- 完善的 RESTful API 接口
- 插件系统支持
- Docker 一键部署
- 多用户权限体系
- 详细的开发者文档
- ------------------------------------------------------------------------------------------------------------
Curnax

English | "简体中文" (README.zh-CN.md)

«Manage assets once. Deliver everywhere.»

Curnax is an open-source media asset platform that helps you manage images, videos and files through a unified storage and delivery layer.
«Manage assets once. Deliver everywhere.»

Curnax is an open-source media asset platform that helps you manage images, videos and files through a unified storage and delivery layer.

Built for developers, creators and self-hosted environments.

---

Why Curnax?

Managing media assets across multiple storage providers and CDNs can quickly become complex.

Curnax provides a unified way to:

- Store assets in different storage providers
- Maintain stable public URLs
- Manage media resources from one place
- Integrate with existing websites and applications

---

Core Principles

Unified

Manage all assets from a single platform.

Portable

Move between storage providers without breaking URLs.

Open

Self-hosted and open-source.

Extensible

Designed for plugins, APIs and future integrations.

---

Planned Features

- Asset Management
- Multi-Storage Support
- Public URL Management
- CDN Integration
- WordPress Integration
- REST API
- Analytics

---

Supported Storage (Planned)

- AWS S3
- Cloudflare R2
- MinIO
- Aliyun OSS
- Tencent COS

---

Roadmap

v0.1

- Project initialization
- Core architecture
- Database design

v0.2

- Authentication
- Storage abstraction
- Asset upload

v0.3

- Public links
- Asset management

v1.0

- Multi-storage support
- Dashboard
- API

---

Status

🚧 Early Development

Curnax is currently under active development.

---

License

Apache License 2.0
