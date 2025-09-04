---
title: MD语法学习
published: 2025-09-04
description: 'Markdown语法学习与示例'
image: './assets/images/a1f5954f684ba732a522919b41b9868660309fdb.jpg'
tags: ["Markdown", "语法", "教程"]
category: '"学习"'
draft: false 
lang: ''
---



> Markdown（简称 MD）是一种轻量级标记语言，允许你使用易读易写的纯文本格式编写文档，然后转换为结构化的HTML等格式。它广泛应用于博客、文档、笔记等场景。

<img src="./assets/images/a1f5954f684ba732a522919b41b9868660309fdb.jpg" title="" alt="" data-align="inline"> 

# general grammar

## 段落

要创建段落，请使用空行来分隔。

aaaa

bbbb

```
这是一个段落。

这是另一个段落。
```

## 小标题

要创建小标题，在小标题文本前添加至多六个 `#` 符号。`#` 符号的数量决定了小标题的级别。

```
# 这是标题 1
## 这是标题 2
### 这是标题 3
#### 这是标题 4
##### 这是标题 5
###### 这是标题 6
```

用 \` 来标注行内代码
用
\`\`\`注释
     code 
\`\`\`
来标注行间代码

## 粗体、斜体、高亮

格式化文本也可以使用[编辑相关的快捷键](https://publish.obsidian.md/help-zh/%E7%BC%96%E8%BE%91%E4%B8%8E%E6%A0%BC%E5%BC%8F%E5%8C%96/%E7%BC%96%E8%BE%91%E7%9B%B8%E5%85%B3%E7%9A%84%E5%BF%AB%E6%8D%B7%E9%94%AE)。

| 样式                   | 语法                    | 示例                  | 输出                |
| -------------------- | --------------------- | ------------------- | ----------------- |
| 粗体                   | `** **` 或 `__ __`     | `**粗体文本**`          | **粗体文本**          |
| 斜体                   | `* *` 或 `_ _`         | `*斜体文本*`            | _斜体文本_            |
| 删除线                  | `~~ ~~`               | `~~删除线文本~~`         | ~~删除线文本~~         |
| 高亮                   | `== ==`               | `==高亮文本==`          | ==高亮文本==          |
| 粗体和嵌套斜体              | `** **` 和 `_ _`       | `**粗体和 _嵌套斜体_ 文本**` | **粗体和 _嵌套斜体_ 文本** |
| 粗体和斜体                | `*** ***` 或 `___ ___` | `***粗体和斜体文本***`     | **_粗体和斜体文本_**     |
| \*\*这里的加粗不会真正的加粗\*\* |                       |                     |                   |
| **这里的加粗不会真正的加粗**     |                       |                     |                   |

```markdown
\*\*这里的加粗不会真正的加粗\*\*
```

## 链接

### 内部链接

用\[\[ link\]\] （Wiki风格）或 \[name \](url) (Markdown风格进行内部链接)

[[我爱你]]

[我爱你](我爱你.md)

### 外部链接

如果要链接到外部URL，可以通过在方括号（`[ ]`）中填入描述链接的文本，然后在括号中（`()`）添加URL来创建内联链接。
[Obsidian帮助](https://help.obsidian.md)

```
[Obsidian帮助](https://help.obsidian.md)
```

### 链接中转义空格

如果你的URL包含空格，必须用 `%20` 替换它们。

```md
[我的 笔记](obsidian://open?vault=主仓库&file=我的%20笔记.md)
```

你也可以用尖括号（`< >`）包裹URL进行转义。

```md
[我的 笔记]（<obsidian://open?vault=主仓库&file=我的 笔记.md>）
```

## 外部图片

你可以通过在[外部链接](https://publish.obsidian.md/help-zh/%E7%BC%96%E8%BE%91%E4%B8%8E%E6%A0%BC%E5%BC%8F%E5%8C%96/%E5%9F%BA%E6%9C%AC%E6%A0%BC%E5%BC%8F%E8%AF%AD%E6%B3%95#%E5%A4%96%E9%83%A8%E9%93%BE%E6%8E%A5)前加上 `!` 符号来在笔记中插入外部图片。

![图片](./assets/images/a1f5954f684ba732a522919b41b9868660309fdb.jpg)

```md
![Engelbart](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)
```

![Engelbart](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)

你可以通过在链接的锚文本中添加 `|640x480` 来更改图片尺寸，其中640是宽度，480是高度。

```md
![Engelbart|100x145](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)
```

如果只指定了宽度，图片会根据原始长宽比进行缩放。例如：

```md
![Engelbart|100](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)
```

Tip

如果要添加来自仓库内部的图片，你也可以[使用嵌入图片语法](https://publish.obsidian.md/help-zh/%E9%93%BE%E6%8E%A5%E7%AC%94%E8%AE%B0%E4%B8%8E%E6%96%87%E4%BB%B6/%E6%8F%92%E5%85%A5%E6%96%87%E4%BB%B6)。

## 引用

你可以在文本前加上 `>` 符号来引用文本。

```md
> 人类面临着越来越复杂和紧迫的问题，他们有效应对这些问题的能力对于社会的稳定和持续发展至关重要。

- 道格·恩格尔巴特，1961
```

> 人类面临着越来越复杂和紧迫的问题，他们有效应对这些问题的能力对于社会的稳定和持续发展至关重要。

- 道格·恩格尔巴特，1961

Tip

你可以通过在引用中的第一行添加 `[!信息]` 来将引用变成[标注](https://publish.obsidian.md/help-zh/%E7%BC%96%E8%BE%91%E4%B8%8E%E6%A0%BC%E5%BC%8F%E5%8C%96/%E6%A0%87%E6%B3%A8)。

[个人博客](https://desuki.me)

> 哈哈哈哈

- me

## 注释

你可以用 `%%` 包围文本来添加注释。注释只在编辑视图中可见。
%%注释%%

```md
这是一个 %%行内%% 注释。

%%
这是一个块注释。

块注释可以跨多行。
%%
```

## 了解更多

要了解更多高级格式化语法，如表格、图表和数学表达式，请参阅[高级格式语法](https://publish.obsidian.md/help-zh/%E7%BC%96%E8%BE%91%E4%B8%8E%E6%A0%BC%E5%BC%8F%E5%8C%96/%E9%AB%98%E7%BA%A7%E6%A0%BC%E5%BC%8F%E8%AF%AD%E6%B3%95)。

要了解Obsidian如何解析Markdown，请参阅[Obsidian 风格的 Markdown 语法](https://publish.obsidian.md/help-zh/%E7%BC%96%E8%BE%91%E4%B8%8E%E6%A0%BC%E5%BC%8F%E5%8C%96/Obsidian+%E9%A3%8E%E6%A0%BC%E7%9A%84+Markdown+%E8%AF%AD%E6%B3%95)。
