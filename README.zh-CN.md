# OpenAppCLI

> **通用应用自动化平台 - 让任何应用成为你的命令行工具！**  
> 智能适配 · 自动降级 · AI 驱动发现 · 跨平台支持

[![English](https://img.shields.io/badge/docs-English-1D4ED8?style=flat-square)](./README.md)
[![License](https://img.shields.io/npm/l/@jackwener/opencli?style=flat-square)](./LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/wanghaisheng/openappcli?style=flat-square)](https://github.com/wanghaisheng/openappcli)
[![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux%20%7C%20Android%20%7C%20iOS-blue?style=flat-square)](https://github.com/wanghaisheng/openappcli)

下一代 CLI 工具，将**任何应用** — 网站、Electron 应用、桌面软件、移动应用和游戏 — 变成命令行接口。由智能策略选择、自适应降级机制和 AI 原生发现驱动。

**从 OpenCLI 演进而来** — 在浏览器和 Electron 自动化的坚实基础上，OpenAppCLI 扩展到通用应用控制，支持基于视觉的自动化、系统级访问和移动应用支持。

**为通用自动化时代而生** — 从桌面记事本到移动 Instagram，从 Unity 游戏到专业软件 — 一个平台自动化所有应用。

---

## 亮点

- **🌍 通用应用支持** — 单一平台自动化网站、Electron 应用、桌面软件、移动应用和游戏
- **🧠 智能策略选择** — AI 驱动的最优自动化策略检测（CDP → UI 层次 → 视觉 → 系统 API）
- **🔄 自适应降级机制** — 主策略失败时自动降级到下一个最佳方法
- **👁️ 高级视觉识别** — SIFT/SURF/ORB 特征点匹配、多尺度模板匹配、OCR 集成
- **📱 移动应用自动化** — 通过 ADB、Frida 和 Airtest 集成支持 Android/iOS
- **🎮 游戏引擎优化** — Unity、Unreal 和自定义引擎支持，内置反作弊绕过
- **⚡ 高性能执行** — Minicap 快速截图、并行处理、智能缓存
- **🔧 系统级访问** — Windows/macOS/Linux API、无障碍框架、内存访问
- **🤖 AI 原生开发** — 自动适配器生成、性能优化、错误恢复

## 为什么选 OpenAppCLI？

自动化工具很多，OpenAppCLI 适合什么场景？

| 你的需求 | 最佳工具 | 原因 |
|----------|----------|------|
| **通用应用自动化** | **OpenAppCLI** | 单一平台支持 Web、桌面、移动和游戏 |
| **零配置桌面应用控制** | **OpenAppCLI** | 自动策略检测和降级机制 |
| **移动应用自动化** | **OpenAppCLI** | Android/iOS 支持，视觉和系统级访问 |
| **游戏自动化** | **OpenAppCLI** | 引擎特定优化和反作弊绕过 |
| **Web 数据提取** | OpenAppCLI | 专注 Web 和 Electron 应用 |
| **大规模网页爬取** | Crawl4AI、Scrapy | 专为吞吐量和规模设计 |
| **通用浏览自动化** | Browser-Use、Stagehand | LLM 驱动的通用浏览，适合一次性任务 |

**OpenAppCLI 的核心差异：**

- **通用覆盖** — 一个平台支持所有应用类型：Web → 桌面 → 移动 → 游戏
- **智能适配** — AI 驱动的策略选择和自动降级优化
- **高性能** — Minicap 截图（快 100 倍）、并行处理、智能缓存
- **反检测** — 内置隐身模式，支持游戏和保护应用
- **开发者友好** — 自动适配器生成、可视化调试、完整工具链
- **企业就绪** — 分布式执行、监控、安全和合规功能

> 与 Browser-Use、Crawl4AI、Firecrawl 等工具的详细对比，请查看 [Comparison Guide](./docs/comparison.md)。

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

直接使用：

```bash
openappcli list                              # 查看所有命令
openappcli list -f yaml                      # 以 YAML 列出所有命令
openappcli hackernews top --limit 5          # 公共 API，无需浏览器
openappcli bilibili hot --limit 5            # 浏览器命令
openappcli zhihu hot -f json                 # JSON 输出
openappcli zhihu hot -f yaml                 # YAML 输出
```

### 从源码安装（面向开发者）

```bash
git clone https://github.com/wanghaisheng/openappcli.git
cd openappcli 
npm install
npm run build
npm link      # 链接到全局环境
openappcli list  # 可以在任何地方使用了！
```

### 更新

```bash
npm install -g @wanghaisheng/openappcli@latest
```

## 内置命令

运行 `openappcli list` 查看完整注册表。

| 站点 | 命令 | 模式 |
|------|------|------|
| **twitter** | `trending` `bookmarks` `profile` `search` `timeline` `thread` `following` `followers` `notifications` `post` `reply` `delete` `like` `article` `follow` `unfollow` `bookmark` `unbookmark` `download` `accept` `reply-dm` `block` `unblock` `hide-reply` | 浏览器 |
| **reddit** | `hot` `frontpage` `popular` `search` `subreddit` `read` `user` `user-posts` `user-comments` `upvote` `save` `comment` `subscribe` `saved` `upvoted` | 浏览器 |
| **tieba** | `hot` `posts` `search` `read` | 浏览器 |
| **cursor** | `status` `send` `read` `new` `dump` `composer` `model` `extract-code` `ask` `screenshot` `history` `export` | 桌面端 |
| **bilibili** | `hot` `search` `me` `favorite` `history` `feed` `subtitle` `dynamic` `ranking` `following` `user-videos` `download` | 浏览器 |
| **codex** | `status` `send` `read` `new` `dump` `extract-diff` `model` `ask` `screenshot` `history` `export` | 桌面端 |
| **chatwise** | `status` `new` `send` `read` `ask` `model` `history` `export` `screenshot` | 桌面端 |
| **doubao** | `status` `new` `send` `read` `ask` `history` `detail` `meeting-summary` `meeting-transcript` | 浏览器 |
| **doubao-app** | `status` `new` `send` `read` `ask` `screenshot` `dump` | 桌面端 |
| **notion** | `status` `search` `read` `new` `write` `sidebar` `favorites` `export` | 桌面端 |
| **discord-app** | `status` `send` `read` `channels` `servers` `search` `members` | 桌面端 |
| **v2ex** | `hot` `latest` `topic` `node` `user` `member` `replies` `nodes` `daily` `me` `notifications` | 公开 / 浏览器 |
| **xueqiu** | `feed` `hot-stock` `hot` `search` `stock` `comments` `watchlist` `earnings-date` `fund-holdings` `fund-snapshot` | 浏览器 |
| **antigravity** | `status` `send` `read` `new` `dump` `extract-code` `model` `watch` | 桌面端 |
| **chatgpt** | `status` `new` `send` `read` `ask` `model` | 桌面端 |
| **xiaohongshu** | `search` `notifications` `feed` `user` `download` `publish` `creator-notes` `creator-note-detail` `creator-notes-summary` `creator-profile` `creator-stats` | 浏览器 |
| **apple-podcasts** | `search` `episodes` `top` | 公开 |
| **xiaoyuzhou** | `podcast` `podcast-episodes` `episode` | 公开 |
| **zhihu** | `hot` `search` `question` `download` | 浏览器 |
| **weixin** | `download` | 浏览器 |
| **youtube** | `search` `video` `transcript` | 浏览器 |
| **boss** | `search` `detail` `recommend` `joblist` `greet` `batchgreet` `send` `chatlist` `chatmsg` `invite` `mark` `exchange` `resume` `stats` | 浏览器 |
| **coupang** | `search` `add-to-cart` | 浏览器 |
| **bbc** | `news` | 公共 API |
| **bloomberg** | `main` `markets` `economics` `industries` `tech` `politics` `businessweek` `opinions` `feeds` `news` | 公共 API / 浏览器 |
| **ctrip** | `search` | 浏览器 |
| **devto** | `top` `tag` `user` | 公开 |
| **dictionary** | `search` `synonyms` `examples` | 公开 |
| **arxiv** | `search` `paper` | 公开 |
| **paperreview** | `submit` `review` `feedback` | 公开 |
| **wikipedia** | `search` `summary` `random` `trending` | 公开 |
| **hackernews** | `top` `new` `best` `ask` `show` `jobs` `search` `user` | 公共 API |
| **jd** | `item` | 浏览器 |
| **linkedin** | `search` `timeline` | 浏览器 |
| **reuters** | `search` | 浏览器 |
| **smzdm** | `search` | 浏览器 |
| **web** | `read` | 浏览器 |
| **weibo** | `hot` `search` | 浏览器 |
| **yahoo-finance** | `quote` | 浏览器 |
| **sinafinance** | `news` | 🌐 公开 |
| **barchart** | `quote` `options` `greeks` `flow` | 浏览器 |
| **chaoxing** | `assignments` `exams` | 浏览器 |
| **grok** | `ask` | 浏览器 |
| **hf** | `top` | 公开 |
| **jike** | `feed` `search` `create` `like` `comment` `repost` `notifications` `post` `topic` `user` | 浏览器 |
| **jimeng** | `generate` `history` | 浏览器 |
| **yollomi** | `generate` `video` `edit` `upload` `models` `remove-bg` `upscale` `face-swap` `restore` `try-on` `background` `object-remover` | 浏览器 |
| **linux-do** | `feed` `categories` `tags` `search` `topic` `user-topics` `user-posts` | 浏览器 |
| **stackoverflow** | `hot` `search` `bounties` `unanswered` | 公开 |
| **steam** | `top-sellers` | 公开 |
| **weread** | `shelf` `search` `book` `highlights` `notes` `notebooks` `ranking` | 浏览器 |
| **douban** | `search` `top250` `subject` `photos` `download` `marks` `reviews` `movie-hot` `book-hot` | 浏览器 |
| **facebook** | `feed` `profile` `search` `friends` `groups` `events` `notifications` `memories` `add-friend` `join-group` | 浏览器 |
| **google** | `news` `search` `suggest` `trends` | 公开 |
| **spotify** | `auth` `status` `play` `pause` `next` `prev` `volume` `search` `queue` `shuffle` `repeat` | OAuth API |
| **notebooklm** | `status` `list` `open` `select` `current` `get` `metadata` `source-list` `source-get` `source-fulltext` `source-guide` `history` `note-list` `notes-list` `notes-get` `summary` | 浏览器 |
| **36kr** | `news` `hot` `search` `article` | 公开 / 浏览器 |
| **imdb** | `search` `title` `top` `trending` `person` `reviews` | 公开 |
| **producthunt** | `posts` `today` `hot` `browse` | 公开 / 浏览器 |
| **instagram** | `explore` `profile` `search` `user` `followers` `following` `follow` `unfollow` `like` `unlike` `comment` `save` `unsave` `saved` | 浏览器 |
| **lobsters** | `hot` `newest` `active` `tag` | 公开 |
| **medium** | `feed` `search` `user` | 浏览器 |
| **sinablog** | `hot` `search` `article` `user` | 浏览器 |
| **substack** | `feed` `search` `publication` | 浏览器 |
| **pixiv** | `ranking` `search` `user` `illusts` `detail` `download` | 浏览器 |
| **tiktok** | `explore` `search` `profile` `user` `following` `follow` `unfollow` `like` `unlike` `comment` `save` `unsave` `live` `notifications` `friends` | 浏览器 |
| **bluesky** | `search` `trending` `user` `profile` `thread` `feeds` `followers` `following` `starter-packs` | 公开 |
| **douyin** | `videos` `publish` `drafts` `draft` `delete` `stats` `profile` `update` `hashtag` `location` `activities` `collections` | 浏览器 |

66+ 适配器 — **[→ 查看完整命令列表](./docs/adapters/index.md)**

### 外部 CLI 枢纽

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
