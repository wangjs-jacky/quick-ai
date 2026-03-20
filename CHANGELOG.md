# Changelog

All notable changes to this project will be documented in this file.

## [0.0.6] - 2026-03-20

### Added

- 新增 Codex、Gemini、Copilot 三款 AI 编程工具支持
- 每个工具均可通过配置开启/关闭状态栏图标（`showCodexIcon`、`showGeminiIcon`、`showCopilotIcon`）
- 每个工具支持自定义命令配置（`codexCommand`、`geminiCommand`、`copilotCommand`）
- 默认仅显示 Claude、Opencode、Codex 图标，Warp、Gemini、Copilot 默认隐藏

## [0.0.5] - 2025-02-21

### Fixed

- 修复 0.0.4 版本发布问题，确保 CLI 命令配置（`claudeCommand`、`opencodeCommand`）正确包含

## [0.0.4] - 2025-02-20

### Added

- 支持 CLI 命令配置（`claudeCommand`、`opencodeCommand`）
- 支持自定义命令配置（`customCommands`），可在状态栏添加任意命令

## [0.0.3] - 2025-02-12

### Added

- 支持多文件夹工作区选择功能
- 更新发布流程，支持同时发布到 VS Code Marketplace 和 Open VSX Registry

## [0.0.2] - 2025-02-12

### Added

- 添加 MIT 许可证
- 添加中文文档（README.zh-CN.md）
- 添加仓库元数据（issues、homepage）

## [0.0.1] - 2025-02-08

### Added

- 初始发布
- 状态栏图标：Warp、Claude、Opencode 快速访问
- 快捷键支持：`Cmd+Shift+C`（Claude）、`Cmd+Shift+O`（Opencode）
- 可配置图标显示/隐藏
- 可配置图标样式（仅图标或图标+文字）
- 可配置终端位置（面板或编辑器标签页）

[0.0.6]: https://github.com/wangjs-jacky/quick-ai/compare/v0.0.5...v0.0.6
[0.0.5]: https://github.com/wangjs-jacky/quick-ai/compare/v0.0.4...v0.0.5
[0.0.4]: https://github.com/wangjs-jacky/quick-ai/compare/v0.0.3...v0.0.4
[0.0.3]: https://github.com/wangjs-jacky/quick-ai/compare/v0.0.2...v0.0.3
[0.0.2]: https://github.com/wangjs-jacky/quick-ai/compare/v0.0.1...v0.0.2
[0.0.1]: https://github.com/wangjs-jacky/quick-ai/releases/tag/v0.0.1
