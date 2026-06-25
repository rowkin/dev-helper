# DevHelper - 七九在线科技开发者工具箱

> 一款专为七九在线科技打造的 Chrome 浏览器扩展，集成 JSON 格式化、编解码、API 调试、代码格式化等 16 个常用开发工具，并内置 **AI 解读** 和独立 **AI 助手**，让开发效率飞升。

[![Chrome Extension](https://img.shields.io/badge/Chrome-Extension-blue?logo=googlechrome)](https://github.com/rowkin/dev-helper)
[![Manifest V3](https://img.shields.io/badge/Manifest-V3-green)](https://developer.chrome.com/docs/extensions/mv3/)

---

## ✨ 功能特性

### 🛠️ 开发工具（16 个工具）

| 工具 | 功能描述 | AI 集成 |
| :--- | :--- | :--- |
| **JSON 格式化** | 美化/压缩/校验/转义 JSON | ✅ AI 解读结构 |
| **编解码工具** | URL / Base64 / Unicode / HTML 实体 | ✅ AI 自动识别 |
| **JWT 解析** | 三段拆分、有效期检测、载荷分析 | ✅ AI 安全分析 |
| **时间戳转换** | 实时时钟、双向转换、世界时区 | ✅ AI 解读 |
| **API 调试** | 轻量 Postman，支持 Headers/Body/Params | ✅ AI 分析响应 |
| **代码格式化** | JS/CSS/HTML/JSON/SQL 格式化 | ✅ AI 读代码 |
| **正则测试** | 实时匹配、标志位、常用正则速查 | ✅ AI 解读正则 |
| **UUID 生成器** | UUID v4 / NanoID / 雪花 ID 批量生成 | ✅ AI 讲解 |
| **密码生成器** | 强密码生成、强度评估、可配置规则 | ✅ AI 安全建议 |
| **哈希计算** | MD5 / SHA-1 / SHA-256 / SHA-512 | ✅ AI 解读 |
| **颜色转换** | HEX / RGB / HSL / HSV 互转，取色器 | — |
| **二维码工具** | 生成/解码二维码，自定义样式 | — |
| **JSON 对比** | 两段 JSON 差异可视化对比 | ✅ AI 解读差异 |
| **进制转换** | 2~36 进制数字互转 | — |
| **图片 Base64** | 图片与 Base64 互转 | — |
| **Markdown 编辑器** | GFM 语法、Mermaid 图表渲染、双栏同步滚动 | ✅ AI 辅助写作 |

### 🤖 AI 助手与双栏架构

- **精美双栏主页**：全景导航页重构为 70/30 双栏黄金比例，左侧显示全景工具，右侧为常驻的 **AI 助手** 聊天窗口与 **AI 就绪卡片**。
- **快捷模型切换**：右侧 AI 聊天面板头部直接提供模型下拉框，可随时在 `🤖 Chrome 内置 AI` 和 `🌐 自定义 API` 之间一键切换。
- **环境自动检测与轮询下载安装**：
  - 如果未检测到 Chrome 内置 AI (Gemini Nano) 所需的 Flags 选项或尚未下载模型（`downloadable` 状态），系统不仅提供针对性的 Flags/Components 一键跳转引导，还会自动将模型组件名复制至剪贴板供用户查找。
  - 点击“下载并激活”后，后台会自动以 2.5 秒的频率启动轮询检测，直到 Gemini Nano 模型下载完毕并变为 `available`，此时将自动完成状态激活、模型切换并提示。
- **AI 解读 Markdown 渲染**：聊天内容完美支持代码块高亮、标题及列表的 Markdown 流式渲染。

---

## 🚀 安装使用

### 方法一：Chrome Web Store 商店安装（首选推荐 🌟）

可以直接在 Chrome 网上应用店一键安装，省去手动下载解压的步骤，并支持自动后台更新与云端配置同步：
👉 [**前往 Chrome Web Store 安装 DevHelper**](https://chromewebstore.google.com/detail/dobgahhmdodeeondedoikibehhmnalie)

### 方法二：下载发布包手动加载安装（离线/开发者模式）

1. 访问对外发布仓库 [dev-helper/releases](https://github.com/rowkin/dev-helper/releases) 下载最新的打包 ZIP 压缩包并解压。
2. 打开 Chrome，在地址栏输入 `chrome://extensions` 并回车。
3. 启用右上角的 **「开发者模式」**。
4. 点击左上角的 **「加载已解压的扩展程序」**。
5. 选择解压出的 `dev-helper` 文件夹目录。

### 💡 快捷键

安装后可使用 `Alt+Shift+D` 快速打开 DevHelper（Mac 同样适用）。

---

## ⚙️ AI 配置

点击插件内任意工具页面右上角 **「AI 设置」** 按钮：

### Chrome 内置 AI（Gemini Nano）

- 需要 Chrome 127+ 版本。
- 首次使用可能需要下载模型。
- 完全本地运行，无需 API Key。

### 自定义 OpenAI 兼容接口

```text
API URL: https://api.openai.com/v1/chat/completions
API Key: sk-xxxx
模型名称: gpt-4o-mini
```

支持任何 OpenAI Chat Completions 兼容服务（例如火山引擎 Coding Plan Lite 等国内大模型代理）。

---

## 🎨 设计理念

- **明亮与暗色多主题支持**：主页面和工具页卡片完美适配明亮（Light）与暗色（Dark）主题模式，并支持一键切换。
- **双栏常驻工作流**：将 AI 聊天框和就绪卡片固定在右侧，在阅读或处理左侧工具时可随时进行 AI 辅助对话。
- **隐私安全**：普通工具完全本地处理；AI 功能仅在用户配置并主动发起时调用。

---

## 🔒 权限说明

| 权限 | 用途 |
| :--- | :--- |
| `tabs` | 在新标签页打开工具 |
| `storage` | 保存 AI 配置、收藏、使用记录 |
| `activeTab` | 获取当前页面信息（API 调试） |
| `scripting` | 注入内容脚本（必要时） |
| `clipboardWrite` | 支持一键复制功能 |

无网络请求权限（除用户主动触发的 AI 调用和 API 调试外）。

---

## 📝 更新日志

### v1.1.0 (2026-06-23)

- ⚡ 重构为主页 70/30 双栏布局，AI 助手和就绪指示器常驻。
- ⚙️ 新增 AI 模型即时切换功能（支持 Chrome 内置与自定义 API 间一键动态切换）。
- 🔄 新增 Chrome 内置 AI (Gemini Nano) 在线下载安装自动轮询与激活检测机制。
- 🎨 卡片与布局支持明亮/暗色双主题，界面更精美。
- 📝 优化 Markdown 流式代码块及列表渲染。

### v1.0.0 (2026-06-22)

- 🎉 初始发布。
- ✨ 16 个开发工具集成。
- 🤖 AI 助手（独立页面 + 工具内嵌解读）。
- 🎨 暗色毛玻璃 UI 设计。
- 🔌 支持 Chrome 内置 AI 和 OpenAI 兼容接口。

---

## 📄 声明

© 2026 七九在线科技. 由 79team 打造。

---

> 如有问题请提交 [Issue](https://github.com/rowkin/dev-helper/issues)。
