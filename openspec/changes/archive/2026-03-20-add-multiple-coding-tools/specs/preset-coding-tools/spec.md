## ADDED Requirements

### Requirement: Codex 工具支持
扩展 SHALL 支持 Codex CLI 作为预定义编码工具。

#### Scenario: 执行 Codex 命令
- **WHEN** 用户点击 Codex 状态栏图标或执行命令
- **THEN** 系统在终端中执行配置的 Codex 命令

#### Scenario: 配置 Codex 命令
- **WHEN** 用户修改 `quickAI.codexCommand` 配置
- **THEN** 下次执行时使用新的命令字符串

### Requirement: Gemini 工具支持
扩展 SHALL 支持 Gemini CLI 作为预定义编码工具。

#### Scenario: 执行 Gemini 命令
- **WHEN** 用户点击 Gemini 状态栏图标或执行命令
- **THEN** 系统在终端中执行配置的 Gemini 命令

#### Scenario: 配置 Gemini 命令
- **WHEN** 用户修改 `quickAI.geminiCommand` 配置
- **THEN** 下次执行时使用新的命令字符串

### Requirement: Copilot 工具支持
扩展 SHALL 支持 Copilot CLI 作为预定义编码工具。

#### Scenario: 执行 Copilot 命令
- **WHEN** 用户点击 Copilot 状态栏图标或执行命令
- **THEN** 系统在终端中执行配置的 Copilot 命令

#### Scenario: 配置 Copilot 命令
- **WHEN** 用户修改 `quickAI.copilotCommand` 配置
- **THEN** 下次执行时使用新的命令字符串

### Requirement: 状态栏图标显示控制
扩展 SHALL 允许用户控制每个预定义工具的状态栏图标显示。

#### Scenario: 隐藏 Codex 图标
- **WHEN** 用户设置 `quickAI.showCodexIcon` 为 `false`
- **THEN** Codex 状态栏图标不显示

#### Scenario: 显示 Codex 图标
- **WHEN** 用户设置 `quickAI.showCodexIcon` 为 `true`
- **THEN** Codex 状态栏图标显示在状态栏

### Requirement: 默认命令值
每个预定义工具 SHALL 有合理的默认命令值。

#### Scenario: Codex 默认值
- **WHEN** 用户未配置 `quickAI.codexCommand`
- **THEN** 默认值为 `codex -c model_reasoning_effort=high --dangerously-bypass-approvals-and-sandbox -c model_reasoning_summary=detailed -c model_supports_reasoning_summaries=true`

#### Scenario: Gemini 默认值
- **WHEN** 用户未配置 `quickAI.geminiCommand`
- **THEN** 默认值为 `gemini --yolo`

#### Scenario: Copilot 默认值
- **WHEN** 用户未配置 `quickAI.copilotCommand`
- **THEN** 默认值为 `copilot --allow-all`
