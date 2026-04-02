# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- **MCP Protocol Integration**: Native integration with Model Context Protocol for AI Agent interaction
- **AI Agent Native Support**: Standardized tools, resources, and prompts for all AI Agents
- **Bidirectional Application Control**: Not just data extraction, but complete application behavior control
- **Universal Application Support**: Extended from web/Electron to desktop, mobile, and game applications
- **Intelligent Strategy Selection**: AI-driven optimal automation strategy detection and fallback
- **Cross-Platform Unified Interface**: Single platform supporting Windows, macOS, Linux, Android, iOS
- **MCP Prompt System**: Intelligent task templates for complex automation workflows

### Changed
- **Project Name**: Evolution from OpenCLI to OpenAppCLI
- **Core Architecture**: From data extraction tool to application interaction platform
- **Target Audience**: From CLI users to both CLI users and AI Agents
- **Value Proposition**: From "Make any application your CLI" to "Make any application your CLI and AI partner"

### Deprecated
- OpenCLI branding (replaced by OpenAppCLI)

## [2.0.0] - 2026-04-02

### Added
- **Universal Application Automation Platform**: Support for desktop, mobile, and game applications
- **AI-Powered Discovery**: Automatic adapter generation and capability detection
- **Intelligent Strategy Selection**: AI-driven optimal automation strategy detection
- **Adaptive Fallback Mechanisms**: Automatic degradation to next best method
- **Advanced Vision Recognition**: SIFT/SURF/ORB feature matching, multi-scale template matching
- **System-Level Access**: Windows/macOS/Linux APIs, accessibility frameworks
- **Mobile App Automation**: Android/iOS support via ADB, UIAutomator, Frida
- **Game Engine Optimization**: Unity, Unreal, and custom engine support
- **High-Performance Execution**: Minicap for fast screenshots, parallel processing
- **CLI Hub**: Unified discovery and execution for external CLI tools

### Changed
- **Architecture**: Extended from browser-only to universal application support
- **Performance**: 100x faster screenshots with Minicap integration
- **Compatibility**: Cross-platform support for all major operating systems

## [1.5.0] - 2025-12-15

### Added
- **Electron App CLI Generation**: Turn any Electron application into a CLI tool
- **AI Agent Compatibility**: Configure instructions for AI agents to discover and use OpenCLI
- **External CLI Hub**: Register and manage external CLI tools
- **Auto-Installation**: Automatic installation of missing tools via package managers
- **Browser Bridge**: Lightweight Chrome extension for browser communication
- **Micro-Daemon**: Background service for browser communication

### Changed
- **Browser Integration**: Improved stability and performance
- **Adapter Framework**: Enhanced TypeScript adapter development
- **Documentation**: Comprehensive developer guides and API documentation

## [1.0.0] - 2025-10-01

### Added
- **Initial Release**: OpenCLI as a web and Electron automation platform
- **Browser Automation**: Chrome DevTools Protocol integration
- **YAML Declarative Adapters**: Simple configuration-based adapters
- **TypeScript Programmatic Adapters**: Advanced control with TypeScript
- **50+ Built-in Site Adapters**: Support for popular websites and services
- **AI-Assisted Development**: Automatic discovery and code generation
- **Anti-Detection**: Stealth mode for protected applications
- **Plugin System**: Extensible architecture for community contributions

### Security
- **Secure Browser Communication**: Encrypted communication between CLI and browser
- **Permission Management**: Granular control over automation capabilities
- **Data Privacy**: Local-only processing, no data transmission to external services

---

## Version History

### Version 2.0.0 (MCP Integration Era)
- **Focus**: AI Agent integration and universal application support
- **Innovation**: First platform to bridge AI Agents with any application
- **Impact**: Revolutionizing application automation for the AI era

### Version 1.5.0 (CLI Hub Era)  
- **Focus**: CLI tool unification and Electron app support
- **Innovation**: First platform to turn any app into a CLI tool
- **Impact**: Expanding automation beyond web applications

### Version 1.0.0 (Web Automation Era)
- **Focus**: Web and Electron application automation
- **Innovation**: AI-powered adapter generation
- **Impact**: Democratizing web automation

---

## Migration Guide

### From OpenCLI to OpenAppCLI

#### Package Installation
```bash
# Old
npm install -g @jackwener/opencli

# New
npm install -g @wanghaisheng/openappcli
```

#### Command Usage
```bash
# Old
opencli bilibili hot

# New
openappcli bilibili hot
```

#### MCP Integration
```bash
# Start MCP server
openappcli mcp start

# AI Agent integration
ai-agent "Extract Bilibili hot videos using OpenAppCLI"
```

### From 1.x to 2.0

#### New Features
- MCP Protocol integration
- Universal application support
- AI Agent native interaction
- Bidirectional application control

#### Breaking Changes
- Package name change
- Some internal API changes
- Configuration format updates

#### Compatibility
- All existing adapters remain compatible
- CLI commands maintain backward compatibility
- Configuration files automatically migrated

---

## Contributing

We welcome contributions to the OpenAppCLI project! Please see our [Contributing Guide](./CONTRIBUTING.md) for details.

### Development Setup
```bash
# Clone the repository
git clone https://github.com/wanghaisheng/openappcli.git
cd openappcli

# Install dependencies
npm install

# Run tests
npm test

# Build the project
npm run build
```

### MCP Integration Development
```bash
# Test MCP server
npm run test:mcp

# Start development server
npm run dev:mcp
```

---

## Support

- **Documentation**: [https://github.com/wanghaisheng/openappcli/docs](https://github.com/wanghaisheng/openappcli/docs)
- **Issues**: [https://github.com/wanghaisheng/openappcli/issues](https://github.com/wanghaisheng/openappcli/issues)
- **Discussions**: [https://github.com/wanghaisheng/openappcli/discussions](https://github.com/wanghaisheng/openappcli/discussions)
- **Community**: [https://discord.gg/openappcli](https://discord.gg/openappcli)

---

## License

OpenAppCLI is licensed under the [Apache License 2.0](https://github.com/wanghaisheng/openappcli/blob/main/LICENSE).

---

## Acknowledgments

- **OpenCLI Community**: For the solid foundation and pioneering work in web automation
- **MCP Protocol**: For providing the standard for AI Agent interaction
- **Contributors**: All the developers and users who have helped shape OpenAppCLI
- **AI Community**: For inspiring the vision of AI-native application interaction

---

*For more detailed information about specific releases, please see the [GitHub Releases](https://github.com/wanghaisheng/openappcli/releases) page.*
