# 导入与恢复

## 应用前

打开设置 → 外观，记录当前模式和账号强调色选项。在深色主题栏点击「复制主题」，把完整分享串保存到本地。这是恢复个性化配色与字体覆盖的依据，不要用一份默认主题代替备份。

## 导入

复制 `theme/Ziye-Cyber-Dream.codex-theme.txt` 的全部内容，然后在「深色主题 → 导入」中粘贴、提交。不要只复制 JSON，不要附带 Markdown 围栏。此入口接受分享文本，不是 VS Code 扩展安装，也不是 CSS 导入。

此方案的关键字段如下：

| 设置 | 值 |
|---|---|
| variant | dark |
| codeThemeId | catppuccin |
| surface / ink | #171326 / #EAE2FF |
| accent / accentSource | #B89BFF / custom |
| semanticColors.diffAdded | #A6E3A1 |
| semanticColors.diffRemoved | #F5A6E8 |
| semanticColors.skill | #B89BFF |
| contrast | 60 |
| fonts.code / fonts.ui | null / null，使用应用默认字体 |
| opaqueWindows | false，不强制侧边栏不透明 |

导入会覆盖当前深色主题槽位中的这些字段，包括取消已有的 UI / 代码字体覆盖。字号、浅色主题、动效、Diff 标记样式和模式不在此分享串中。若系统当时为浅色，需要另行切换到深色模式才会显示本方案。

应用的强调色机制可能将自定义色对应到最接近的账号命名色并同步；这不是保证只在本机生效的配置。原生分享结构没有自定义主题显示名称字段，选择器仍可能显示 Catppuccin。

## 检查

应用后检查首页、任务卡片、输入框、焦点边框、代码与 Diff。确认中文字体、代码文字、注释、选中文字、悬停和状态提示在你的显示器上清晰可读。透明效果会受 Windows 桌面背景和应用支持影响。

## 恢复

在同一个深色主题栏导入应用前保存的完整分享串，再恢复原来的 System / Dark / Light 模式。如果账号强调色发生了同步变化，也把账号强调色选回原来的选项。

如果导入按钮不可用，检查是否选择了深色主题栏、前缀是否完整、内置 Catppuccin 是否存在，以及桌面版是否仍支持此格式。不要直接覆盖全局状态文件或把主题写进 `config.toml`。

## 预览说明

`preview/preview.html` 可离线打开，内含配色模拟和复制按钮。它不会连接或修改 Codex。示意图中的布局、角色位置、文案不属于主题导入功能。

`theme/Ziye-Cyber-Dream.reference.json` 是便于阅读的字段参考，导入时请使用 TXT 版本。
