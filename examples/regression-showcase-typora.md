# Esther Inspired Typora 回归测试样例

> 这是 Typora 专用测试素材。请勿覆盖 Obsidian 测试文件，因为 Typora 保存时可能规范化列表、引用及其不支持的 Obsidian 扩展语法。

## 01 / 标题与正文

# 一级标题 H1

## 二级标题 H2

### 三级标题 H3

#### 四级标题 H4

##### 五级标题 H5

###### 六级标题 H6

这是一段中文正文，用于检查行高、字重和段落间距。This is an English sentence with numbers 0123456789 and punctuation: `.,;:!?`.

这是一段包含 **粗体**、*斜体*、***粗斜体***、~~删除线~~、==下半段荧光高亮==、`行内代码` 和[外部链接](https://github.com/lisitan/esther-obsidian-typora-themes)的文本。

当前输入行对比度测试：依次把光标放入本段、上一段和下一段，正在编辑的正文不能突然变成浅灰色，Markdown 辅助符号仍可使用次要颜色。

光标移开后的普通正文应与当前输入行保持一致的主体文字颜色。

长行内代码换行测试：正文接近行尾时插入 `/Users/example/Documents/Notes/theme-test-with-a-very-long-file-name.md`，路径应利用当前行剩余空间并自然换行，不应整段跳到下一行。

---

## 02 / 紧凑列表与任务

- 一级无序列表
  - 二级无序列表
    - 三级无序列表，内容稍长，用于检查换行后的缩进
- 另一个一级项目

1. 一级有序列表
2. 第二项
   1. 二级有序列表
   2. 中英混排：Obsidian、Typora、Markdown

- [ ] 未完成任务
- [x] 已完成任务
  - [ ] 嵌套未完成任务
  - [x] 嵌套已完成任务

## 03 / 引用

> 单行引用：黄色引号应完整显示在正文左侧。

> 多行引用第一段。
>
> 第二段包含 **粗体**、==高亮==、[链接](https://typora.io/)和 `inline-code`。
>
> - 引用中的列表
> - 第二个列表项目

> [!NOTE]
> Typora 的 GitHub 风格 Note Callout，用于检查标题、图标与正文。

> [!WARNING]
> Typora 的 GitHub 风格 Warning Callout，用于检查警告色与文字对比度。

Obsidian 的 `[!success]-` 折叠 Callout、双链和嵌入只在 Obsidian 专用文件中测试。

## 04 / 表格

| 要回答的问题 | 写作系统里的例子 |
| --- | --- |
| 我看见了什么功能？ | 得到金线 Skill |
| 它替用户解决什么任务？ | 把编辑品控经验变成重复检查 |
| 公开线索在哪里？ | 产品文档、品控手册、开放接口、公开案例 |
| 空单元格 |  |

## 05 / 代码

行内代码测试：`const theme = "Esther Inspired";`

无语言代码块：

```
Esther Inspired
中文、English、0123456789
plain code without syntax highlighting
```

CSS 代码块：

```css
:root {
  --blue: #236dbb;
  --yellow: #f4d758;
  --paper: #fefcf6;
}

.good-writing {
  color: var(--ink);
  background: var(--paper);
}
```

JavaScript 代码块：

```javascript
function regressionTest(theme) {
  // 注释应该清晰，但可以弱于正文代码。
  const checks = ["cursor", "active-line", "horizontal-scroll"];
  return checks.every((item) => theme.supports(item));
}
```

JSON 代码块：

```json
{
  "name": "Esther Inspired",
  "modes": ["light", "dark"],
  "enabled": true,
  "contrastTarget": 4.5
}
```

代码测试动作：

1. 点击代码块的第一行、中间行和最后一行。
2. 检查光标、当前行背景、语言标识和横向滚动。
3. 点击代码块外部，确认各代码块的第一行或上次编辑行不再残留当前行底色。
4. 对比注释、关键字、字符串、数字、变量和属性。
5. 分别在 Paper 和 Midnight 下输入中文、英文和符号。

## 06 / 链接、脚注与图片

普通链接：[主题仓库](https://github.com/lisitan/esther-obsidian-typora-themes)

正文脚注测试。[^typora-regression]

[^typora-regression]: 这是 Typora 回归测试脚注。

![横向主题总览](../assets/esther-inspired-overview.png)

结束检查：回到文件顶部，重新检查列表、引用、表格与代码块，并分别切换 Paper 和 Midnight。
