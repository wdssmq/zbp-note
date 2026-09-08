# 常见问题

- [常见问题](#常见问题)
  - [链接/图谱/反向链接无法使用，如何启用](#链接图谱反向链接无法使用如何启用)
  - [我不希望 Foam 在所有工作区中启用](#我不希望-foam-在所有工作区中启用)
  - [如何将图谱视图发布到 GitHub Pages 或 Vercel](#如何将图谱视图发布到-github-pages-或-vercel)
  - [Foam 会收集数据吗](#foam-会收集数据吗)

## 链接/图谱/反向链接无法使用，如何启用

- 确保已在 Visual Studio Code 中安装所有[[recommended-extensions]]。
- 运行 `Cmd` + `Shift` + `P`（Windows 使用 `Ctrl` + `Shift` + `P`），输入“reload”，然后运行 **Developer: Reload Window** 命令，使更新后的扩展生效。
- 检查 [[wikilinks]] 中的链接格式规则。

## 我不希望 Foam 在所有工作区中启用

在 Visual Studio Code 中安装的任何扩展默认都会启用。按照 Foam 的设计理念，它无需预先配置即可开箱即用。如果你希望在特定工作区中禁用 Foam，或者默认禁用 Foam、仅在特定工作区中启用，建议遵循 [Visual Studio Code 文档](https://code.visualstudio.com/docs/editor/extension-marketplace#_manage-extensions)中介绍的最佳实践。

## 如何将图谱视图发布到 GitHub Pages 或 Vercel

如果你希望为发布后的 Foam 使用不同的前端样式，并能够查看图谱视图，建议了解以下模板：

- [foam-gatsby](https://github.com/mathieudutour/foam-gatsby-template)，作者：[Mathieu Dutour](https://github.com/mathieudutour)
- [foam-gatsby-kb](https://github.com/hikerpig/foam-template-gatsby-kb)，作者：[hikerpig](https://github.com/hikerpig)

## Foam 会收集数据吗

Foam 会收集匿名使用数据（例如使用了哪些命令、配置了哪些功能），以帮助确定开发优先级。Foam 从不会收集笔记内容、文件名或个人信息。

Foam 遵循 VS Code 的全局遥测设置（`telemetry.telemetryLevel`）。如果你已在 VS Code 中禁用遥测，Foam 将不会发送任何数据。

如需查看发送的内容，请将 Foam 日志级别设置为 `Debug`（在命令面板中运行 `Foam: Set log level`），遥测事件会显示在 Foam 输出通道中。详情请参阅 [[foam-logging-in-vscode]]。

有关收集数据的完整列表和退出方法，请参阅 [[telemetry]]。

[recommended-extensions]: getting-started/recommended-extensions.md "Recommended Extensions"
[wikilinks]: features/wikilinks.md "Wikilinks"
[foam-logging-in-vscode]: tools/foam-logging-in-vscode.md "Foam logging in VsCode"
[telemetry]: tools/telemetry.md "Telemetry"
