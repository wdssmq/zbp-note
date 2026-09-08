# 每日笔记

每日笔记可以让你快速创建和访问每天对应的笔记文件。

## 创建每日笔记

- **命令：** `Ctrl+Shift+P` → “Foam: Open Daily Note”
- **快捷键：** `Alt+D`
- **片段：** 在任意笔记中输入 `/today`、`/yesterday`、`/tomorrow`

## 自动打开每日笔记

在 VS Code 启动时自动打开每日笔记：

```json
{
  "foam.openDailyNote.onStartup": true
}
```

## 每日笔记模板

创建 `.foam/templates/daily-note.md` 来自定义结构：

```markdown
---
type: daily-note
---

# 每日笔记 - $FOAM_DATE_YEAR-$FOAM_DATE_MONTH-$FOAM_DATE_DATE

## 任务

- [ ]

## 笔记
```

## 日期片段

Create links to recent daily notes using snippets:

| 片段         | 日期          |
| ------------ | ------------- |
| `/today`     | 今天          |
| `/tomorrow`  | 明天          |
| `/yesterday` | 昨天          |
| `/monday`    | 下周一        |
| `/+1d`       | 明天          |
| `/-3d`       | 3 天前        |
| `/+1w`       | 一周后        |
| `/-1m`       | 一个月前      |
| `/+1y`       | 一年后        |

## 配置

默认情况下，每日笔记会以 `yyyy-mm-dd.md` 的形式创建在工作区的 `journals` 文件夹中。

要自定义每日笔记的位置和格式，可以创建 `.foam/templates/daily-note.md` 模板。更多信息请参阅 [[templates]]。

还有一些设置可以自定义每日笔记的行为，但这些设置已弃用并将被移除。请使用 `daily-note.md` 模板。

要从终端处理每日笔记，请参阅 [[daily|CLI daily command]]。

[templates]: templates.md 'Note Templates'
[daily]: ../tools/cli/daily.md 'foam daily'
