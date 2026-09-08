# 使用 Foam

Foam 是一个基于 [Visual Studio Code](https://code.visualstudio.com/) 和 [GitHub](https://github.com/) 构建的个人知识管理系统。它可以帮助你整理研究资料、创建易于发现的笔记并发布你的知识。

> 另请参阅 [[frequently-asked-questions]]。

## 主要功能

- **Wiki 链接** - 使用 `[[双层方括号]]` 语法连接想法
- **块锚点** - 使用 `[[note#^id]]` 链接或嵌入特定的段落、列表项和标题
- **嵌入** - 使用 `![[note]]` 语法包含其他笔记中的内容
- **反向链接** - 自动发现笔记之间的联系
- **图谱可视化** - 以可视化方式查看你的知识网络
- **每日笔记** - 记录带时间戳的想法
- **模板** - 规范笔记创建流程
- **标签** - 整理和筛选内容

## 为什么选择 Foam

- **免费且开源** - 无订阅费用，也不存在厂商锁定
- **数据归你所有** - 笔记以标准 Markdown 文件存储
- **集成 VS Code** - 利用强大的编辑功能和扩展
- **基于 Git** - 内置版本控制和协作功能

Foam 就像浴缸：_你能从中得到什么，取决于你放入了什么。_

## 开始使用

- [[installation]]
- [[get-started-with-vscode]]
- [[recommended-extensions]]
- [[first-workspace]]
- [[note-taking-in-foam]]
- [[sync-notes]]
- [[keyboard-shortcuts]]
- [[search-and-navigate-notes]]

从 Obsidian 转来？请参阅 [[migrating-from-obsidian]]。

## 功能

- [[wikilinks]]
- [[footnotes]]
- [[block-anchors]]
- [[embeds]]
- [[foam-queries]]
- [[smart-folders]]
- [[tags]]
- [[backlinking]]
- [[daily-notes]]
- [[spell-checking]]
- [[graph-view]]
- [[note-properties]]
- [[templates]]
- [[paste-images-from-clipboard]]
- [[custom-markdown-preview-styles]]
- [[link-reference-definitions]]
- [[custom-snippets]]

## 实用方案

[[recipes]] 是用户贡献的实践方案集合，介绍了使用 Foam 或将其与其他工具集成的不同方式。

## 发布

你可以将 Foam 笔记以不同格式发布，供他人阅读和使用。
示例：[[publish-to-github-pages]]、[[generate-gatsby-site]]、[[publish-to-vercel]]

详情请参阅 [[publishing]]。

## 工具

- [[cli]] — 从终端操作你的工作区（`search`、`list`、`daily`、`lint` 等）
- [[workspace-lint]]
- [[orphans]]
- [[foam-logging-in-vscode]]
- [[telemetry]]

[frequently-asked-questions]: frequently-asked-questions.md "常见问题"
[installation]: getting-started/installation.md "Installation"
[get-started-with-vscode]: getting-started/get-started-with-vscode.md "Using Foam with VS Code Features"
[recommended-extensions]: getting-started/recommended-extensions.md "Recommended Extensions"
[first-workspace]: getting-started/first-workspace.md "Creating Your First Workspace"
[note-taking-in-foam]: getting-started/note-taking-in-foam.md "Note-Taking in Foam"
[sync-notes]: getting-started/sync-notes.md "Sync notes with source control"
[keyboard-shortcuts]: getting-started/keyboard-shortcuts.md "Keyboard Shortcuts"
[search-and-navigate-notes]: recipes/search-and-navigate-notes.md "Search and Navigate Notes"
[migrating-from-obsidian]: recipes/migrating-from-obsidian.md "Coming from Obsidian"
[wikilinks]: features/wikilinks.md "Wikilinks"
[footnotes]: features/footnotes.md "Footnotes"
[block-anchors]: features/block-anchors.md "Block Anchors"
[embeds]: features/embeds.md "Note Embeds"
[foam-queries]: features/foam-queries.md "Foam Queries"
[smart-folders]: features/smart-folders.md "Smart Folders"
[tags]: features/tags.md "Tags"
[backlinking]: features/backlinking.md "Backlinks"
[daily-notes]: features/daily-notes.md "Daily Notes"
[spell-checking]: features/spell-checking.md "Spell Checking"
[graph-view]: features/graph-view.md "Graph Visualization"
[note-properties]: features/note-properties.md "Note Properties"
[templates]: features/templates.md "Note Templates"
[paste-images-from-clipboard]: features/paste-images-from-clipboard.md "Paste Images from Clipboard"
[custom-markdown-preview-styles]: features/custom-markdown-preview-styles.md "Custom Markdown Preview Styles"
[link-reference-definitions]: features/link-reference-definitions.md "Link Reference Definitions"
[custom-snippets]: features/custom-snippets.md "Adding Custom Snippets"
[recipes]: recipes/recipes.md "Recipes"
[publish-to-github-pages]: publishing/publish-to-github-pages.md "GitHub Pages"
[generate-gatsby-site]: publishing/generate-gatsby-site.md "Generate a site using Gatsby"
[publish-to-vercel]: publishing/publish-to-vercel.md "Publish to Vercel"
[cli]: tools/cli.md "Foam CLI"
[workspace-lint]: tools/workspace-lint.md "Lint"
[orphans]: tools/orphans.md "Orphaned Notes"
[foam-logging-in-vscode]: tools/foam-logging-in-vscode.md "Foam logging in VsCode"
[telemetry]: tools/telemetry.md "Telemetry"
