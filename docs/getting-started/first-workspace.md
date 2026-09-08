# 创建你的第一个工作区

Foam 工作区是存放所有笔记、想法和知识的地方。你可以把它想象成一座数字花园，让思想在其中生长并建立联系。本指南将帮助你设置一个结构清晰、可扩展且符合个人思维方式的工作区。

## 了解工作区

Foam 工作区本质上是一个包含 **Markdown 文件**（`.md`）的文件夹，也就是存放实际笔记的地方。

此外还可以包含：

- **配置文件** - VS Code 设置和 Foam 首选项
- **资源** - 图片、附件和其他媒体
- **模板** - 可重复使用的笔记结构

### 单个工作区与多个工作区

**推荐：单个工作区**

- 将所有知识集中在一个地方
- 更便于发现链接和查看图谱
- 更容易维护和备份
- 遵循“统一知识库”原则

**已弃用：多个工作区**（已弃用，仅供高级用户使用）

- 分离工作和个人知识
- 隔离敏感信息
- 为不同项目使用不同工作流

目前应将多个工作区视为已弃用功能，未来可能不再受支持。
你可以通过文件/文件夹链接模拟复杂工作区。

## 方法 1：使用 Foam 模板（推荐）

最简单的开始方式是使用我们预先配置好的模板：

### 第 1 步：从模板创建

1. **访问** [github.com/foambubble/foam-template](https://github.com/foambubble/foam-template)
2. **点击“Use this template”**（需要 GitHub 账户）
3. **为仓库命名**（例如 “john-knowledge-base”、“my-second-brain”）
4. **选择可见性：**
   - **Private** - 用于个人笔记（推荐）
   - **Public** - 如果希望公开分享知识

### 第 2 步：克隆到本地

```bash
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name
```

### 第 3 步：在 VS Code 中打开

1. **启动 VS Code**
2. **File > Open Folder**
3. **选择克隆的仓库文件夹**

## 方法 2：从头开始

如需最简设置：

1. 在电脑上**创建新文件夹**
2. 在 VS Code 中**打开该文件夹**（`File > Open Folder`）

就这么简单，你可以开始处理 Markdown 文件，剩下的交给 Foam 即可。

> 已经有 Obsidian vault？可以直接在 VS Code 中打开它，参见 [[migrating-from-obsidian]]。

## 知识库构想

### 1. 自定义设置

根据个人偏好检查并调整 `.vscode/settings.json`：

- **每日笔记位置** - 存放每日笔记的位置
- **图片处理** - 整理粘贴图片的方式
- **链接格式** - 是否包含文件扩展名

### 2. 设置收件箱

创建 `inbox.md` 作为默认记录位置：

```markdown
# Inbox

整理之前，可以先将临时笔记和想法记录在这里。

## 今天的记录

-

## 待处理

-

## 想法

-
```

### 3. 创建核心结构笔记

## 工作区组织策略

建立主要的组织笔记。
你可以使用任何方法，Foam 不限定具体的组织方式。

唯一的建议是先开始，之后再逐步改进。

用户采用较多的两种方法是 [PARA](https://fortelabs.com/blog/para/) 和 [Zettelkasten](https://zettelkasten.de/overview/)。

### PARA 方法

围绕四个类别进行组织：

- **项目** - 有截止日期的事项
- **领域** - 持续承担的职责
- **资源** - 未来参考资料
- **归档** - 不活跃的事项

### Zettelkasten 方法

使用编号管理原子化想法：

- **永久笔记** - `202501251030-idea-title.md`
- **文献笔记** - `book-author-year.md`
- **索引笔记** - `index-topic.md`

### 4. 配置每日笔记

每日笔记适合用于：

- 每日计划和反思
- 会议笔记
- 日记记录
- 临时记录

测试每日笔记设置：

1. **按 `Ctrl+Shift+P` / `Cmd+Shift+P`**
2. **输入“Foam: Open Daily Note”**
3. **确认笔记已创建在正确位置**

你也可以按 `Alt+D` 打开今天的每日笔记，或按 `Alt+H` 打开其他日期的每日笔记。
使用 `.foam/templates/daily-note.md` 自定义每日笔记。

## 新工作区的最佳实践

### 1. 从小处开始

- 先从几篇笔记开始
- 初期不要过度组织
- 让结构自然形成

### 2. 使用模板

- 为常见笔记类型创建模板
- 保持相似笔记的一致性
- 节省重复格式化的时间

### 3. 尽早并经常建立链接

- 灵活使用 `[[wikilinks]]`
- 不必担心创建“完美”的链接
- Foam 能妥善处理断开的链接

### 4. 定期回顾

- 每周清理工作区
- 归档已完成的项目
- 找出缺失的连接

## 同步和备份

Foam 基于普通文件运行，你可以在此基础上添加任何喜欢的备份方式。

### Git

你的工作区是一个 Git 仓库：

```bash
git add .
git commit -m "Add new notes and ideas"
git push origin main
```

如果有帮助，也可以使用其他 VS Code 扩展管理 Git 同步。

### 其他同步方式

- **云存储** - Dropbox、OneDrive、Google Drive
- **本地备份** - Time Machine、文件历史记录
- **手动导出** - 定期创建 ZIP 备份

## 接下来做什么

工作区设置完成后，你可以：

1. **[学习笔记基础](note-taking-in-foam.md)** - 掌握 Markdown 和高效笔记写作
2. **[探索导航](navigation.md)** - 使用 wikilink 连接想法
3. **[了解图谱视图](../features/graph-view.md)** - 将知识网络可视化
4. **[设置模板](../features/templates.md)** - 规范笔记创建流程

## 获取帮助

如果在设置过程中遇到问题：

- 查看[安装指南](installation.md)了解前置要求
- 查看[[frequently-asked-questions]]了解常见工作区问题
- 加入 [Foam Discord 社区](https://discord.com/invite/HV2tn2FpEk)

[migrating-from-obsidian]: ../recipes/migrating-from-obsidian.md "Coming from Obsidian"
[frequently-asked-questions]: ../frequently-asked-questions.md "常见问题"
