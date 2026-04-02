# OpenAppCLI

> **通用应用自动化平台 + AI Agent 交互标准 - 让任何应用成为你的命令行工具和 AI 伙伴！**  
> 智能适配 · 自动降级 · AI 原生发现 · MCP 协议集成 · 跨平台支持

[![English](https://img.shields.io/badge/docs-English-1D4ED8?style=flat-square)](./README.md)
[![License](https://img.shields.io/npm/l/@wanghaisheng/openappcli?style=flat-square)](./LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/wanghaisheng/openappcli?style=flat-square)](https://github.com/wanghaisheng/openappcli)
[![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux%20%7C%20Android%20%7C%20iOS-blue?style=flat-square)](https://github.com/wanghaisheng/openappcli)
[![MCP Compatible](https://img.shields.io/badge/MCP-Compatible-00D084?style=flat-square)](./docs/mcp-integration.md)

下一代 CLI 工具，将**任何应用** — 网站、Electron 应用、桌面软件、移动应用和游戏 — 变成命令行接口和 **AI Agent 可交互的平台**。由智能策略选择、自适应降级机制、AI 原生发现和 **MCP 协议集成**驱动。

**从 OpenCLI 演进而来** — 在浏览器和 Electron 自动化的坚实基础上，OpenAppCLI 扩展到通用应用控制，支持基于视觉的自动化、系统级访问、移动应用支持，并**通过 MCP 协议实现与 AI Agent 的原生集成**。

**为 AI 时代而生** — 从桌面记事本到移动 Instagram，从 Unity 游戏到专业软件 — 一个平台自动化所有应用，并为 AI Agent 提供标准化的应用交互能力。

---

## 亮点

- **🌍 通用应用支持** — 单一平台自动化网站、Electron 应用、桌面软件、移动应用和游戏
- **🤖 AI Agent 原生集成** — 通过 MCP 协议与所有 AI Agent 无缝对接，标准化工具、资源和提示词
- **🧠 智能策略选择** — AI 驱动的最优自动化策略检测（CDP → UI 层次 → 视觉 → 系统 API）
- **🔄 自适应降级机制** — 主策略失败时自动降级到下一个最佳方法
- **📊 信息提取 + 应用操作** — 不仅获取数据，更能完整控制应用行为（点赞、评论、上传等）
- **👁️ 高级视觉识别** — SIFT/SURF/ORB 特征点匹配、多尺度模板匹配、OCR 集成
- **📱 移动应用自动化** — 通过 ADB、Frida 和 Airtest 集成支持 Android/iOS
- **🎮 游戏引擎优化** — Unity、Unreal 和自定义引擎支持，内置反作弊绕过
- **⚡ 高性能执行** — Minicap 快速截图、并行处理、智能缓存
- **🔧 系统级访问** — Windows/macOS/Linux API、无障碍框架、内存访问
- **📝 MCP 提示词系统** — 智能任务模板，AI Agent 可直接理解并执行复杂自动化流程

## 为什么选 OpenAppCLI？

自动化工具很多，OpenAppCLI 适合什么场景？

| 你的需求 | 最佳工具 | 原因 |
|----------|----------|------|
| **通用应用自动化** | **OpenAppCLI** | 单一平台支持 Web、桌面、移动和游戏 |
| **零配置桌面应用控制** | **OpenAppCLI** | 自动策略检测和降级机制 |
| **移动应用自动化** | **OpenAppCLI** | Android/iOS 支持，视觉和系统级访问 |
| **游戏自动化** | **OpenAppCLI** | 引擎特定优化和反作弊绕过 |
| **AI Agent 应用交互** | **OpenAppCLI** | MCP 协议原生支持，标准化工具和资源访问 |
| **Web 数据提取** | OpenAppCLI | 专注 Web 和 Electron 应用 |
| **大规模网页爬取** | Crawl4AI、Scrapy | 专为吞吐量和规模设计 |
| **通用浏览自动化** | Browser-Use、Stagehand | LLM 驱动的通用浏览，适合一次性任务 |

**OpenAppCLI 的核心差异：**

- **通用覆盖** — 一个平台支持所有应用类型：Web → 桌面 → 移动 → 游戏
- **AI 原生集成** — 通过 MCP 协议成为 AI Agent 的标准应用交互桥梁
- **双向交互** — 不仅能提取数据，更能完整控制应用行为
- **智能适配** — AI 驱动的策略选择和自动降级优化
- **高性能** — Minicap 截图（快 100 倍）、并行处理、智能缓存
- **反检测** — 内置隐身模式，支持游戏和保护应用
- **开发者友好** — 自动适配器生成、可视化调试、完整工具链
- **企业就绪** — 分布式执行、监控、安全和合规功能

> 与 Browser-Use、Crawl4AI、Firecrawl 等工具的详细对比，请查看 [Comparison Guide](./docs/comparison.md)。
> 
> 了解 MCP 集成详情，请查看 [MCP Integration Guide](./docs/mcp-integration.md)。

## 前置要求

- **Node.js**: >= 20.0.0
- **Chrome** 浏览器正在运行，且**已登录目标网站**（如 bilibili.com、zhihu.com、xiaohongshu.com）

> **⚠️ 重要**：大多数命令复用你的 Chrome 登录状态。运行命令前，你必须已在 Chrome 中打开目标网站并完成登录。如果获取到空数据或报错，请先检查你的浏览器登录状态。

OpenAppCLI 通过轻量化的 **Browser Bridge** Chrome 扩展 + 微型 daemon 与浏览器通信（零配置，自动启动）。

### Browser Bridge 扩展配置

你可以选择以下任一方式安装扩展：

**方式一：下载构建好的安装包（推荐）**
1. 到 GitHub [Releases 页面](https://github.com/wanghaisheng/openappcli/releases) 下载最新的 `openappcli-extension.zip`。
2. 解压后打开 Chrome 的 `chrome://extensions`，启用右上角的 **开发者模式**。
3. 点击 **加载已解压的扩展程序**，选择解压后的文件夹。

**方式二：加载源码（针对开发者）**
1. 同样在 `chrome://extensions` 开启 **开发者模式**。
2. 点击 **加载已解压的扩展程序**，选择本仓库代码树中的 `extension/` 文件夹。

完成！运行任何 openappcli 浏览器命令时，后台微型 daemon 会自动启动与浏览器通信。无需配 API Token，零代码配置。

> **Tip**：后续诊断和 daemon 管理：
> ```bash
> openappcli doctor            # 检查扩展和 daemon 连通性
> openappcli daemon status     # 查看 daemon 状态
> openappcli daemon stop       # 停止 daemon
> ```

## 快速开始

### npm 全局安装（推荐）

```bash
npm install -g @wanghaisheng/openappcli
```

### 基础使用

```bash
# 查看所有可用命令
openappcli list                              # 查看所有命令
openappcli list -f yaml                      # 以 YAML 列出所有命令
openappcli hackernews top --limit 5          # 公共 API，无需浏览器
openappcli bilibili hot --limit 5            # 浏览器命令
openappcli zhihu hot -f json                 # JSON 输出
openappcli zhihu hot -f yaml                 # YAML 输出
```

### MCP 集成使用

```bash
# 启动 MCP 服务器
openappcli mcp start

# AI Agent 可用的工具
mcp-tools list | grep openappcli
🤖 Available OpenAppCLI Tools:
   - openappcli.discover_applications
   - openappcli.execute_automation
   - openappcli.get_screenshot
   - openappcli.extract_data

# AI Agent 示例
ai-agent "使用 OpenAppCLI 提取 Bilibili 热门视频"
✅ AI Agent executed: openappcli.bilibili.hot
📺 Retrieved 10 hot videos via MCP protocol
```

### 应用操作示例

```bash
# 信息提取（原有能力）
openappcli instagram feed --limit 10
📸 Latest 10 posts from @user1

# 应用操作（新增能力）
openappcli instagram like --post_id 12345
❤️ Liked post successfully

openappcli instagram comment --post_id 12345 "Great content!"
💬 Comment posted successfully

openappcli instagram follow --user @target_user
 Following @target_user

# 批量操作
openappcli bilibili batch-like --tag "AI" --limit 5
🎯 Liked 5 videos with AI tag
```

### 平台设置

#### Web 和 Electron 应用
> 继承 OpenCLI 的所有 Web 自动化能力，零配置即可使用。

#### 移动应用
> 需要设备连接和调试权限。

```bash
# Android 设置
openappcli mobile setup android
# iOS 设置（即将支持）
openappcli mobile setup ios
```

#### 桌面应用
> 系统级访问需要管理员权限（首次运行时）。

```bash
# Windows
openappcli desktop setup windows --admin
# macOS
openappcli desktop setup macos --accessibility
# Linux
openappcli desktop setup linux --x11
```

### 验证与连接

```bash
openappcli doctor          # 检查所有平台连通性
openappcli status          # 显示可用平台和功能
```

**立即体验：**

```bash
# Web 自动化（继承 OpenCLI）
openappcli hackernews top --limit 5
openappcli bilibili hot --limit 5

# 桌面应用自动化
openappcli discover --app "notepad.exe"
openappcli notepad list-files

# 移动应用自动化
openappcli connect --device android
openappcli discover --app "com.instagram.android"
openappcli instagram feed --limit 5

# AI Agent 集成
openappcli mcp start
ai-agent "通过 OpenAppCLI 为我点赞 Instagram 上的最新照片"
```

## 内置命令

运行 `openappcli list` 查看完整注册表。

### Web 和 Electron 应用（信息提取 + 基础操作）

| 站点 | 命令 | 功能 |
|------|------|------|
| **twitter** | `trending` `bookmarks` `profile` `search` `timeline` `thread` `following` `followers` `notifications` `post` `reply` `delete` `like` `article` `follow` `unfollow` `bookmark` `unbookmark` `download` `accept` `reply-dm` `block` `unblock` `hide-reply` | 信息提取 + 社交互动 |
| **reddit** | `hot` `frontpage` `popular` `search` `subreddit` `read` `user` `user-posts` `user-comments` `upvote` `save` `comment` `subscribe` `saved` `upvoted` | 信息提取 + 社区互动 |
| **bilibili** | `hot` `search` `me` `favorite` `history` `feed` `subtitle` `dynamic` `ranking` `following` `user-videos` `download` `like` `comment` `follow` | 信息提取 + 视频互动 |
| **instagram** | `feed` `profile` `search` `stories` `explore` `like` `comment` `follow` `unfollow` `save` `unsave` `dm` `post` `upload` | 信息提取 + 社交互动 |
| **youtube** | `trending` `search` `channel` `playlist` `watch` `like` `comment` `subscribe` `upload` | 信息提取 + 视频互动 |

### 移动应用（完整应用控制）

| 平台 | 应用 | 命令 | 功能 |
|------|------|------|------|
| **Android** | **Instagram** | `feed` `profile` `stories` `like` `comment` `follow` `post` `upload` `dm` | 完整社交应用控制 |
| **Android** | **TikTok** | `feed` `profile` `search` `like` `comment` `follow` `upload` `duet` | 短视频应用控制 |
| **Android** | **微信** | `messages` `contacts` `moments` `pay` `mini-programs` | 即时通讯应用控制 |
| **iOS** | **Instagram** | `feed` `profile` `stories` `like` `comment` `follow` `post` | iOS 社交应用控制 |

### 桌面应用（系统级控制）

| 平台 | 应用 | 命令 | 功能 |
|------|------|------|------|
| **Windows** | **Notepad++** | `list-files` `read-file` `write-file` `search` `replace` | 文本编辑器控制 |
| **Windows** | **Visual Studio** | `list-solutions` `build` `debug` `code-navigate` `extensions` | IDE 开发控制 |
| **macOS** | **Xcode** | `list-projects` `build` `run` `debug` `simulator` | iOS 开发控制 |
| **Linux** | **VS Code** | `list-workspaces` `open-file` `run-task` `extensions` | 跨平台编辑器控制 |

### 游戏应用（特殊优化）

| 引擎 | 游戏 | 命令 | 功能 |
|------|------|------|------|
| **Unity** | **原神** | `inventory` `characters` `daily-quest` `resin-check` `auto-explore` | RPG 游戏自动化 |
| **Unity** | **王者荣耀** | `match` `hero-select` `skills` `shop` `rank-info` | MOBA 游戏控制 |
| **Unreal** | **堡垒之夜** | `match` `inventory` `building` `emotes` `stats` | 战斗游戏控制 |

66+ 适配器 — **[→ 查看完整命令列表](./docs/adapters/index.md)**

## MCP 协议集成

OpenAppCLI 通过 MCP (Model Context Protocol) 协议为 AI Agent 提供标准化的应用交互能力。

### MCP 工具接口

```typescript
// 标准化工具调用
{
  "name": "openappcli.execute_automation",
  "description": "在任何应用上执行自动化操作",
  "inputSchema": {
    "type": "object",
    "properties": {
      "app_id": {"type": "string"},
      "operation": {"type": "string"},
      "parameters": {"type": "object"}
    }
  }
}
```

### MCP 资源访问

```typescript
// 应用状态资源
openappcli://instagram/ui_hierarchy     // UI 层次结构
openappcli://bilibili/current_state     // 当前播放状态
openappcli://genshin/inventory          // 游戏背包状态

// 系统资源
openappcli://applications              // 已发现应用列表
openappcli://performance_metrics       // 性能指标
openappcli://screenshots              // 应用截图
```

### MCP 提示词系统

```typescript
// 智能任务模板
{
  "name": "social_media_manager",
  "description": "自动化社交媒体管理",
  "arguments": [
    {"name": "platform", "description": "社交媒体平台"},
    {"name": "action", "description": "执行的操作"},
    {"name": "target", "description": "操作目标"}
  ]
}
```

### AI Agent 使用示例

```bash
# 启动 MCP 服务器
openappcli mcp start --port 19826

# AI Agent 自动化社交媒体
ai-agent "帮我管理 Instagram：点赞最新帖子，回复粉丝评论，关注相关用户"

# AI Agent 游戏自动化
ai-agent "完成原神每日任务：领取委托奖励，检查树脂，管理角色装备"

# AI Agent 内容创作
ai-agent "在 Bilibili 发布视频：上传文件，添加标题标签，发布后分享到微博"
```
## 外部 CLI 枢纽

OpenAppCLI 也可以作为你现有命令行工具的统一入口，负责发现、自动安装和纯透传执行。

| 外部 CLI | 描述 | 示例 |
|----------|------|------|
| **gh** | GitHub CLI | `openappcli gh pr list --limit 5` |
| **obsidian** | Obsidian 仓库管理 | `openappcli obsidian search query="AI"` |
| **docker** | Docker 命令行工具 | `openappcli docker ps` |
| **lark-cli** | 飞书 CLI — 消息、文档、日历、任务，200+ 命令 | `openappcli lark-cli calendar +agenda` |
| **dingtalk** | 钉钉 CLI — 钉钉全套产品能力的跨平台命令行工具，支持人类和 AI Agent 使用 | `openappcli dingtalk msg send --to user "hello"` |
| **wecom** | 企业微信 CLI — 企业微信开放平台命令行工具，支持人类和 AI Agent 使用 | `openappcli wecom msg send --to user "hello"` |
| **vercel** | Vercel — 部署项目、管理域名、环境变量、日志 | `openappcli vercel deploy --prod` |

**零配置透传**：OpenAppCLI 会把你的输入原样转发给底层二进制，保留原生 stdout / stderr 行为。

**自动安装**：如果你运行 `openappcli gh ...` 时系统中还没有 `gh`，OpenAppCLI 会优先尝试通过系统包管理器安装，然后自动重试命令。

**注册自定义本地 CLI**：

```bash
openappcli register mycli
```

## 下载支持

OpenAppCLI 支持从各平台下载图片、视频和文章。

### 支持的平台

| 平台 | 内容类型 | 说明 |
|------|----------|------|
| **小红书** | 图片、视频 | 下载笔记中的所有媒体文件 |
| **B站** | 视频 | 需要安装 `yt-dlp` |
| **Twitter/X** | 图片、视频 | 从用户媒体页或单条推文下载 |
| **Pixiv** | 图片 | 下载原始画质插画，支持多页作品 |
| **知乎** | 文章（Markdown） | 导出文章，可选下载图片到本地 |
| **微信公众号** | 文章（Markdown） | 导出公众号文章 |

### 使用示例

```bash
# 下载小红书笔记中的图片/视频
openappcli xiaohongshu download abc123 --output ./xhs

# 下载B站视频（需要 yt-dlp）
openappcli bilibili download BV1xxx --output ./bilibili
openappcli bilibili download BV1xxx --quality 1080p  # 指定画质

# 下载 Twitter 用户的媒体
openappcli twitter download elonmusk --limit 20 --output ./twitter

# 下载单条推文的媒体
openappcli twitter download --tweet-url "https://x.com/user/status/123" --output ./twitter

# 导出知乎文章为 Markdown
openappcli zhihu download "https://zhuanlan.zhihu.com/p/xxx" --output ./zhihu

# 导出并下载图片
openappcli zhihu download "https://zhuanlan.zhihu.com/p/xxx" --download-images

# 导出微信公众号文章为 Markdown
openappcli weixin download --url "https://mp.weixin.qq.com/s/xxx" --output ./weixin
```

对于视频下载，请先安装 `yt-dlp`：`pip install yt-dlp` 或 `brew install yt-dlp`

## 输出格式

所有内置命令都支持 `--format` / `-f`，可选值为 `table`、`json`、`yaml`、`md`、`csv`。

```bash
openappcli list -f yaml            # 用 YAML 列出命令注册表
openappcli bilibili hot -f table   # 默认：富文本表格
openappcli bilibili hot -f json    # JSON（适合传给 jq 或者各类 AI Agent）
openappcli bilibili hot -f yaml    # YAML（更适合人类直接阅读）
openappcli bilibili hot -f md      # Markdown
openappcli bilibili hot -f csv     # CSV
openappcli bilibili hot -v         # 详细模式：展示管线执行步骤调试信息
```

## 退出码

openappcli 遵循 Unix `sysexits.h` 惯例，可无缝接入 shell 管道和 CI 脚本：

| 退出码 | 含义 | 触发场景 |
|--------|------|----------|
| `0` | 成功 | 命令正常完成 |
| `1` | 通用错误 | 未分类的意外错误 |
| `2` | 用法错误 | 参数错误或未知命令 |
| `66` | 无数据 | 命令返回空结果（`EX_NOINPUT`） |
| `69` | 服务不可用 | Browser Bridge 未连接（`EX_UNAVAILABLE`） |
| `75` | 临时失败 | 命令超时，可重试（`EX_TEMPFAIL`） |
| `77` | 需要认证 | 未登录目标网站（`EX_NOPERM`） |
| `78` | 配置错误 | 凭证缺失或配置有误（`EX_CONFIG`） |
| `130` | 中断 | Ctrl-C / SIGINT |

```bash
openappcli bilibili hot 2>/dev/null
case $? in
  0)   echo "ok" ;;
  69)  echo "请先启动 Browser Bridge" ;;
esac
```

## 插件

通过社区贡献的插件扩展 OpenAppCLI。插件使用与内置命令相同的 YAML/TS 格式，启动时自动发现。

```bash
openappcli plugin install github:user/openappcli-plugin-my-tool  # 安装
openappcli plugin list                                         # 查看已安装
openappcli plugin update my-tool                               # 更新到最新
openappcli plugin update --all                                 # 更新全部已安装插件
openappcli plugin uninstall my-tool                            # 卸载
```

当 plugin 的版本被记录到 `~/.openappcli/plugins.lock.json` 后，`openappcli plugin list` 也会显示对应的短 commit hash。

| 插件 | 类型 | 描述 |
|------|------|------|
| [openappcli-plugin-github-trending](https://github.com/ByteYue/openappcli-plugin-github-trending) | YAML | GitHub Trending 仓库 |
| [openappcli-plugin-hot-digest](https://github.com/ByteYue/openappcli-plugin-hot-digest) | TS | 多平台热榜聚合 |
| [openappcli-plugin-juejin](https://github.com/Astro-Han/openappcli-plugin-juejin) | YAML | 稀土掘金热门文章 |

详见 [插件指南](./docs/zh/guide/plugins.md) 了解如何创建自己的插件。

## 致 AI Agent（开发者指南）

如果你是一个被要求查阅代码并编写新 `openappcli` 适配器的 AI，请遵守以下工作流。

> **快速模式**：只想为某个页面快速生成一个命令？看 [CLI-ONESHOT.md](./CLI-ONESHOT.md) — 给一个 URL + 一句话描述，4 步搞定。

> **完整模式**：在编写任何新代码前，先阅读 [CLI-EXPLORER.md](./CLI-EXPLORER.md)。它包含完整的适配器探索开发指南、API 探测流程、5级认证策略以及常见陷阱。

```bash
openappcli explore https://example.com --site mysite   # 探索 API + 能力
openappcli synthesize mysite                            # 生成 YAML 适配器
openappcli generate https://example.com --goal "hot"   # 一键：探索 → 生成 → 注册
openappcli cascade https://api.example.com/data         # 自动探测：PUBLIC → COOKIE → HEADER
```

探索结果输出到 `.openappcli/explore/<site>/`。

## 常见问题排查

- **"Extension not connected" 报错**
  - 确保你当前的 Chrome 已安装且**开启了** openappcli Browser Bridge 扩展（在 `chrome://extensions` 中检查）。
- **"attach failed: Cannot access a chrome-extension:// URL" 报错**
  - 其他 Chrome 扩展（如 youmind、New Tab Override 或 AI 助手类扩展）可能产生冲突。请尝试**暂时禁用其他扩展**后重试。
- **返回空数据，或者报错 "Unauthorized"**
  - Chrome 里的登录态可能已经过期。请打开当前 Chrome 页面，在新标签页重新手工登录或刷新该页面。
- **Node API 错误 (如 parseArgs, fs 等)**
  - 确保 Node.js 版本 `>= 20`。
- **Daemon 问题**
  - 检查 daemon 状态：`curl localhost:19825/status`
  - 查看扩展日志：`curl localhost:19825/logs`

## 测试

详见 **[TESTING.md](./TESTING.md)** 了解如何运行和编写测试。

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=wanghaisheng/openappcli&type=Date)](https://star-history.com/#wanghaisheng/openappcli&Date)

## License

[Apache-2.0](./LICENSE)

---

## 🎯 最终愿景

OpenAppCLI 将成为**应用自动化的通用语言**和 **AI Agent 与应用交互的标准桥梁**，就像 SQL 成为数据库查询的通用语言一样。

### 核心价值主张：
1. **零学习成本**：任何应用，一行命令即可自动化
2. **无限扩展性**：支持任何平台、任何应用类型
3. **智能自适应**：AI 驱动的策略选择和优化
4. **开放生态**：社区驱动的适配器市场
5. **企业级可靠**：生产环境的稳定性和性能
6. **AI 原生集成**：通过 MCP 协议与所有 AI Agent 无缝对接
7. **双向交互能力**：不仅能提取数据，更能完整控制应用行为
8. **标准化协议**：业界统一的工具和资源访问标准

### 影响力：
- **开发者**：从繁琐的逆向工程中解放，专注于业务逻辑
- **企业**：大幅降低自动化成本，提高效率
- **用户**：享受更智能、更自动化的应用体验
- **行业**：推动应用自动化标准化和普及
- **AI 社区**：提供标准化的应用交互能力，加速 AI 应用落地
- **工具生态**：建立统一的应用自动化标准，促进生态繁荣

**最终，OpenAppCLI 将实现"万物皆可自动化，AI 皆可交互应用"的愿景，让任何应用都能通过命令行和 AI Agent 轻松控制和自动化，成为连接数字世界和智能世界的通用桥梁。** 🚀🤖

## 外部 CLI 枢纽

OpenAppCLI 也可以作为你现有命令行工具的统一入口，负责发现、自动安装和纯透传执行。

| 外部 CLI | 描述 | 示例 |
|----------|------|------|
| **gh** | GitHub CLI | `openappcli gh pr list --limit 5` |
| **obsidian** | Obsidian 仓库管理 | `openappcli obsidian search query="AI"` |
| **docker** | Docker 命令行工具 | `openappcli docker ps` |
| **lark-cli** | 飞书 CLI — 消息、文档、日历、任务，200+ 命令 | `openappcli lark-cli calendar +agenda` |
| **dingtalk** | 钉钉 CLI — 钉钉全套产品能力的跨平台命令行工具，支持人类和 AI Agent 使用 | `openappcli dingtalk msg send --to user "hello"` |
| **wecom** | 企业微信 CLI — 企业微信开放平台命令行工具，支持人类和 AI Agent 使用 | `openappcli wecom msg send --to user "hello"` |
| **vercel** | Vercel — 部署项目、管理域名、环境变量、日志 | `openappcli vercel deploy --prod` |

**零配置透传**：OpenAppCLI 会把你的输入原样转发给底层二进制，保留原生 stdout / stderr 行为。

**自动安装**：如果你运行 `openappcli gh ...` 时系统中还没有 `gh`，OpenAppCLI 会优先尝试通过系统包管理器安装，然后自动重试命令。

**注册自定义本地 CLI**：

```bash
openappcli register mycli
```

### 桌面应用适配器

每个桌面适配器都有自己详细的文档说明，包括命令参考、启动配置与使用示例：

| 应用 | 描述 | 文档 |
|-----|-------------|-----|
| **Cursor** | 控制 Cursor IDE — Composer、对话、代码提取等 | [Doc](./docs/adapters/desktop/cursor.md) |
| **Codex** | 在后台（无头）驱动 OpenAI Codex CLI Agent | [Doc](./docs/adapters/desktop/codex.md) |
| **Antigravity** | 在终端直接控制 Antigravity Ultra | [Doc](./docs/adapters/desktop/antigravity.md) |
| **ChatGPT** | 自动化操作 ChatGPT macOS 桌面客户端 | [Doc](./docs/adapters/desktop/chatgpt.md) |
| **ChatWise** | 多 LLM 客户端（GPT-4、Claude、Gemini） | [Doc](./docs/adapters/desktop/chatwise.md) |
| **Notion** | 搜索、读取、写入 Notion 页面 | [Doc](./docs/adapters/desktop/notion.md) |
| **Discord** | Discord 桌面版 — 消息、频道、服务器 | [Doc](./docs/adapters/desktop/discord.md) |
| **Doubao** | 通过 CDP 控制豆包桌面应用 | [Doc](./docs/adapters/desktop/doubao-app.md) |

## 下载支持

OpenAppCLI 支持从各平台下载图片、视频和文章。

### 支持的平台

| 平台 | 内容类型 | 说明 |
|------|----------|------|
| **小红书** | 图片、视频 | 下载笔记中的所有媒体文件 |
| **B站** | 视频 | 需要安装 `yt-dlp` |
| **Twitter/X** | 图片、视频 | 从用户媒体页或单条推文下载 |
| **Pixiv** | 图片 | 下载原始画质插画，支持多页作品 |
| **知乎** | 文章（Markdown） | 导出文章，可选下载图片到本地 |
| **微信公众号** | 文章（Markdown） | 导出微信公众号文章为 Markdown |
| **豆瓣** | 图片 | 下载电影条目的海报 / 剧照图片 |

### 前置依赖

下载流媒体平台的视频需要安装 `yt-dlp`：

```bash
# 安装 yt-dlp
pip install yt-dlp
# 或者
brew install yt-dlp
```

### 使用示例

```bash
# 下载小红书笔记中的图片/视频
openappcli xiaohongshu download abc123 --output ./xhs

# 下载B站视频（需要 yt-dlp）
openappcli bilibili download BV1xxx --output ./bilibili
openappcli bilibili download BV1xxx --quality 1080p  # 指定画质

# 下载 Twitter 用户的媒体
openappcli twitter download elonmusk --limit 20 --output ./twitter

# 下载单条推文的媒体
openappcli twitter download --tweet-url "https://x.com/user/status/123" --output ./twitter

# 下载豆瓣电影海报 / 剧照
openappcli douban download 30382501 --output ./douban

# 导出知乎文章为 Markdown
openappcli zhihu download "https://zhuanlan.zhihu.com/p/xxx" --output ./zhihu

# 导出并下载图片
openappcli zhihu download "https://zhuanlan.zhihu.com/p/xxx" --download-images

# 导出微信公众号文章为 Markdown
openappcli weixin download --url "https://mp.weixin.qq.com/s/xxx" --output ./weixin
```



## 输出格式

所有内置命令都支持 `--format` / `-f`，可选值为 `table`、`json`、`yaml`、`md`、`csv`。
`list` 命令也支持同样的格式参数，同时继续兼容 `--json`。

```bash
openappcli list -f yaml            # 用 YAML 列出命令注册表
openappcli bilibili hot -f table   # 默认：富文本表格
openappcli bilibili hot -f json    # JSON（适合传给 jq 或者各类 AI Agent）
openappcli bilibili hot -f yaml    # YAML（更适合人类直接阅读）
openappcli bilibili hot -f md      # Markdown
openappcli bilibili hot -f csv     # CSV
openappcli bilibili hot -v         # 详细模式：展示管线执行步骤调试信息
```

## 退出码

openappcli 遵循 Unix `sysexits.h` 惯例，可无缝接入 shell 管道和 CI 脚本：

| 退出码 | 含义 | 触发场景 |
|--------|------|----------|
| `0` | 成功 | 命令正常完成 |
| `1` | 通用错误 | 未分类的意外错误 |
| `2` | 用法错误 | 参数错误或未知命令 |
| `66` | 无数据 | 命令返回空结果（`EX_NOINPUT`） |
| `69` | 服务不可用 | Browser Bridge 未连接（`EX_UNAVAILABLE`） |
| `75` | 临时失败 | 命令超时，可重试（`EX_TEMPFAIL`） |
| `77` | 需要认证 | 未登录目标网站（`EX_NOPERM`） |
| `78` | 配置错误 | 凭证缺失或配置有误（`EX_CONFIG`） |
| `130` | 中断 | Ctrl-C / SIGINT |

```bash
opencli bilibili hot 2>/dev/null
case $? in
  0)   echo "ok" ;;
  69)  echo "请先启动 Browser Bridge" ;;
esac
```

## 插件

通过社区贡献的插件扩展 OpenAppCLI。插件使用与内置命令相同的 YAML/TS 格式，启动时自动发现。

```bash
openappcli plugin install github:user/openappcli-plugin-my-tool  # 安装
openappcli plugin list                                         # 查看已安装
openappcli plugin update my-tool                               # 更新到最新
openappcli plugin update --all                                 # 更新全部已安装插件
openappcli plugin uninstall my-tool                            # 卸载
```

当 plugin 的版本被记录到 `~/.openappcli/plugins.lock.json` 后，`openappcli plugin list` 也会显示对应的短 commit hash。

| 插件 | 类型 | 描述 |
|------|------|------|
| [openappcli-plugin-github-trending](https://github.com/ByteYue/openappcli-plugin-github-trending) | YAML | GitHub Trending 仓库 |
| [openappcli-plugin-hot-digest](https://github.com/ByteYue/openappcli-plugin-hot-digest) | TS | 多平台热榜聚合 |
| [openappcli-plugin-juejin](https://github.com/Astro-Han/openappcli-plugin-juejin) | YAML | 稀土掘金热门文章 |

详见 [插件指南](./docs/zh/guide/plugins.md) 了解如何创建自己的插件。

## 致 AI Agent（开发者指南）

如果你是一个被要求查阅代码并编写新 `openappcli` 适配器的 AI，请遵守以下工作流。

> **快速模式**：只想为某个页面快速生成一个命令？看 [CLI-ONESHOT.md](./CLI-ONESHOT.md) — 给一个 URL + 一句话描述，4 步搞定。

> **完整模式**：在编写任何新代码前，先阅读 [CLI-EXPLORER.md](./CLI-EXPLORER.md)。它包含完整的适配器探索开发指南、API 探测流程、5级认证策略以及常见陷阱。

```bash
openappcli explore https://example.com --site mysite   # 探索 API + 能力
openappcli synthesize mysite                            # 生成 YAML 适配器
openappcli generate https://example.com --goal "hot"   # 一键：探索 → 生成 → 注册
openappcli cascade https://api.example.com/data         # 自动探测：PUBLIC → COOKIE → HEADER
```

探索结果输出到 `.openappcli/explore/<site>/`。

## 常见问题排查

- **"Extension not connected" 报错**
  - 确保你当前的 Chrome 已安装且**开启了** openappcli Browser Bridge 扩展（在 `chrome://extensions` 中检查）。
- **"attach failed: Cannot access a chrome-extension:// URL" 报错**
  - 其他 Chrome 扩展（如 youmind、New Tab Override 或 AI 助手类扩展）可能产生冲突。请尝试**暂时禁用其他扩展**后重试。
- **返回空数据，或者报错 "Unauthorized"**
  - Chrome 里的登录态可能已经过期。请打开当前 Chrome 页面，在新标签页重新手工登录或刷新该页面。
- **Node API 错误 (如 parseArgs, fs 等)**
  - 确保 Node.js 版本 `>= 20`。
- **Daemon 问题**
  - 检查 daemon 状态：`curl localhost:19825/status`
  - 查看扩展日志：`curl localhost:19825/logs`


## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=jackwener/opencli&type=Date)](https://star-history.com/#jackwener/opencli&Date)



## License

[Apache-2.0](./LICENSE)
