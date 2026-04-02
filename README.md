# OpenAppCLI

> **Universal Application Automation Platform + AI Agent Interaction Standard - Make any application your CLI and AI partner!**
> Zero risk · Intelligent adaptation · AI-powered discovery · MCP Protocol Integration · Multi-platform support

[![中文文档](https://img.shields.io/badge/docs-%E4%B8%AD%E6%96%87-0F766E?style=flat-square)](./README.zh-CN.md)
[![License](https://img.shields.io/npm/l/@jackwener/opencli?style=flat-square)](./LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/wanghaisheng/openappcli?style=flat-square)](https://github.com/wanghaisheng/openappcli)
[![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux%20%7C%20Android%20%7C%20iOS-blue?style=flat-square)](https://github.com/wanghaisheng/openappcli)
[![MCP Compatible](https://img.shields.io/badge/MCP-Compatible-00D084?style=flat-square)](./docs/mcp-integration.md)

A next-generation CLI tool that turns **any application** — websites, Electron apps, desktop software, mobile apps, and games — into a command-line interface **and AI Agent-interactable platform**. Powered by intelligent strategy selection, adaptive fallback mechanisms, AI-native discovery, and **MCP Protocol integration**.

**Evolved from OpenCLI** — Building on the solid foundation of browser and Electron automation, OpenAppCLI extends to universal application control with vision-based automation, system-level access, mobile app support, and **native integration with AI Agents through MCP Protocol**.

**Built for the AI Era** — From desktop Notepad to mobile Instagram, from Unity games to professional software — one platform to automate all applications and provide standardized interaction capabilities for AI Agents.

**Built for AI Agents** — Configure an instruction in your `AGENT.md` or `.cursorrules` to run `openappcli list` via Bash. The AI will automatically discover and invoke all available tools through MCP Protocol.

**CLI Hub** — Register any local CLI (`openappcli register mycli`) so AI agents can discover and call it alongside built-in commands. Auto-installs missing tools via your package manager (e.g. if `gh` isn't installed, `openappcli gh ...` runs `brew install gh` first then re-executes seamlessly).

**CLI for Electron Apps** — Turn any Electron application into a CLI tool. Recombine, script, and extend apps like Antigravity Ultra from the terminal. AI agents can now control other AI apps natively.

---

## Highlights

- **🌍 Universal Application Support** — Automate websites, Electron apps, desktop software, mobile apps, and games with a single platform
- **� AI Agent Native Integration** — Seamless integration with all AI Agents through MCP Protocol, standardized tools, resources, and prompts
- **� Intelligent Strategy Selection** — AI-powered detection of optimal automation strategies (CDP → UI Hierarchy → Vision → System API)
- **🔄 Adaptive Fallback Mechanisms** — Automatic degradation to the next best method when primary strategy fails
- **📊 Information Extraction + Application Control** — Not just data extraction, but complete application behavior control (like, comment, upload, etc.)
- **👁️ Advanced Vision Recognition** — SIFT/SURF/ORB feature matching, multi-scale template matching, OCR integration
- **📱 Mobile App Automation** — Android/iOS support via ADB, Frida, and Airtest integration
- **🎮 Game Engine Optimization** — Unity, Unreal, and custom engine support with anti-cheat bypass
- **⚡ High-Performance Execution** — Minicap for fast screenshots, parallel processing, intelligent caching
- **🔧 System-Level Access** — Windows/macOS/Linux APIs, accessibility frameworks, memory access
- **📝 MCP Prompt System** — Intelligent task templates that AI Agents can directly understand and execute complex automation workflows

## Why OpenAppCLI?

There are many great automation tools. Here's when OpenAppCLI is the right choice:

| Your need | Best tool | Why |
|-----------|-----------|-----|
| **Universal application automation** | **OpenAppCLI** | Single platform for web, desktop, mobile, and games |
| **Zero-config desktop app control** | **OpenAppCLI** | Automatic strategy detection and fallback mechanisms |
| **Mobile app automation** | **OpenAppCLI** | Android/iOS support with vision and system-level access |
| **Game automation** | **OpenAppCLI** | Engine-specific optimizations and anti-cheat bypass |
| **AI Agent application interaction** | **OpenAppCLI** | MCP Protocol native support, standardized tools and resource access |
| **Web data extraction** | OpenAppCLI | Focused on web and Electron apps |
| **Large-scale web crawling** | Crawl4AI, Scrapy | Purpose-built for throughput and scale |
| **General browsing automation** | Browser-Use, Stagehand | LLM-driven general browsing for one-off tasks |

**What makes OpenAppCLI different:**

- **Universal Coverage** — One platform supports all application types: Web → Desktop → Mobile → Games
- **AI Native Integration** — Becomes the standard bridge for AI Agent application interaction through MCP Protocol
- **Bidirectional Interaction** — Not just data extraction, but complete application behavior control
- **Intelligent Adaptation** — AI-driven strategy selection and automatic fallback optimization
- **High Performance** — Minicap screenshots (100x faster), parallel processing, intelligent caching
- **Anti-Detection** — Built-in stealth mode, supports games and protected applications
- **Developer Friendly** — Automatic adapter generation, visual debugging, comprehensive toolchain
- **Enterprise Ready** — Distributed execution, monitoring, security, and compliance features

> For detailed comparison with Browser-Use, Crawl4AI, Firecrawl and other tools, see [Comparison Guide](./docs/comparison.md).
> 
> For MCP integration details, see [MCP Integration Guide](./docs/mcp-integration.md).

---

## Quick Start

### 1. Install OpenAppCLI

**Install via npm (recommended)**

```bash
npm install -g @wanghaisheng/openappcli
```

### 2. Basic Usage

```bash
# List all available commands
openappcli list                              # List all commands
openappcli list -f yaml                      # List commands in YAML format
openappcli hackernews top --limit 5          # Public API, no browser needed
openappcli bilibili hot --limit 5            # Browser command
openappcli zhihu hot -f json                 # JSON output
openappcli zhihu hot -f yaml                 # YAML output
```

### 3. MCP Integration Usage

```bash
# Start MCP server
openappcli mcp start

# AI Agent available tools
mcp-tools list | grep openappcli
🤖 Available OpenAppCLI Tools:
   - openappcli.discover_applications
   - openappcli.execute_automation
   - openappcli.get_screenshot
   - openappcli.extract_data

# AI Agent example
ai-agent "Extract Bilibili hot videos using OpenAppCLI"
✅ AI Agent executed: openappcli.bilibili.hot
📺 Retrieved 10 hot videos via MCP protocol
```

### 4. Application Operation Examples

```bash
# Information extraction (original capability)
openappcli instagram feed --limit 10
📸 Latest 10 posts from @user1

# Application operations (new capability)
openappcli instagram like --post_id 12345
❤️ Liked post successfully

openappcli instagram comment --post_id 12345 "Great content!"
💬 Comment posted successfully

openappcli instagram follow --user @target_user
 Following @target_user

# Batch operations
openappcli bilibili batch-like --tag "AI" --limit 5
🎯 Liked 5 videos with AI tag
```

### 5. Platform Setup

#### For Web & Electron Apps (Browser Bridge)
> OpenAppCLI connects to your browser through a lightweight **Browser Bridge** Chrome Extension + micro-daemon (zero config, auto-start).

1. Go to the GitHub [Releases page](https://github.com/wanghaisheng/openappcli/releases) and download the latest `openappcli-extension.zip`.
2. Unzip the file and open `chrome://extensions`, enable **Developer mode** (top-right toggle).
3. Click **Load unpacked** and select the unzipped folder.

#### For Mobile Apps (Android/iOS)
> Connect your mobile device and install required dependencies.

```bash
# Android setup
openappcli mobile setup android
# iOS setup (coming soon)
openappcli mobile setup ios
```

#### For Desktop Apps
> System-level access requires administrator privileges on first run.

```bash
# Windows
openappcli desktop setup windows --admin
# macOS
openappcli desktop setup macos --accessibility
# Linux
openappcli desktop setup linux --x11
```

### 6. Verify & Try

```bash
openappcli doctor          # Check all platform connectivity
openappcli status          # Show available platforms and capabilities
```

**Try it out:**

```bash
# Web automation (inherited from OpenCLI)
openappcli hackernews top --limit 5
openappcli bilibili hot --limit 5

# Desktop app automation
openappcli discover --app "notepad.exe"
openappcli notepad list-files

# Mobile app automation
openappcli connect --device android
openappcli discover --app "com.instagram.android"
openappcli instagram feed --limit 5

# AI Agent integration
openappcli mcp start
ai-agent "Like Instagram's latest photos for me using OpenAppCLI"
```

### Update

```bash
npm install -g @wanghaisheng/openappcli@latest
```

---

## Platform Support

OpenAppCLI supports a wide range of application types across all major platforms:

### 🌐 Web Applications
*Inherited from OpenCLI with enhanced capabilities*
- **50+ built-in site adapters**: Bilibili, Twitter, Reddit, GitHub, etc.
- **Browser session reuse**: Zero login required
- **Anti-detection**: Stealth mode for protected sites

### 🖥️ Desktop Applications
*New universal desktop automation*
- **Windows Native Apps**: Via Win32 API and Accessibility frameworks
- **macOS Native Apps**: Via Cocoa and Accessibility APIs
- **Linux Native Apps**: Via X11 and AT-SPI
- **Cross-platform IDEs**: VS Code, Visual Studio, Xcode, etc.

### 📱 Mobile Applications
*Complete mobile app control*
- **Android**: ADB, UIAutomator, Frida dynamic instrumentation
- **iOS**: XCUITest, Accessibility Inspector
- **Cross-platform Apps**: Instagram, TikTok, WeChat, etc.

### 🎮 Game Applications
*Specialized game engine support*
- **Unity Games**: Memory access, GameObject manipulation, anti-cheat bypass
- **Unreal Games**: Actor and component access, rendering data extraction
- **Custom Engines**: Vision-based automation with AI enhancement

### 🤖 AI Agent Integration
*Native MCP Protocol support*
- **Standardized Tools**: Universal automation interface for all AI Agents
- **Resource Access**: Real-time application state and system information
- **Prompt Templates**: Intelligent task templates for complex workflows

## CLI Hub

OpenAppCLI acts as a universal hub for your existing command-line tools — unified discovery, pure passthrough execution, and auto-install (if a tool isn't installed, OpenAppCLI runs `brew install <tool>` automatically before re-running the command).

| External CLI | Description | Example |
|--------------|-------------|---------|
| **gh** | GitHub CLI | `openappcli gh pr list --limit 5` |
| **obsidian** | Obsidian vault management | `openappcli obsidian search query="AI"` |
| **docker** | Docker | `openappcli docker ps` |
| **lark-cli** | Lark/Feishu — messages, docs, calendar, tasks, 200+ commands | `openappcli lark-cli calendar +agenda` |
| **dingtalk** | DingTalk — cross-platform CLI for DingTalk's full suite, designed for humans and AI agents | `openappcli dingtalk msg send --to user "hello"` |
| **wecom** | WeCom/企业微信 — CLI for WeCom open platform, for humans and AI agents | `openappcli wecom msg send --to user "hello"` |
| **vercel** | Vercel — deploy projects, manage domains, env vars, logs | `openappcli vercel deploy --prod` |

**Zero-config passthrough**：OpenAppCLI forwards your input directly to the underlying binary, preserving native stdout / stderr behavior.

**Auto-install**：If you run `openappcli gh ...` and `gh` isn't installed, OpenAppCLI automatically installs it via your package manager first, then re-executes seamlessly.

**Register your own** — add any local CLI so AI agents can discover it via `openappcli list`:

```bash
openappcli register mycli
```
- **Windows Apps**: Notepad, Calculator, VS Code, Photoshop, etc.
- **macOS Apps**: Finder, Safari, Xcode, etc.  
- **Linux Apps**: File managers, IDEs, system tools
- **Electron Apps**: Cursor, Antigravity, ChatGPT desktop, etc.

### 📱 Mobile Applications
*Cross-platform mobile automation*
- **Android Apps**: Instagram, TikTok, WeChat, games, etc.
- **iOS Apps**: Coming soon with XCUITest integration
- **Hybrid Apps**: React Native, Flutter, Cordova

### 🎮 Games
*Specialized game automation*
- **Unity Games**: Genshin Impact, Honkai Star Rail, etc.
- **Unreal Games**: Fortnite, PUBG Mobile, etc.
- **Custom Engines**: Anti-cheat bypass and stealth mode

### 🔧 System Integration
*Deep system-level access*
- **Windows API**: Win32, COM, WMI integration
- **macOS API**: Cocoa, Accessibility, AppleScript
- **Linux API**: X11, AT-SPI, D-Bus
- **Mobile APIs**: ADB, Frida, UIAutomator

---

## Universal Discovery

OpenAppCLI can automatically analyze and generate adapters for any application:

```bash
# Discover any application
openappcli discover --app "C:\Program Files\Notepad++\notepad++.exe"

# Output example:
🔍 Analyzing application: Notepad++
📊 Application Type: Native Windows Application
🎯 Recommended Strategy: Hybrid (Accessibility + Vision + System API)
🔧 Generated Adapter: ./src/clis/notepadpp/adapter.ts
📝 Sample Pipeline: ./src/clis/notepadpp/extract.yaml
🧪 Test Script: ./src/clis/notepadpp/test.py

# Use immediately
openappcli notepadpp list-files
📄 Found 12 files in current directory:
   - README.md (2.3KB)
   - package.json (1.1KB)
   - src/ (directory)
   - docs/ (directory)
```

## Prerequisites

- **Node.js**: >= 20.0.0 (or **Bun** >= 1.0)
- **Chrome** running **and logged into the target site** (e.g. bilibili.com, zhihu.com, xiaohongshu.com).

> **⚠️ Important**: Browser commands reuse your Chrome login session. You must be logged into the target website in Chrome before running commands. If you get empty data or errors, check your login status first.

## Built-in Commands

| Site | Commands |
|------|----------|
| **xiaohongshu** | `search` `note` `comments` `feed` `user` `download` `publish` `notifications` `creator-notes` `creator-notes-summary` `creator-note-detail` `creator-profile` `creator-stats` |
| **bilibili** | `hot` `search` `history` `feed` `ranking` `download` `comments` `dynamic` `favorite` `following` `me` `subtitle` `user-videos` |
| **tieba** | `hot` `posts` `search` `read` |
| **twitter** | `trending` `search` `timeline` `bookmarks` `post` `download` `profile` `article` `like` `likes` `notifications` `reply` `reply-dm` `thread` `follow` `unfollow` `followers` `following` `block` `unblock` `bookmark` `unbookmark` `delete` `hide-reply` `accept` |
| **reddit** | `hot` `frontpage` `popular` `search` `subreddit` `user` `user-posts` `user-comments` `read` `save` `saved` `subscribe` `upvote` `upvoted` `comment` |
| **notebooklm** | `status` `list` `open` `select` `current` `get` `metadata` `source-list` `source-get` `source-fulltext` `source-guide` `history` `note-list` `notes-list` `notes-get` `summary` |
| **spotify** | `auth` `status` `play` `pause` `next` `prev` `volume` `search` `queue` `shuffle` `repeat` |

66+ adapters in total — **[→ see all supported sites & commands](./docs/adapters/index.md)**

## CLI Hub

OpenAppCLI acts as a universal hub for your existing command-line tools — unified discovery, pure passthrough execution, and auto-install (if a tool isn't installed, OpenAppCLI runs `brew install <tool>` automatically before re-running the command).

| External CLI | Description | Example |
|--------------|-------------|---------|

### Desktop App Adapters

Each desktop adapter has its own detailed documentation, including command reference, startup configuration, and usage examples.

| App | Description | Doc |
|-----|-------------|-----|
| **Cursor** | Control Cursor IDE — Composer, chat, code extraction | [Doc](./docs/adapters/desktop/cursor.md) |
| **Codex** | Drive OpenAI Codex CLI agent headlessly | [Doc](./docs/adapters/desktop/codex.md) |
| **Antigravity** | Control Antigravity Ultra from the terminal | [Doc](./docs/adapters/desktop/antigravity.md) |
| **ChatGPT** | Automate ChatGPT macOS desktop app | [Doc](./docs/adapters/desktop/chatgpt.md) |
| **ChatWise** | Multi-LLM client (GPT-4, Claude, Gemini) | [Doc](./docs/adapters/desktop/chatwise.md) |
| **Notion** | Search, read, write Notion pages | [Doc](./docs/adapters/desktop/notion.md) |
| **Discord** | Discord Desktop — messages, channels, servers | [Doc](./docs/adapters/desktop/discord.md) |
| **Doubao** | Control Doubao AI desktop app via CDP | [Doc](./docs/adapters/desktop/doubao-app.md) |

To add a new Electron app, start with [docs/guide/electron-app-cli.md](./docs/guide/electron-app-cli.md).

## Download Support

OpenAppCLI supports downloading images, videos, and articles from supported platforms.

| Platform | Content Types | Notes |
|----------|---------------|-------|
| **Xiaohongshu** | Images, Videos | Downloads all media from a note |
| **Bilibili** | Videos | Requires `yt-dlp` |
| **Twitter/X** | Images, Videos | From user media tab or single tweet |
| **Pixiv** | Images | Original-quality illustrations, multi-page |
| **Zhihu** | Articles (Markdown) | Exports with optional image download |
| **WeChat** | Articles (Markdown) | WeChat Official Account articles |

For video downloads, install `yt-dlp` first: `brew install yt-dlp`

```bash
# Download Xiaohongshu note media
openappcli xiaohongshu download abc123 --output ./xhs

# Download Bilibili video (requires yt-dlp)
openappcli bilibili download BV1xxx --output ./bilibili
openappcli bilibili download BV1xxx --quality 1080p  # Specify quality

# Download Twitter user media
openappcli twitter download elonmusk --limit 20 --output ./twitter

# Download single tweet media
openappcli twitter download --tweet-url "https://x.com/user/status/123" --output ./twitter

# Export Zhihu article as Markdown
openappcli zhihu download "https://zhuanlan.zhihu.com/p/xxx" --output ./zhihu

# Export and download images
openappcli zhihu download "https://zhuanlan.zhihu.com/p/xxx" --download-images

# Export WeChat article as Markdown
openappcli weixin download --url "https://mp.weixin.qq.com/s/xxx" --output ./weixin
```

## Output Formats

All built-in commands support `--format` / `-f` with `table` (default), `json`, `yaml`, `md`, and `csv`.

```bash
openappcli list -f yaml            # List command registry in YAML
openappcli bilibili hot -f table   # Default: Rich text table
openappcli bilibili hot -f json    # Pipe to jq or LLMs
openappcli bilibili hot -f yaml    # More human-readable
openappcli bilibili hot -f md      # Markdown
openappcli bilibili hot -f csv     # CSV
openappcli bilibili hot -v         # Verbose: show pipeline debug steps
```

## Exit Codes

OpenAppCLI follows Unix `sysexits.h` conventions so it integrates naturally with shell pipelines and CI scripts:

| Code | Meaning | When |
|------|---------|------|
| `0` | Success | Command completed normally |
| `1` | Generic error | Unexpected / unclassified failure |
| `2` | Usage error | Bad arguments or unknown command |
| `66` | Empty result | No data returned (`EX_NOINPUT`) |
| `69` | Service unavailable | Browser Bridge not connected (`EX_UNAVAILABLE`) |
| `75` | Temporary failure | Command timed out — retry (`EX_TEMPFAIL`) |
| `77` | Auth required | Not logged in to target site (`EX_NOPERM`) |
| `78` | Config error | Missing credentials or bad config (`EX_CONFIG`) |
| `130` | Interrupted | Ctrl-C / SIGINT |

```bash
openappcli spotify status || echo "exit $?"   # 69 if browser not running
openappcli github issues 2>/dev/null
[ $? -eq 77 ] && openappcli github auth       # auto-auth if not logged in
```

## Plugins

Extend OpenAppCLI with community-contributed adapters:

```bash
openappcli plugin install github:user/openappcli-plugin-my-tool  # Install
openappcli plugin list                                         # View installed
openappcli plugin update --all                                 # Update all
openappcli plugin uninstall my-tool                            # Uninstall
```

| Plugin | Type | Description |
|--------|------|-------------|
| [openappcli-plugin-github-trending](https://github.com/ByteYue/openappcli-plugin-github-trending) | YAML | GitHub Trending repositories |
| [openappcli-plugin-hot-digest](https://github.com/ByteYue/openappcli-plugin-hot-digest) | TS | Multi-platform trending aggregator |
| [openappcli-plugin-juejin](https://github.com/Astro-Han/openappcli-plugin-juejin) | YAML | 稀土掘金 hot articles |

See [Plugins Guide](./docs/guide/plugins.md) for creating your own plugin.

## For AI Agents (Developer Guide)

> **Quick mode**: To generate a single command for a specific page URL, see [CLI-ONESHOT.md](./CLI-ONESHOT.md) — just a URL + one-line goal, 4 steps done.

> **Full mode**: Before writing any adapter code, read [CLI-EXPLORER.md](./CLI-EXPLORER.md). It contains the complete browser exploration workflow, the 5-tier authentication strategy decision tree, and debugging guide.

```bash
openappcli explore https://example.com --site mysite   # Discover APIs + capabilities
openappcli synthesize mysite                            # Generate YAML adapters
openappcli generate https://example.com --goal "hot"   # One-shot: explore → synthesize → register
openappcli cascade https://api.example.com/data         # Auto-probe: PUBLIC → COOKIE → HEADER
```

## Testing

See **[TESTING.md](./TESTING.md)** for how to run and write tests.

## Troubleshooting

- **"Extension not connected" error**
  - Ensure your Chrome has the **openappcli Browser Bridge** extension installed and **enabled** in `chrome://extensions`.
- **"attach failed: Cannot access a chrome-extension:// URL" error**
  - Other extensions (like youmind, New Tab Override or AI assistant extensions) may be interfering. Try **temporarily disabling other extensions**.
- **Empty data or 'Unauthorized' error**
  - Your Chrome login session may have expired. Navigate to the target site in a new tab and log in again.
- **Node API errors (like parseArgs, fs, etc.)**
  - Ensure Node.js >= 20. Some dependencies require modern Node APIs.
- **Daemon issues**
  - Check status: `curl localhost:19825/status`
  - View logs: `curl localhost:19825/logs`

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=wanghaisheng/openappcli&type=Date)](https://star-history.com/#wanghaisheng/openappcli&Date)

## License

[Apache-2.0](./LICENSE)

---

## 🎯 Final Vision

OpenAppCLI will become **the universal language for application automation** and **the standard bridge for AI Agent application interaction**, just as SQL became the universal language for database queries.

### Core Value Propositions:
1. **Zero Learning Cost** — Any application, one command line to automate
2. **Unlimited Extensibility** — Support any platform, any application type
3. **Intelligent Adaptation** — AI-driven strategy selection and optimization
4. **Open Ecosystem** — Community-driven adapter marketplace
5. **Enterprise-Grade Reliability** — Production environment stability and performance
6. **AI Native Integration** — Seamless integration with all AI Agents through MCP Protocol
7. **Bidirectional Interaction** — Not just data extraction, but complete application behavior control
8. **Standardized Protocol** — Industry-standard tools and resource access

### Impact:
- **Developers** — Liberated from tedious reverse engineering, focus on business logic
- **Enterprises** — Significantly reduce automation costs, improve efficiency
- **Users** — Enjoy more intelligent, more automated application experiences
- **Industry** — Promote standardization and adoption of application automation
- **AI Community** — Provide standardized application interaction capabilities, accelerate AI application deployment
- **Tool Ecosystem** — Establish unified application automation standards, foster ecosystem prosperity

**Ultimately, OpenAppCLI will achieve the vision of "Automate Everything, Enable AI-to-Application Interaction," allowing any application to be easily controlled and automated through both command lines and AI Agents, becoming the universal bridge connecting the digital world and the intelligent world.** 🚀🤖
