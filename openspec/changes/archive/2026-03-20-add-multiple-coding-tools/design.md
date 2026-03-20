## Context

当前 Quick AI 扩展通过 `extension.ts` 管理命令执行和状态栏图标展示。已有 Claude 和 Opencode 的硬编码实现，以及一个灵活的 `customCommands` 配置系统允许用户自定义命令。

本项目是一个 VS Code 扩展，用户主要通过 settings.json 或 VS Code 设置界面进行配置。

## Goals / Non-Goals

**Goals:**
- 将 Codex、Gemini、Copilot 作为一等公民集成到扩展中
- 提供合理的默认命令，同时允许用户完全自定义
- 保持与现有 Claude/Opencode 实现一致的用户体验
- 复用现有的状态栏图标和终端管理逻辑

**Non-Goals:**
- 不实现命令参数的 GUI 编辑器（使用 VS Code 原生 settings 界面）
- 不自动安装 CLI 工具（假设用户已安装）
- 不改变现有的自定义命令系统架构

## Decisions

### 方案选择：扩展现有模式 vs 重构为通用系统

**选择**: 扩展现有模式（硬编码配置项）

**理由**:
- 简单直接，与 Claude/Opencode 实现保持一致
- VS Code 的 settings UI 对具体配置项有更好的支持
- 避免过度设计，三个工具数量可控

**替代方案**: 重构为可配置的工具列表
- 拒绝原因：会增加复杂度，且不符合当前代码风格

### 配置结构设计

每个工具使用独立的配置项：
```json
"quickAI.codexCommand": "codex -c model_reasoning_effort=high ...",
"quickAI.geminiCommand": "gemini --yolo",
"quickAI.copilotCommand": "copilot --allow-all"
```

**理由**:
- 清晰的命名空间，便于用户查找和编辑
- VS Code 会为每个配置项生成独立的设置 UI
- 支持每个工具的单独开关控制

## Risks / Trade-offs

**[Risk] 命令参数可能随 CLI 版本变化**
→ Mitigation: 配置项允许用户完全编辑，不受默认值的限制

**[Risk] 状态栏图标过多导致拥挤**
→ Mitigation: 每个工具都有独立的 `showXxxIcon` 开关配置

**[Trade-off] 硬编码配置项 vs 完全动态配置**
- 硬编码提供了更好的 IDE 支持和文档
- 代价是新增工具需要修改代码（当前可接受）
