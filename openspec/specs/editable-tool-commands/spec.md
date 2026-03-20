## ADDED Requirements

### Requirement: 命令字符串完全可编辑
扩展 SHALL 允许用户通过 VS Code 设置完全编辑每个预定义工具的命令字符串。

#### Scenario: 修改 Codex 命令参数
- **WHEN** 用户在 settings.json 中修改 `quickAI.codexCommand` 的值
- **THEN** 新的命令字符串被保存并立即生效

#### Scenario: 修改 Gemini 命令参数
- **WHEN** 用户在 VS Code 设置 UI 中修改 Gemini 命令
- **THEN** 新的命令字符串被保存并立即生效

#### Scenario: 修改 Copilot 命令参数
- **WHEN** 用户在 settings.json 中修改 `quickAI.copilotCommand` 的值
- **THEN** 新的命令字符串被保存并立即生效

### Requirement: 配置变更热重载
扩展 SHALL 在配置变更时自动重新加载命令字符串，无需重启 VS Code。

#### Scenario: 配置变更后执行
- **GIVEN** 用户修改了某个工具的命令配置
- **WHEN** 用户点击对应的状态栏图标
- **THEN** 系统使用最新的命令字符串执行

### Requirement: 配置类型安全
扩展 SHALL 在 package.json 中定义配置项的类型为字符串。

#### Scenario: 配置验证
- **WHEN** 用户在 settings.json 中编辑命令配置
- **THEN** VS Code 将值视为字符串类型，不验证格式
