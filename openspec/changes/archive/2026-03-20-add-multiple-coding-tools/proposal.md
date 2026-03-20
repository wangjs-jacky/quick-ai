## Why

当前 Quick AI 扩展仅支持 Claude 和 Opencode 两个 CLI 工具。随着 AI 编码助手生态的发展，用户需要快速访问更多编码工具（Codex、Gemini、Copilot）。将这些工具作为内置预设，可以简化用户配置流程，同时保持命令参数的可编辑性，满足不同场景需求。

## What Changes

- 在扩展配置中添加三个预定义编码工具：Codex、Gemini、Copilot
- 每个工具都有默认的命令模板和可编辑的命令参数字段
- 在状态栏为每个工具添加快捷入口（可通过配置开关显示/隐藏）
- 支持通过 VS Code 设置界面直接编辑每个工具的完整命令

## Capabilities

### New Capabilities
- `preset-coding-tools`: 预定义编码工具的管理、配置和状态栏展示
- `editable-tool-commands`: 可编辑的工具命令配置系统

### Modified Capabilities
- (无现有能力需要修改)

## Impact

- **extension.ts**: 添加新的命令注册、状态栏图标创建逻辑
- **package.json**: 扩展 contributes.configuration 添加三个工具的配置项
- 用户配置: 新增 `quickAI.codexCommand`, `quickAI.geminiCommand`, `quickAI.copilotCommand` 等配置
