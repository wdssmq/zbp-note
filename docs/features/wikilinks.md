# Wikilink

Wikilink 是使用 `[[双括号]]` 语法连接知识库中文件的内部链接。

## 创建 Wikilink

1. **输入 `[[`**，然后开始输入笔记名称
2. **从自动补全中选择**并按 `Tab`
3. 使用 `Ctrl+Click`（Mac 上使用 `Cmd+Click`）或 `F12` **进行导航**
4. 点击不存在的 wikilink **创建新笔记**

示例：[[graph-view]]

## 占位符

指向不存在文件的 wikilink 会创建占位链接，并以不同样式显示，表明需要创建对应文件。占位链接适合用于规划知识结构。

可以使用 `Foam: Show Graph` 命令在图谱中查看占位符，也可以在 `Placeholders` 面板中查看。

## 章节链接

使用 `[[note-name#Section Title]]` 语法链接到特定章节。Foam 会为章节标题提供自动补全。

示例：

- 外部文件：`[link text](other-file.md#section-name)`
- 同一文档：`[link text](#section-name)`

## 块链接

使用 `[[note-name#^blockid]]` 语法链接到特定段落、列表项、标题或引用块。在任意块元素末尾添加 `^your-id` 锚点，然后即可从其他笔记引用它。

详情请参阅 [[block-anchors]]。

## 目录链接

链接到文件夹名称会导航到该文件夹的索引文件，即 `index.md` 或 `README.md`。Wikilink 和普通 Markdown 链接都支持此功能：

- `[[projects]]` → 打开 `projects/index.md`（或 `projects/README.md`）
- `[Projects](projects)` → 效果相同
- `[Projects](projects/)` → 忽略末尾的斜杠

如果 `projects/` 文件夹旁边存在名为 `projects.md` 的文件，则优先使用该文件。

要禁用此行为，请在 VS Code 设置中将 `foam.links.directory.mode` 设置为 `disabled`。

## 重命名时同步链接

重命名或移动笔记、文件夹时，Foam 会自动更新所有指向它的 wikilink。此功能默认启用，可以通过 `foam.links.sync.enable` 设置关闭。

对于标准 Markdown 链接（例如 `[text](path/to/note.md)`），VS Code 提供了内置功能来处理此行为。在 VS Code 设置中将 `markdown.updateLinksOnFileMove.enabled` 设置为 `always` 或 `prompt` 即可启用。

## 路径链接与标识符链接

Wikilink 有两种形式：

- **标识符链接** — `[[filename]]`、`[[folder/filename]]` — 通过名称标识资源，相对于整个工作区解析
- **路径链接** — `[[./file]]`、`[[../other/file]]`、`[[/from/root]]` — 通过文件路径标识资源

规则是：如果链接以 `/` 或 `.` 开头，则属于路径引用；否则属于标识符。

对于标识符链接，可以使用能够唯一标识文件的任意后缀。假设存在 `projects/house/todo.md` 和 `work/todo.md`，则 `[[todo]]`（有歧义）、`[[house/todo]]`（唯一）和 `[[projects/house/todo]]`（唯一）都有效，Foam 会选择最短且无歧义的形式。

## 有歧义的链接

当多个位置存在同名文件时，`[[todo]]` 就会产生歧义。Foam 会按字母顺序解析它（结果是确定的），并显示警告诊断，提示你使用更具体的标识符，例如 `[[house/todo]]`。

## Markdown 兼容性

Foam 可以在文件底部自动生成 [[link-reference-definitions]]，使 wikilink 兼容标准 Markdown 处理器。

## 与其他应用的兼容性

| Wikilink                       | Obsidian                        | Foam                            |
| ------------------------------ | ------------------------------- | ------------------------------- |
| `[[notes]]`                    | ✔ unique identifier in repo     | ✔ unique identifier in repo     |
| `[[/work/notes]]`              | ✔ valid path from repo root     | ✔ valid path from repo root     |
| `[[work/notes]]`               | ✔ valid path from repo root     | ✔ valid identifier in repo      |
| `[[project/house/todo]]`       | ✔ valid path from repo root     | ✔ valid unique identifier       |
| `[[/project/house/todo]]`      | ✔ valid path from repo root     | ✔ valid path from repo root     |
| `[[house/todo]]`               | ✔ valid unique identifier       | ✔ valid unique identifier       |
| `[[todo]]` (ambiguous)         | ✘ ambiguous identifier          | ✘ ambiguous identifier          |
| `[[/house/todo]]` (wrong path) | ✘ incorrect path from repo root | ✘ incorrect path from repo root |

## 相关内容

- [[footnotes]] - 添加引用和旁注
- [[block-anchors]] - 链接到笔记中的特定块
- [[templates]] - 创建新笔记

[graph-view]: graph-view.md "图谱可视化"
[block-anchors]: block-anchors.md "块锚点"
[link-reference-definitions]: link-reference-definitions.md "链接引用定义"
[footnotes]: footnotes.md "Footnotes"
[templates]: templates.md "笔记模板"
