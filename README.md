# WeMark - 微信公众号文章导出神器 🚀

[![Version](https://img.shields.io/github/v/release/wechat-article/wemark?style=flat-square&logo=github)](https://github.com/wechat-article/wemark/releases)
[![License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](LICENSE)
[![Node.js](https://img.shields.io/badge/node-%3E%3D22-brightgreen?style=flat-square&logo=node.js)](https://nodejs.org/)
[![Nuxt](https://img.shields.io/badge/Nuxt-3.x-00DC82?style=flat-square&logo=nuxt.js)](https://nuxt.com/)
[![Electron](https://img.shields.io/badge/Electron-30.x-47848F?style=flat-square&logo=electron)](https://www.electronjs.org/)
[![Stars](https://img.shields.io/github/stars/wechat-article/wemark?style=flat-square)](https://github.com/wechat-article/wemark/stargazers)

> **一款基于 MITM + Nuxt 3 + Electron 的微信公众号内容抓取与导出工具**  
> 支持 HTML/JSON/Excel/TXT 多格式导出，100% 还原文章排版，批量获取阅读量、评论等运营数据

💬 欢迎交流：[才哥主页](https://www.caizhidao.cc)

### 🌐 多端部署方案
- **桌面应用** - Electron 跨平台打包 (Windows/macOS/Linux)
- **Web 服务** - Nuxt SSR/SSG 静态部署
- **Docker 容器** - 一键启动，开箱即用
- **Cloudflare Workers** - Serverless 边缘计算部署

---

## 📸 软件截图

### 主界面 - 软件说明
![软件说明](screenshots/software-info.png)

### 公众号管理
![公众号管理](screenshots/account-management.png)

### 文章下载
![文章下载](screenshots/article-download.png)

### 数据导出
![数据导出](screenshots/data-export.png)
![数据导出1](screenshots/data-exprot1.png)

### 效果展示
![效果展示](screenshots/html-result.png)
![效果展示1](screenshots/pdf-result.png)
---

## 🛠️ 技术栈

## ✨ 核心特性

### 🔍 智能搜索与采集
- **公众号模糊搜索** - 支持关键字快速定位目标账号
- **全量文章爬取** - 突破微信接口限制，批量获取历史文章
- **合集/专辑下载** - 一键下载整个专题内容
- **多媒体支持** - 自动捕获图片、视频分享消息

### 📊 数据深度挖掘
- **运营指标导出** - 阅读量、点赞数、转发量、在看数
- **评论数据采集** - 支持主评论及回复层级关系
- **元信息完整保留** - 发布时间、作者、原创标识、所属合集

### 🎨 完美格式还原
- **HTML 像素级还原** - 内联样式 + 资源打包，离线浏览无差异
- **多格式导出** - HTML / JSON / Excel / TXT / Markdown
- **样式隔离渲染** - Shadow DOM 技术避免全局污染
- **代码高亮支持** - 内置 Monaco Editor，支持语法高亮

### ⚡ 高性能架构
- **并发控制** - P-Queue 实现智能请求队列
- **增量缓存** - IndexedDB (Dexie) 本地持久化，减少重复请求
- **断点续传** - 大文件下载支持中断恢复
- **代理池管理** - 支持公共/私有代理配置

### 🔐 安全认证机制
- **MITM 抓包** - 自动化拦截微信登录凭证
- **Cookie 会话管理** - 多账号隔离，Token 自动刷新
- **扫码登录** - 官方 OAuth 流程，无需输入密码
- **凭证加密存储** - 敏感信息安全落地

### 🌐 多端部署方案
- **桌面应用** - Electron 跨平台打包 (Windows/macOS/Linux)
- **Web 服务** - Nuxt SSR/SSG 静态部署
- **Docker 容器** - 一键启动，开箱即用
- **Cloudflare Workers** - Serverless 边缘计算部署

---

## 🛠️ 技术栈

| 分类 | 技术选型 |
|------|---------|
| **前端框架** | [Nuxt 3](https://nuxt.com/) + [Vue 3](https://vuejs.org/) + TypeScript |
| **桌面端** | [Electron](https://www.electronjs.org/) + electron-updater |
| **UI 组件** | [@nuxt/ui](https://ui.nuxt.com/) + TailwindCSS |
| **数据表格** | [AG Grid Enterprise](https://www.ag-grid.com/) |
| **状态管理** | [Pinia](https://pinia.vuejs.org/) |
| **本地数据库** | [Dexie.js](https://dexie.org/) (IndexedDB Wrapper) |
| **HTTP 客户端** | [ofetch](https://github.com/unjs/ofetch) |
| **文件处理** | [ExcelJS](https://github.com/exceljs/exceljs) · [JSZip](https://stuk.github.io/jszip/) · [html-docx-js](https://github.com/evidenceprime/html-docx-js) |
| **HTML 解析** | [Cheerio](https://cheerio.js.org/) · [Turndown](https://domchristie.github.io/turndown/) |
| **代码编辑** | [Monaco Editor](https://microsoft.github.io/monaco-editor/) |
| **中间人代理** | [mitmproxy](https://mitmproxy.org/) |
| **浏览器自动化** | [Puppeteer](https://pptr.dev/) |
| **错误监控** | [Sentry](https://sentry.io/) |
| **数据校验** | [Zod](https://zod.dev/) |


## 📖 使用指南

### 1. 账号登录

1. 进入「账号管理」页面
2. 点击「扫码登录」按钮
3. 使用微信扫描弹出的二维码
4. 等待认证成功提示

### 2. 搜索公众号

在搜索框输入公众号名称或关键词，系统会实时返回匹配结果。

### 3. 批量导出文章

1. 选择目标公众号
2. 设置过滤条件（时间范围、原创标识、合集标签）
3. 勾选需要导出的文章
4. 选择导出格式（推荐 HTML 以保留完整样式）
5. 点击「开始下载」