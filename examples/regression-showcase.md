---
title: Esther Inspired 回归测试样例
tags:
  - theme-test
  - regression
aliases:
  - 主题回归测试
status: testing
---

# Esther Inspired 回归测试样例

> 这是 Obsidian 专用的固定测试素材。请直接复制原始 `.md` 文件到仓库，不要从 Typora 的渲染界面复制，也不要用 Typora 保存后再交给 Obsidian 测试；Typora 测试请使用 `regression-showcase-typora.md`。

## 01 / 标题层级

# 一级标题 H1

## 二级标题 H2

### 三级标题 H3

#### 四级标题 H4

##### 五级标题 H5

###### 六级标题 H6

这是一段中文正文，用于检查行高、字重和段落间距。This is an English sentence with numbers 0123456789 and punctuation: `.,;:!?`.

这是一段包含 **粗体**、*斜体*、***粗斜体***、~~删除线~~、==下半段荧光高亮==、`行内代码` 和[外部链接](https://github.com/lisitan/esther-obsidian-typora-themes)的文本。

超长链接换行测试：https://example.com/a-very-long-path/for/testing/typography/overflow/and-line-wrapping?source=regression-test

---

## 02 / 列表与任务

- 一级无序列表
  - 二级无序列表
    - 三级无序列表，内容稍长，用于检查换行后的缩进是否与首行对齐
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

> 多行引用第一段，用于检查引号是否遮挡正文，以及背景是否始终保持一种颜色。
>
> 第二段包含 **粗体**、==高亮==、[链接](https://obsidian.md/)和 `inline-code`。
>
> - 引用中的列表
>   - 引用中的二级无序列表
> - 第二个一级列表项目
>
> 1. 引用中的有序列表
> 2. 第二个有序列表项目
>
> - [ ] 引用中的未完成任务
> - [x] 引用中的已完成任务
>
> 引用中的代码块：
>
> ```javascript
> const quotedCode = "代码背景与文字需要保持可读";
> ```

> 外层引用
>
> > 二级嵌套引用不应出现异常宽度、重复背景或裁切。
> >
> > - 二级引用中的列表
> > - 第二个列表项目
> >
> > > 三级嵌套引用用于检查更深层级的缩进和换行。

## 04 / Callout

> [!note] 普通提示
> 用于检查 Callout 标题、图标和正文。

> [!warning] 警告提示
> 警告状态需要保持足够的文字对比度。

> [!success]- 可折叠成功提示
> 展开和折叠状态都需要测试。

## 05 / 表格

### 普通表格

| 要回答的问题 | 写作系统里的例子 |
| --- | --- |
| 我看见了什么功能？ | 得到金线 Skill |
| 它替用户解决什么任务？ | 把编辑品控经验变成重复检查 |
| 公开线索在哪里？ | 产品文档、品控手册、开放接口、公开案例 |
| 我真正需要什么？ | 规则、搜索接口、生成模型或状态文件 |
| 哪些现成零件可以替代？ | OpenAPI、MCP、GPT Image 2、本地 Markdown |
| 我的边界是什么？ | 个人笔记只读、关键节点必须确认、中转站匿名 |
| 用什么任务验证？ | 完成一篇真的准备发布的公众号文章 |
| 这次返工要留下什么？ | Skill、检查表、状态字段或脚本 |

### 边界表格

| 类型 | 短内容 | 长内容或空内容 |
| :--- | :---: | ---: |
| 中文 | 正常 | 这是一段比较长的中文表格内容，用来测试编辑状态、自动换行、单元格高度和窄窗口布局 |
| English | OK | A long English table cell for checking wrapping, spacing, alignment, and overflow behavior |
| URL | Link | https://example.com/a/very/long/table/cell/url/that/needs/to/wrap |
| 空单元格 |  | 右侧有内容 |

测试动作：

1. 点击普通表格中的每一个单元格。
2. 在单元格开头和末尾移动光标。
3. 新增一行和一列，再撤销。
4. 缩窄窗口，确认表格不会产生异常巨大的空白。

## 06 / 代码

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
  --red: #e84a5f;
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

const veryLongLine = "This line is intentionally long to verify that fenced code blocks scroll horizontally instead of breaking the surrounding layout or hiding the editing cursor.";
```

JSON 代码块：

```json
{
  "name": "Esther Inspired",
  "version": "regression-test",
  "modes": ["light", "dark"],
  "enabled": true,
  "contrastTarget": 4.5
}
```

测试动作：

1. 先点击代码块外部，确认代码框、工具栏和窗口圆点正常显示。
2. 再点击代码块的第一行、中间行和最后一行。
3. 检查光标、当前行背景、语言标识和横向滚动。
4. 再次点击代码块外部，确认第一行或上次编辑行不再残留当前行底色。
5. 对比注释、关键字、字符串、数字、变量和属性是否容易辨认。
6. 分别在浅色和深色模式下输入中文、英文和符号。

## 07 / Obsidian 双链与嵌入

- 已存在双链：[[README]]
- 双链别名：[[README|主题说明]]
- 未创建双链：[[尚未创建的测试笔记]]
- 标题链接：[[README#在 Obsidian 中安装]]
- 块链接：[[regression-showcase#^regression-test-block]]

这是一段用于块链接测试的内容。 ^regression-test-block

> [!info] 嵌入测试
> 在 Obsidian 中确认嵌入标题、正文、编辑按钮和边框正常。

![[README]]

## 08 / 标签、脚注与特殊文本

标签测试：#theme-test #中文标签 #design/system

正文脚注测试。[^regression]

[^regression]: 这是回归测试脚注，用于检查脚注区域、返回链接和字号。

特殊字符：`< > { } [ ] ( ) # * _ | \ / @ & © ® ™`

## 09 / 图片

![横向主题总览](../assets/esther-inspired-overview.png)

图片测试应覆盖：

- 正常宽度。
- 窄窗口缩放。
- 图片说明和替代文本。
- 阅读模式与编辑模式。

## 10 / 长段落与边界

这是一个用于测试长段落的文本。主题需要在长时间阅读时保持稳定的行距、段落间距和中文标点节奏，同时避免因为超长句子、中英文混排、数字 2026-07-16、产品名称 Obsidian 1.12 和 Typora，以及路径 `/Users/example/Documents/Notes/theme-test.md` 而出现异常断行、溢出或文字重叠。窗口变窄时，正文应自然换行，侧栏、滚动条、状态栏和浮动按钮不应覆盖内容。

结束检查：回到文件顶部，分别切换阅读模式与编辑模式，再切换一次浅色与深色模式。
