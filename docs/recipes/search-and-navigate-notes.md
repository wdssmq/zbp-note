# 搜索和浏览笔记

本 `#recipe` 介绍在 Foam 中查找和浏览笔记的方式。

## 快速打开

按 `Cmd+P`（Windows 上为 `Ctrl+P`），输入笔记名称即可直接打开。支持部分匹配，例如 `proj meet` 可以找到 `projects/meeting-notes.md`。

## 全文搜索

按 `Cmd+Shift+F`（Windows 上为 `Ctrl+Shift+F`）搜索所有笔记内容。使用筛选图标可以将搜索范围限制为特定文件夹或文件类型。

## 笔记导航器面板

侧边栏中的 **Note Navigator** 面板可以浏览和筛选工作区中的所有笔记。使用筛选输入框按名称缩小范围，并通过面板工具栏在平铺视图和按文件夹分组的视图之间切换。

## 其他面板

Foam 在侧边栏中添加了多个面板，帮助你发现笔记：

- **Backlinks** — 显示哪些笔记链接到了当前打开的笔记
- **Placeholders** — 列出尚未有对应文件的 wikilink
- **Orphans** — 列出没有入链或出链的笔记（参见 [[orphans]]）
- **Tags** — 浏览所有标签并跳转到带标签的笔记（参见 [[tags]]）

## 图谱视图

[[graph-view]] 提供整个知识库的可视化概览。点击任意节点即可打开对应笔记。你还可以按标签、类型、路径或标题[[resource-filters|筛选图谱]]，聚焦于部分笔记。

## 随机笔记

从命令面板运行 **“Foam: Open Random Note”**，重新发现被遗忘的笔记。

[orphans]: ../tools/orphans.md "Orphaned Notes"
[tags]: ../features/tags.md "标签"
[graph-view]: ../features/graph-view.md "图谱可视化"
[resource-filters|筛选图谱]: ../features/resource-filters.md "Resource Filters"
