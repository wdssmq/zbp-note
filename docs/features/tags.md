# 标签

除了 wikilink 和文件夹之外，标签还可以灵活地对笔记进行分类和组织。

## 创建标签

### 行内标签

直接在笔记内容中添加标签：

```markdown
# Machine Learning Fundamentals

This covers basic algorithms and applications.

#machine-learning #data-science #algorithms #beginner
```

### Front Matter 标签

在 YAML front matter 中添加标签：

```markdown
---
tags: [machine-learning, data-science, algorithms, beginner]
---
```

### 层级标签

使用正斜杠创建标签层级：

```markdown
#programming/languages/python
#programming/frameworks/react
#work/projects/website-redesign
#personal/health/exercise
```

## 自动补全

输入 `#` 会显示已有标签。在 front matter 中，使用 `Ctrl+Space` 获取标签建议。

## 标签资源管理器

使用 VS Code 侧边栏中的 Tag Explorer 面板可以：

- 浏览标签层级结构
- 按标签名称筛选
- 点击标签查看所有关联笔记
- 查看标签使用次数
- 搜索标签（点击搜索图标或使用“Foam: Search Tag”命令）

标签也会显示在 [[graph-view]] 中，并且可以自定义颜色。

## 搜索标签

搜索工作区中某个标签的所有出现位置：

1. 使用命令面板中的“Foam: Search Tag”
2. 或点击 Tag Explorer 面板中标签旁的搜索图标

结果会显示在 VS Code 的搜索面板中，你可以在匹配项之间导航。

> 已知限制：此命令利用 VS Code 的搜索功能，因此会受到正则表达式的限制。搜索结果仅供参考，可能会出现一些误匹配。

## 自定义标签样式

通过添加 CSS 自定义 Markdown 预览中的标签外观：

1. 创建 `.foam/css/custom-tag-style.css`
2. 添加针对 `.foam-tag` 类的 CSS：
   ```css
   .foam-tag {
     color: #ffffff;
     background-color: #000000;
   }
   ```
3. 更新 `.vscode/settings.json`：
   ```json
   {
     "markdown.styles": [".foam/css/custom-tag-style.css"]
   }
   ```

## 标签与反向链接

有些用户更喜欢使用反向链接（例如链接到 `book` 笔记），而不是使用 #book 标签进行分类。两种方式都可行，请选择适合自己工作流的方式。

要从终端管理标签，请参阅 [[tag|CLI tag command]]。

[graph-view]: graph-view.md 'Graph Visualization'
[tag]: ../tools/cli/tag.md 'foam tag'
