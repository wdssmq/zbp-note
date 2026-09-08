# 安装

开始使用 Foam 非常简单。本指南将带你安装开启知识管理之旅所需的一切。

## 第 1 步：安装 Visual Studio Code

Foam 基于微软免费开源的代码编辑器 VS Code 构建。你可以从 https://code.visualstudio.com/ 下载。

### 为什么选择 VS Code

VS Code 提供：

- 出色的 Markdown 编辑功能
- 丰富的扩展生态系统
- 跨平台兼容性
- 集成终端和 Git 支持
- 可自定义的界面和快捷键

要详细了解如何将 VS Code 与 Foam 搭配使用，请参阅 [[get-started-with-vscode]]。

## 第 2 步：安装 Foam 扩展

Foam 扩展为 VS Code 增添强大的知识管理功能。

1. **打开 VS Code**
2. **点击侧边栏中的扩展图标**（或按 `Ctrl+Shift+X` / `Cmd+Shift+X`）
3. **在扩展市场中搜索“Foam”**
4. **点击由 Foam Team 发布的官方 Foam 扩展中的“安装”**
5. **根据提示重新加载 VS Code**

### Foam 扩展提供的功能

- Wiki 链接自动补全和导航
- 反向链接发现和面板
- 图谱可视化
- 强大的笔记模板引擎
- 每日笔记功能

## 第 3 步：安装推荐扩展

虽然 Foam 可以独立运行，但它主要关注笔记之间的连接。你可以安装其他扩展，以改善编辑体验或增强笔记功能。

### 实用扩展

- **Markdown All in One** - 丰富的 Markdown 编辑功能，强烈推荐。

其他扩展：

- **Spell Right** - 检查笔记中的拼写
- **Paste Image** - 轻松从剪贴板插入图片
- **Todo Tree** - 跟踪工作区中的 TODO 项

## 可选：安装 Foam CLI

Foam CLI 让你无需打开 VS Code，即可从终端操作工作区，包括搜索笔记、管理标签、创建每日笔记等。

```bash
npm install -g foam-cli
```

安装完成后，运行 `foam --help` 查看可用命令，或参阅 [[cli|CLI 文档]] 了解详情。

## 接下来做什么

现在 Foam 已安装完成，你可以：

1. **[[first-workspace]]** - 设置知识库结构
2. **[[get-started-with-vscode]]** - 学习如何使用 VS Code 记笔记
3. **[[note-taking-in-foam]]** - 编写你的第一篇 Markdown 笔记
4. **[[navigation]]** - 使用 Wiki 链接连接你的想法
5. **[[graph-view]]** - 将知识网络可视化

## 获取帮助

如果遇到问题：

- 查看 [[frequently-asked-questions]] 了解常见问题
- 访问 [Foam 社区 Discord](https://discord.com/invite/HV2tn2FpEk)
- 浏览 [GitHub Issues](https://github.com/foambubble/foam/issues) 查找已知问题
- 在 [GitHub Discussions](https://github.com/foambubble/foam/discussions) 中提问

[get-started-with-vscode]: get-started-with-vscode.md "使用 VS Code 功能配合 Foam"
[cli|CLI 文档]: ../tools/cli.md "Foam CLI"
[first-workspace]: first-workspace.md "创建你的第一个工作区"
[note-taking-in-foam]: note-taking-in-foam.md "在 Foam 中记笔记"
[navigation]: navigation.md "Navigation in Foam"
[graph-view]: ../features/graph-view.md "图谱可视化"
[frequently-asked-questions]: ../frequently-asked-questions.md "常见问题"
