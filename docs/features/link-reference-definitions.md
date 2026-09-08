# 链接引用定义

链接引用定义会将 wikilink 转换为标准 Markdown 引用，使你的笔记兼容标准 Markdown 处理器。

Foam 本身不需要引用定义也能正常工作，但此功能旨在支持你可能希望集成的其他工具。

## 什么是链接引用定义

Foam 可以自动将引用定义添加到笔记底部：

**你的笔记：**

```markdown
# Machine Learning

Related to [[Data Science]] and [[Statistics]].
```

**添加引用定义后：**

```markdown
# Machine Learning

Related to [[Data Science]] and [[Statistics]].

[Data Science]: data-science.md 'Data Science'
[Statistics]: statistics.md 'Statistics'
```

## 启用引用定义

在设置中进行配置：

```json
{
  "foam.edit.linkReferenceDefinitions": "withExtensions"
}
```

**选项：**

- `"off"` - 禁用（默认）
- `"withoutExtensions"` - 不带扩展名的引用
- `"withExtensions"` - 带扩展名的引用

如果只在 Foam 中使用笔记，可以保持 `off`（也能减少杂乱）；否则请根据使用场景选择合适的设置。

## 工作原理

1. 扫描笔记中的 wikilink
2. 保存时生成引用定义
3. 链接发生变化时更新定义
4. 维护自动生成的区域

## 优点

- **标准 Markdown 兼容性** - 可与任何 Markdown 处理器配合使用
- **发布平台** - 兼容 GitHub Pages、Jekyll 等平台
- **面向未来** - 不局限于 Foam 专用格式
- **团队协作** - 其他人无需安装 Foam 也能阅读笔记
