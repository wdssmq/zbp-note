# 在 Foam 中记笔记

高效记笔记是任何知识管理系统的基础。在 Foam 中，你将使用 Markdown 编写笔记。这是一种简单而强大的格式，既便于人类阅读，也得到广泛支持。本指南将介绍在 Foam 中写好笔记所需了解的一切。

## Markdown 基础

Markdown 是一种轻量级标记语言，使用简单语法格式化文本。以下是基础内容：

### 标题

```markdown
# 标题 1（主标题）

## 标题 2（主要章节）

### 标题 3（子章节）

#### 标题 4（次要章节）
```

### 文本格式

```markdown
**粗体文本**
_斜体文本_
**_粗体和斜体_**
~~删除线~~
`行内代码`
```

### 列表

```markdown
## 无序列表

- 第一项
- 第二项
  - 嵌套项
  - 另一个嵌套项

## 有序列表

1. 第一步
2. 第二步
   1. 子步骤
   2. 另一个子步骤
```

### 链接和图片

```markdown
[外部链接](https://example.com)
![图片说明](./assets/images/screenshot.png)
```

### Code Blocks

````markdown
```javascript
function greet(name) {
  return `你好，${name}！`;
}
```
````

### 表格

```markdown
| 第 1 列  | 第 2 列  | 第 3 列  |
| -------- | -------- | -------- |
| 数据 1   | 数据 2   | 数据 3   |
| 数据 4   | 数据 5   | 数据 6   |
```

### 引用和分隔线

```markdown
> 这是引用或重要笔记
> 它可以跨越多行

---

使用三个短横线创建水平分隔线
```

_[📹 观看：记笔记所需的 Markdown 语法基础]_

## Foam 专属功能

除了标准 Markdown 外，Foam 还添加了多个强大功能：

### Wikilink

使用双括号连接笔记：

```markdown
我正在阅读 [[Project Management]] 以及它与 [[Personal Productivity]] 的关系。

这与 [[2025-01-25-daily-note]] 相连接，我最初就是在那里产生这个想法的。
```

### 笔记嵌入

通过 [[embeds]] 包含其他笔记中的内容：

```markdown
![[Project Management#Key Principles]]

这会嵌入 Project Management 笔记中的“关键原则”章节。
```

### 标签

使用 [[tags]] 组织内容：

```markdown
#productivity #learning #foam

标签可以放在笔记的任意位置，帮助组织和筛选内容。
```

使用嵌套标签进行更好的组织：

```markdown
#work/projects/website
#learning/programming/javascript
#personal/health/exercise
```

这些标签会在 [Tag Explorer](../features/tags.md) 中以树形结构显示。

### 笔记属性（YAML Front Matter）

为笔记添加元数据：

```markdown
---
title: '高级记笔记策略'
tags: [productivity, learning, methods]
created: 2025-01-25
modified: 2025-01-25
status: draft
---

# 高级记笔记策略

在此填写笔记内容……
```

## 写出高效笔记

### 原子化原则

每篇笔记都应专注于一个概念或想法：

**正确示例：**

```markdown
# 费曼技巧

一种学习方法：像向他人授课一样，用简单的语言解释一个概念。

## 步骤

1. 选择要学习的主题
2. 用简单的语言进行解释
3. 找出理解上的空白
4. 简化内容并使用类比

## 为什么有效

- 迫使自己主动参与材料学习
- 快速暴露知识空白
- 通过讲授提高记忆保持度

相关内容：[[Active Learning]] [[Study Methods]]
```

**避免：**
在一篇笔记中混合多个无关概念。

### 使用描述性标题

笔记标题应清晰表明内容：

**推荐：** `REST API Design Principles`
**推荐：** `Meeting Notes - Product Roadmap Review 2025-01-25`
**避免：** `Stuff I Learned Today`
**避免：** `Notes`

### 大胆建立链接

即使目标笔记尚不存在，也不要犹豫，尽管创建链接：

```markdown
# 机器学习基础

机器学习是 [[Artificial Intelligence]] 的一个分支，专注于创建能够从 [[Data]] 中学习的算法。

关键概念包括：

- [[Supervised Learning]]
- [[Unsupervised Learning]]
- [[Neural Networks]]
- [[Feature Engineering]]

这与我在 [[Customer Behavior Analysis]] 和 [[Predictive Analytics]] 方面的工作相关。
```

Foam 会为缺失的笔记创建占位页面，方便之后填补知识空白。

## 键盘快捷键

记笔记时常用的 VS Code 快捷键：

| 快捷键                        | 操作                  |
| ------------------------------ | --------------------- |
| `Ctrl+N` / `Cmd+N`             | 新建文件              |
| `Ctrl+S` / `Cmd+S`             | 保存文件              |
| `Ctrl+P` / `Cmd+P`             | 快速打开文件          |
| `Ctrl+Shift+P` / `Cmd+Shift+P` | 命令面板              |
| `Ctrl+K V` / `Cmd+K V`         | 打开 Markdown 预览    |
| `Ctrl+[` / `Cmd+[`             | 减少缩进              |
| `Ctrl+]` / `Cmd+]`             | 增加缩进              |
| `Alt+Z` / `Option+Z`           | 切换自动换行          |

## 接下来做什么

了解记笔记基础后：

1. **[[navigation]]** - 学习使用 wikilink 在笔记之间高效移动
2. **[探索图谱视图](../features/graph-view.md)** - 将知识库中的连接可视化
3. **[设置模板](../features/templates.md)** - 创建可重复使用的笔记结构
4. **[使用每日笔记](../features/daily-notes.md)** - 建立每日记录习惯

[embeds]: ../features/embeds.md "Note Embeds"
[tags]: ../features/tags.md "标签"
[navigation]: navigation.md "Navigation in Foam"
