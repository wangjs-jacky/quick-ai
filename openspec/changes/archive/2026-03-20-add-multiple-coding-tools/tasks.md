## 1. Package.json 配置扩展

- [x] 1.1 在 contributes.configuration.properties 中添加 `quickAI.showCodexIcon` 配置项（布尔类型，默认 true）
- [x] 1.2 添加 `quickAI.showGeminiIcon` 配置项（布尔类型，默认 true）
- [x] 1.3 添加 `quickAI.showCopilotIcon` 配置项（布尔类型，默认 true）
- [x] 1.4 添加 `quickAI.codexCommand` 配置项（字符串类型，默认含完整参数）
- [x] 1.5 添加 `quickAI.geminiCommand` 配置项（字符串类型，默认 `gemini --yolo`）
- [x] 1.6 添加 `quickAI.copilotCommand` 配置项（字符串类型，默认 `copilot --allow-all`）
- [x] 1.7 在 contributes.commands 中注册三个新命令（quickCodexCommand, quickGeminiCommand, quickCopilotCommand）

## 2. Extension.ts 核心实现

- [x] 2.1 添加状态栏项引用变量（codexStatusBarItem, geminiStatusBarItem, copilotStatusBarItem）
- [x] 2.2 更新 getConfig() 函数，读取三个新工具的命令和显示配置
- [x] 2.3 在 activate() 中注册三个新命令（executeQuickCodex, executeQuickGemini, executeQuickCopilot）
- [x] 2.4 更新 createStatusBarItems()，添加三个新工具的状态栏图标创建逻辑
- [x] 2.5 更新 disposeStatusBarItems()，清理三个新状态栏项
- [x] 2.6 实现 executeQuickCodex() 函数，发送 codexCommand 到终端
- [x] 2.7 实现 executeQuickGemini() 函数，发送 geminiCommand 到终端
- [x] 2.8 实现 executeQuickCopilot() 函数，发送 copilotCommand 到终端

## 3. 配置变更热重载

- [x] 3.1 验证配置监听器已覆盖新配置项（确认 affectsConfiguration('quickAI') 能捕获变更）

## 4. 测试与验证

- [x] 4.1 验证 Codex 状态栏图标显示/隐藏功能正常
- [x] 4.2 验证 Gemini 状态栏图标显示/隐藏功能正常
- [x] 4.3 验证 Copilot 状态栏图标显示/隐藏功能正常
- [x] 4.4 验证修改命令配置后，下次执行使用新命令
- [x] 4.5 验证默认命令值符合预期
