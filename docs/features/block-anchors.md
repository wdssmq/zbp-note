# 块锚点

块锚点可以链接到笔记中的特定段落、列表项、标题或引用块，而不仅仅是整篇笔记或某个章节标题。

## 添加块锚点

将 `^your-id` 放在任意块元素的末尾。ID 可以包含字母、数字和连字符。

`^id` 标记会在预览中隐藏，它属于元数据，不是可见文本。

### 段落

```markdown
This is an important finding from the experiment. ^key-finding
```

多行段落同样适用，将锚点放在最后一行的末尾：

```markdown
The first measurements were inconclusive.
After repeating the experiment, results became clear. ^experiment-result
```

### 列表项

将锚点放在列表项文本的末尾。Foam 会锚定整个列表项，包括其中的子项：

```markdown
- Mix dry ingredients thoroughly ^dry-step
  - 2 cups flour
  - 1 tsp salt
- Add wet ingredients ^wet-step
```

要锚定整个列表，请将 `^id` 单独放在最后一个列表项之后的紧邻一行（中间不要有空行）：

```markdown
- First item
- Second item
- Third item
^shopping-list
```

### 标题

```markdown
## Methodology ^methodology
```

锚点只应用于标题行本身，不会应用于下面的整个章节。

### 引用块

支持以下三种放置方式：

**作为引用块中的最后一行：**

```markdown
> The only way to do great work is to love what you do.
> ^jobs-quote
```

**单独放在引用块之后的紧邻一行：**

```markdown
> We shall fight on the beaches,
> we shall fight on the landing grounds.
^churchill-beaches
```

**在引用块后空一行**（如果 Markdown 格式化工具会自动插入空行，这种方式很有用）：

```markdown
> We shall fight on the beaches,
> we shall fight on the landing grounds.

^churchill-beaches
```

### 代码块

将 `^id` 单独放在结束围栏之后的一行。围栏和 `^id` 之间有一个空行也可以接受（如果 Markdown 格式化工具会自动添加空行，这种方式很有用）：

````markdown
```python
def greet(name):
    return f"Hello, {name}"
```
^greet-function
````

### 表格

将 `^id` 单独放在表格之后的一行。中间有一个空行也可以接受：

```markdown
| Name  | Score |
| ----- | ----- |
| Alice | 95    |
| Bob   | 87    |
^results-table
```

## 链接到块

使用 `[[note-name#^blockid]]` 直接链接到块：

```markdown
[[research-notes#^key-insight]]
[[research-notes#^list-ref]]
```

在 wikilink 中输入 `#^` 时，Foam 会为块 ID 提供自动补全。

你还可以添加显示文本：

```markdown
[[research-notes#^key-insight|See the key insight]]
```

## 嵌入块

使用 `![[note-name#^blockid]]` 将该块直接嵌入正文：

```markdown
![[research-notes#^key-insight]]
```

只会显示被引用块的内容，不会显示整篇笔记。

## 重命名块 ID

将光标放在 `^blockid` 锚点上并按 `F2` 可重命名它。Foam 会更新工作区中该锚点及所有引用它的 wikilink。

## 诊断

当块链接指向目标笔记中不存在的 `^id` 时，Foam 会发出警告。通过快速修复可以从可用的块 ID 中选择。

如果在同一文件中意外使用了两次相同的 `^id`，Foam 会发出重复标记警告。快速修复会将其替换为新生成的唯一 ID。

## 相关内容

- [[wikilinks]] - General linking
- [[footnotes]] - Adding references and side notes
- [[embeds]] - Embedding notes and blocks

[wikilinks]: wikilinks.md "Wikilink"
[footnotes]: footnotes.md "Footnotes"
[embeds]: embeds.md "Note Embeds"
