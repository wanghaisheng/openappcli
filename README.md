# OpenAppCLI

> **Universal Application Automation Platform - Make any application your CLI.**
> Zero risk · Intelligent adaptation · AI-powered discovery · Multi-platform support

[![中文文档](https://img.shields.io/badge/docs-%E4%B8%AD%E6%96%87-0F766E?style=flat-square)](./README.zh-CN.md)
[![License](https://img.shields.io/npm/l/@jackwener/opencli?style=flat-square)](./LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/wanghaisheng/openappcli?style=flat-square)](https://github.com/wanghaisheng/openappcli)
[![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux%20%7C%20Android%20%7C%20iOS-blue?style=flat-square)](https://github.com/wanghaisheng/openappcli)

A next-generation CLI tool that turns **any application** — websites, Electron apps, desktop software, mobile apps, and games — into a command-line interface. Powered by intelligent strategy selection, adaptive fallback mechanisms, and AI-native discovery.

**Evolved from OpenCLI** — Building on the solid foundation of browser and Electron automation, OpenAppCLI extends to universal application control with vision-based automation, system-level access, and mobile app support.

**Built for the Universal Automation Era** — From desktop Notepad to mobile Instagram, from Unity games to professional software — one platform to automate them all.

**Built for AI Agents** — Configure an instruction in your `AGENT.md` or `.cursorrules` to run `opencli list` via Bash. The AI will automatically discover and invoke all available tools.

**CLI Hub** — Register any local CLI (`opencli register mycli`) so AI agents can discover and call it alongside built-in commands. Auto-installs missing tools via your package manager (e.g. if `gh` isn't installed, `opencli gh ...` runs `brew install gh` first then re-executes seamlessly).

**CLI for Electron Apps** — Turn any Electron application into a CLI tool. Recombine, script, and extend apps like Antigravity Ultra from the terminal. AI agents can now control other AI apps natively.

---

## Highlights

- **🌍 Universal Application Support** — Automate websites, Electron apps, desktop software, mobile apps, and games with a single platform
- **🧠 Intelligent Strategy Selection** — AI-powered detection of optimal automation strategies (CDP → UI Hierarchy → Vision → System API)
- **🔄 Adaptive Fallback Mechanisms** — Automatic degradation to the next best method when primary strategy fails
- **👁️ Advanced Vision Recognition** — SIFT/SURF/ORB feature matching, multi-scale template matching, OCR integration
- **📱 Mobile App Automation** — Android/iOS support via ADB, Frida, and Airtest integration
- **🎮 Game Engine Optimization** — Unity, Unreal, and custom engine support with anti-cheat bypass
- **⚡ High-Performance Execution** — Minicap for fast screenshots, parallel processing, intelligent caching
- **🔧 System-Level Access** — Windows/macOS/Linux APIs, accessibility frameworks, memory access
- **🤖 AI-Native Development** — Automatic adapter generation, performance optimization, error recovery

## Why OpenAppCLI?

There are many great automation tools. Here's when OpenAppCLI is the right choice:

| Your need | Best tool | Why |
|-----------|-----------|-----|
| **Universal application automation** | **OpenAppCLI** | Single platform for web, desktop, mobile, and games |
| **Zero-config desktop app control** | **OpenAppCLI** | Automatic strategy detection and fallback mechanisms |
| **Mobile app automation** | **OpenAppCLI** | Android/iOS support with vision and system-level access |
| **Game automation** | **OpenAppCLI** | Engine-specific optimizations and anti-cheat bypass |
| **Web data extraction** | OpenCLI | Focused on web and Electron apps |
| **Large-scale web crawling** | Crawl4AI, Scrapy | Purpose-built for throughput and scale |
| **General browsing automation** | Browser-Use, Stagehand | LLM-driven general browsing for one-off tasks |

**What makes OpenAppCLI different:**

- **Universal Coverage** — One platform for all application types: Web → Desktop → Mobile → Games
- **Intelligent Adaptation** — AI-driven strategy selection and automatic fallback optimization
- **High Performance** — Minicap screenshots (100x faster), parallel processing, intelligent caching
- **Anti-Detection** — Built-in stealth mode for games and protected applications
- **Developer-Friendly** — Automatic adapter generation, visual debugging, comprehensive tooling
- **Enterprise Ready** — Distributed execution, monitoring, security, and compliance features

> For a detailed comparison with Browser-Use, Crawl4AI, Firecrawl, and others, see the [Comparison Guide](./docs/comparison.md).

---

## Quick Start

### 1. Install OpenAppCLI

**Install via npm (recommended)**

```bash
npm install -g @wanghaisheng/openappcli
```

**Install from source**

```bash
git clone https://github.com/wanghaisheng/openappcli.git && cd openappcli && npm install && npm run build && npm link
```

### 2. Platform Setup

#### For Web & Electron Apps (Browser Bridge)
> OpenAppCLI connects to your browser through a lightweight **Browser Bridge** Chrome Extension + micro-daemon (zero config, auto-start).

1. Go to the GitHub [Releases page](https://github.com/wanghaisheng/openappcli/releases) and download the latest `openappcli-extension.zip`.
2. Unzip the file and open `chrome://extensions`, enable **Developer mode** (top-right toggle).
3. Click **Load unpacked** and select the unzipped folder.

#### For Mobile Apps (Android/iOS)
> Connect your mobile device and install required dependencies.

```bash
# Android setup
opencli mobile setup android
# iOS setup (coming soon)
opencli mobile setup ios
```

#### For Desktop Apps
> System-level access requires administrator privileges on first run.

```bash
# Windows
opencli desktop setup windows --admin
# macOS
opencli desktop setup macos --accessibility
# Linux
opencli desktop setup linux --x11
```

### 3. Verify & Try

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

# Game automation
openappcli discover --app "genshin.exe"
openappcli genshin inventory
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

OpenCLI acts as a universal hub for your existing command-line tools — unified discovery, pure passthrough execution, and auto-install (if a tool isn't installed, OpenCLI runs `brew install <tool>` automatically before re-running the command).

| External CLI | Description | Example |
|--------------|-------------|---------|
| **gh** | GitHub CLI | `opencli gh pr list --limit 5` |
| **obsidian** | Obsidian vault management | `opencli obsidian search query="AI"` |
| **docker** | Docker | `opencli docker ps` |
| **lark-cli** | Lark/Feishu — messages, docs, calendar, tasks, 200+ commands | `opencli lark-cli calendar +agenda` |
| **dingtalk** | DingTalk — cross-platform CLI for DingTalk's full suite, designed for humans and AI agents | `opencli dingtalk msg send --to user "hello"` |
| **wecom** | WeCom/企业微信 — CLI for WeCom open platform, for humans and AI agents | `opencli wecom msg send --to user "hello"` |
| **vercel** | Vercel — deploy projects, manage domains, env vars, logs | `opencli vercel deploy --prod` |

**Register your own** — add any local CLI so AI agents can discover it via `opencli list`:

```bash
opencli register mycli
```

### Desktop App Adapters

Control Electron desktop apps directly from the terminal. Each adapter has its own detailed documentation:

| App | Description | Doc |
|-----|-------------|-----|
| **Cursor** | Control Cursor IDE — Composer, chat, code extraction | [Doc](./docs/adapters/desktop/cursor.md) |
| **Codex** | Drive OpenAI Codex CLI agent headlessly | [Doc](./docs/adapters/desktop/codex.md) |
| **Antigravity** | Control Antigravity Ultra from terminal | [Doc](./docs/adapters/desktop/antigravity.md) |
| **ChatGPT** | Automate ChatGPT macOS desktop app | [Doc](./docs/adapters/desktop/chatgpt.md) |
| **ChatWise** | Multi-LLM client (GPT-4, Claude, Gemini) | [Doc](./docs/adapters/desktop/chatwise.md) |
| **Notion** | Search, read, write Notion pages | [Doc](./docs/adapters/desktop/notion.md) |
| **Discord** | Discord Desktop — messages, channels, servers | [Doc](./docs/adapters/desktop/discord.md) |
| **Doubao** | Control Doubao AI desktop app via CDP | [Doc](./docs/adapters/desktop/doubao-app.md) |

To add a new Electron app, start with [docs/guide/electron-app-cli.md](./docs/guide/electron-app-cli.md).

## Download Support

OpenCLI supports downloading images, videos, and articles from supported platforms.

| Platform | Content Types | Notes |
|----------|---------------|-------|
| **xiaohongshu** | Images, Videos | Downloads all media from a note |
| **bilibili** | Videos | Requires `yt-dlp` installed |
| **twitter** | Images, Videos | From user media tab or single tweet |
| **douban** | Images | Poster / still image lists |
| **pixiv** | Images | Original-quality illustrations, multi-page |
| **zhihu** | Articles (Markdown) | Exports with optional image download |
| **weixin** | Articles (Markdown) | WeChat Official Account articles |

For video downloads, install `yt-dlp` first: `brew install yt-dlp`

```bash
opencli xiaohongshu download abc123 --output ./xhs
opencli bilibili download BV1xxx --output ./bilibili
opencli twitter download elonmusk --limit 20 --output ./twitter
```

## Output Formats

All built-in commands support `--format` / `-f` with `table` (default), `json`, `yaml`, `md`, and `csv`.

```bash
opencli bilibili hot -f json    # Pipe to jq or LLMs
opencli bilibili hot -f csv     # Spreadsheet-friendly
opencli bilibili hot -v         # Verbose: show pipeline debug steps
```

## Exit Codes

opencli follows Unix `sysexits.h` conventions so it integrates naturally with shell pipelines and CI scripts:

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
opencli spotify status || echo "exit $?"   # 69 if browser not running
opencli github issues 2>/dev/null
[ $? -eq 77 ] && opencli github auth       # auto-auth if not logged in
```

## Plugins

Extend OpenCLI with community-contributed adapters:

```bash
opencli plugin install github:user/opencli-plugin-my-tool
opencli plugin list
opencli plugin update --all
opencli plugin uninstall my-tool
```

| Plugin | Type | Description |
|--------|------|-------------|
| [opencli-plugin-github-trending](https://github.com/ByteYue/opencli-plugin-github-trending) | YAML | GitHub Trending repositories |
| [opencli-plugin-hot-digest](https://github.com/ByteYue/opencli-plugin-hot-digest) | TS | Multi-platform trending aggregator |
| [opencli-plugin-juejin](https://github.com/Astro-Han/opencli-plugin-juejin) | YAML | 稀土掘金 (Juejin) hot articles |

See [Plugins Guide](./docs/guide/plugins.md) for creating your own plugin.

## For AI Agents (Developer Guide)

> **Quick mode**: To generate a single command for a specific page URL, see [CLI-ONESHOT.md](./CLI-ONESHOT.md) — just a URL + one-line goal, 4 steps done.

> **Full mode**: Before writing any adapter code, read [CLI-EXPLORER.md](./CLI-EXPLORER.md). It contains the complete browser exploration workflow, the 5-tier authentication strategy decision tree, and debugging guide.

```bash
opencli explore https://example.com --site mysite   # Discover APIs + capabilities
opencli synthesize mysite                            # Generate YAML adapters
opencli generate https://example.com --goal "hot"   # One-shot: explore → synthesize → register
opencli cascade https://api.example.com/data         # Auto-probe: PUBLIC → COOKIE → HEADER
```

## Testing

See **[TESTING.md](./TESTING.md)** for how to run and write tests.

## Troubleshooting

- **"Extension not connected"** — Ensure the Browser Bridge extension is installed and **enabled** in `chrome://extensions`.
- **"attach failed: Cannot access a chrome-extension:// URL"** — Another extension may be interfering. Try disabling other extensions temporarily.
- **Empty data or 'Unauthorized' error** — Your Chrome login session may have expired. Navigate to the target site and log in again.
- **Node API errors** — Ensure Node.js >= 20. Some dependencies require modern Node APIs.
- **Daemon issues** — Check status: `curl localhost:19825/status` · View logs: `curl localhost:19825/logs`

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=jackwener/opencli&type=Date)](https://star-history.com/#jackwener/opencli&Date)

## License

[Apache-2.0](./LICENSE)
