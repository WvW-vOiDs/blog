---
# **************************************************************************** #
#                                   metadata                                   #
# **************************************************************************** #
date: "2024-12-30T12:03:13+08:00"
title: "Test Demo"
slug: "Test demo"

description: "Description 将会在 single page 展示. 本文用于测试网站功能." # 文章内容的描述
summary: "Summary 将会在list page展示. 本文用于测试网站功能."

tags: ["Markdown", "Hugo", "TODO"] # 关键词
categories: ["Draft"] # 文件夹结构
collections: ["博客搭建"] # 合集: 用于更新系列文章, 如: "量子力学抄书笔记"

# **************************************************************************** #
#                                     页面设置                                     #
# **************************************************************************** #
# =================================== model ================================== #
draft: false
# weight: 1 # 需要置顶时使用

# ================================ encryption ================================ #
# password: "1234" # [必需] 加密页面内容的密码
# message: "密码是 1234" # [可选] 加密提示信息
# ---------------------------------------------------------------------------- #

# ================================= component ================================ #
# ShowToc: false # 默认 true
# TocOpen: false # 默认 true

# readingTime: false # 默认 true
# wordCount: false # 默认 true

# ================================== search ================================== #
# searchHidden: true # 默认 false

# =================================== cover ================================== #
featuredImage: "https://t.alcy.cc/ycy" # 文章的特色图片 在文章开始展示
featuredImagePreview: "images/cover.webp" # 用在主页预览的文章特色图片

# **************************************************************************** #
#                                     其他设置                                     #
# **************************************************************************** #

# ================================== mathjax ================================= #
math: true # 使用 mathjax 渲染 latex 公式
---

**Summary:** 本文用于测试和展示网站功能, 并作为博客功能的说明书.

<!--more-->
---
## Markdown 基本语法

FixIt 主题作者已经提供了一个很好的 [markdown 基本语法介绍](https://fixit.lruihao.cn/zh-cn/documentation/content-management/markdown-syntax/basics/), 这里仅对个人不太熟悉和常用的进行记录. 本节内容大量来自于主题作者提供的 [文档](https://fixit.lruihao.cn/zh-cn/documentation/content-management/markdown-syntax/basics/).

### 锚点

#### 标题锚点 <a id="custom-id"></a>

标题自带锚点, 即标题的内容(空格用 `-` 替代, 大写用小写替代). 如 [点击这里](#锚点) 可以链接到本节标题. 如果有同名标题, 则按顺序在后面添加 `-1`, `-2`等后缀, 如: `#锚点`, `#锚点-1`, `#锚点-2`.

> [!Note]
> 要想自定义标题锚点名称, 请在与标题相同的行中将自定义 ID 放在花括号中, 或者用[正文锚点](#正文锚点):
> ```md
> ## markdown 基本语法 {#custom-id}
> ## markdown 基本语法 <a id="custom-id"></a>
> ```
> 前者会导致默认生成的锚点 (上例中即为 `#markdown-基本语法`) 无法使用, 取而代之为自定义的锚点名称 (上例中即为 `#custon-id`). 后者则是两个锚点名均可使用并且定位到相同位置. 个人推荐使用后者.

#### 正文锚点

可以在正文中任意位置处添加锚点:
```md
我想在这句话处添加一个锚点.<a id="a-means-anchor"></a>

这样我就可以[跳转](#a-means-anchor)到相应的地方.
```
> [!Example]-
> 我想在这句话处添加一个锚点.<a id="a-means-anchor"></a>
>
> 这样我就可以[跳转](#a-means-anchor)到相应的地方.

### 粗体和斜体

按照个人习惯规定, 粗体使用 `**` 包裹, 斜体使用 `_` 包裹. 但是 粗体中有斜体 除外, 使用 `__粗体*粗斜体*粗体__` 形式.[^粗斜体]
[^粗斜体]: 粗中有斜和斜中有粗只能外面`_`, 里面`*`.

```md
__粗体*粗斜体*粗体__ <!-- 正确渲染 -->
**粗体_粗斜体_粗体** <!-- 错误渲染 -->
_斜体**粗斜体**斜体_ <!-- 正确渲染 -->
*斜体__粗斜体__斜体* <!-- 错误渲染 -->
```

> [!Example]-
> __粗体*粗斜体*粗体__<br>
> **粗体_粗斜体_粗体**<br>
> _斜体**粗斜体**斜体_<br>
> *斜体__粗斜体__斜体*<br><br>
> 全体对比: 正常|**加粗**|_斜体_|***粗斜体***|_斜体**包含粗体**斜体_|__粗体*包含斜体*粗体__.

### 预格式化文本

如果想要保留原格式输出一些文本, 可以使用[预格式化文本]^(preformatted text).

```md
<pre>
这是一些
    预格式化的文本.
   文本中的空格 和 换行符
        都会被保留.
</pre>
```

> [!Example]-
> <pre>
> 这是一些
>     预格式化的文本.
>    文本中的空格 和 换行符
>         都会被保留.
> </pre>

### 超链接

基本格式:
```md
https://WvW-vOiDs.github.io
<https://WvW-vOiDs.github.io> <!-- 直接写链接时推荐 -->
<voidsofficial@outlook.com>
[我的主页](https://WvW-vOiDs.github.io)
[我的主页](https://WvW-vOiDs.github.io "跳转到 Github")
[我的主页][MyHomePage]
[MyHomePage]: https://WvW-vOiDs.github.io "跳转到 Github" <!-- 这个可以放在文章的任何地方 -->
```

> [!Example]-
> https://WvW-vOiDs.github.io <br>
> <https://WvW-vOiDs.github.io> <br>
> <voidsofficial@outlook.com> <br>
> [我的主页](https://WvW-vOiDs.github.io) <br>
> [我的主页](https://WvW-vOiDs.github.io "跳转到 Github")<br>
> [我的主页][MyHomePage]

[MyHomePage]: https://WvW-vOiDs.github.io "跳转到 Github"


## Markdown 扩展语法

本节内容为 FixIt 主题定制版语法. 与上节相同, 本节内容基本全部来自于 [FixIt 官方介绍文档](https://fixit.lruihao.cn/zh-cn/documentation/content-management/markdown-syntax/extended/).

### Callout

Callout 是特殊的 用于强调关键信息的 引用块. FixIt 中基本兼容 [obsidian 中的 callouts 用法](https://help.obsidian.md/callouts).

FixIt 有两种类型的 Callouts:

#### 基本 Callout

如果给这些基本 Callout 加 title, 或者选择是否折叠, 则会变成[扩展版](#扩展-callout).

```md
> [!note]

> [!tip]

> [!important]

> [!warning]

> [!caution]
```
> [!Example]-
> > [!note]
> > Lorem ipsum dolor sit amet<br>
> > WvW-Note: 这是排版中常用的无意义拉丁文
>
> > [!tip]
> > Lorem ipsum dolor sit amet
>
> > [!important]
> > Lorem ipsum dolor sit amet
>
> > [!warning]
> > Lorem ipsum dolor sit amet
>
> > [!caution]
> > Lorem ipsum dolor sit amet

#### 扩展 Callout

扩展 Callouts [**可以**]^(optional) 在类型后面加 `+` 和 `-` 来表示其默认状态.

> [!note]
> Obsidian 自定义 callout 标题的方法和 FixIt 不太一样:
> ```md
> <!-- Obsidian 允许用以下方式自定义 callout 标题: -->
> > [!Everything is ok.]
> <!-- 这等价于: -->
> > [!note] Everything is ok.
>
> <!-- FixIt 只能用以下方式自定义 callout 标题: -->
> > [!note] Everything is ok.
> > [!warning] Everything is not ok.
> ...
> ```
> 只要包含空格, 数字, 汉字或者符号(连字符, 下划线, 句号)就不能使用以下方式自定义 callout
> ```md
> > [!Everythingisok]
> ```

FixIt 支持在配置文件中[自定义 callout](https://fixit.lruihao.cn/zh-cn/documentation/advanced/#custom-admonitions). FixIt 主题原生支持以下类型扩展版 callouts.

```md
> [!note] This is Title.

> [!tip]
> alias: important, hint

> [!warning]
> aliases: caution, attention

> [!abstract]
> aliases: summary, tldr.

> [!info]

> [!todo]

> [!success]
> aliases: check, done

> [!question]
> aliases: help, faq

> [!failure]
> aliases: fail, missing

> [!danger]
> alias: error

> [!bug]

> [!example]

> [!quote]
> alias: cite
```

> [!Example]-
> > [!note] This is Title.
> > type: note
>
> > [!tip]+
> > type: tip<br>
> > aliases: important, hint
>
> > [!warning]+
> > type: warning<br>
> > aliases: caution, attention
>
> > [!abstract]+
> > type: abstract<br>
> > aliases: summary, tldr<br>
> > WvW-Note: TL;DR means: too long; didn't read.
>
> > [!info]-
> > type: info<br>
> > 一些不太重要的信息.
>
> > [!todo]
> > type: todo
>
> > [!success]
> > type: success<br>
> > aliases: check, done
>
> > [!question]
> > type: question<br>
> > aliases: help, faq<br>
> > WvW-Note: faq means: frequently asked questions.
>
> > [!failure]
> > type: failure<br>
> > aliases: fail, missing
>
> > [!danger]
> > type: danger<br>
> > alias: error
>
> > [!bug]
> > type: bug
>
> > [!example]
> > type: example
>
> > [!quote]
> > type: quote<br>
> > alias: cite

### 任务列表

FixIt 在 markdown 基本的待办事项表示方法上增加了许多新的状态, 所有支持的状态如下:
```md
- [ ] 未完成
- [x] 已完成
- [/] 进行中
- [-] 已取消
- [<] 已计划
- [>] 已重新计划
- [!] 重要
- [?] 问题
```

> [!Example]-
> - [ ] 未完成
> - [x] 已完成
> - [/] 进行中
> - [-] 已取消
> - [<] 已计划
> - [>] 已重新计划
> - [!] 重要
> - [?] 问题

同 callout, FixIt 支持[自定义待办事项](https://fixit.lruihao.cn/zh-cn/documentation/advanced/#custom-task-lists).

### 删除线, 下划线, 高亮 和 上下标

在 加粗, 斜体 的基础 markdown 语法上, Hugo 定义了类似的[扩展语法](https://gohugo.io/configuration/markup/#extras):
```md {data-open=true}
这是~~删除线~~.
这是++下划线++.
这是==高亮==.
这是^上标^.
这是~下标~.

其他高亮颜色:
==Primary==[primary]
==Secondary==[secondary]
==Success==[success]
==Info==[info]
==Warning==[warning]
==Danger==[danger]
```
> [!Example]-
> 这是~~删除线~~.<br>
> 这是++下划线++.<br>
> 这是==高亮==.<br>
> 这是^上标^.[^禁用上标]<br>
> 这是~下标~.<br>
> <br>
> 其他高亮颜色:<br>
> ==Primary==[primary]
> ==Secondary==[secondary]
> ==Success==[success]
> ==Info==[info]
> ==Warning==[warning]
> ==Danger==[danger]

[^禁用上标]: 上标已禁用, 因为有时会和[文字上方标记](#字符注音-或-注释)冲突.

### 数学公式

FixIt 原本使用 [KaTeX](https://katex.org/) 对 LaTeX 语法提供支持. 但由于个人对宏包有较多需求, 故暂时使用了一个 **破坏性的** 方法强制使用 [MathJax](https://www.mathjax.org/). 具体情况见:
{{< link href="https://github.com/hugo-fixit/FixIt/issues/574" content="[FEATURE] Add MathJax Support as an Alternative Renderer" title="[FEATURE] Add MathJax Support as an Alternative Renderer" card=true card-icon="fa-brands fa-github fa-fw" >}}

> [!Warning]
> 目前若加密文章, 公式则无法渲染.

以下是具体测试:

> [!Example]- 行内公式
> ```LaTeX
> 这是一个行内公式 \(a^*=x-b^*\).
> ```
> 这是一个行内公式 \(a^*=x-b^*\).

> [!Example]- 行间公式
> ```latex
> \begin{aligned}
> \ce{CO2 + C -> 2CO}\\
> \ce{Hg^2+ ->[I-] HgI2 ->[I-] [Hg^{II}I4]^2-}
> \end{aligned}
> ```
> \[
    \begin{aligned}
        &\ce{CO2 + C -> 2CO}\\
        &\ce{Hg^2+ ->[I-] HgI2 ->[I-] [Hg^{II}I4]^2-}
    \end{aligned}
  \]

> [!Example]- physics 宏包
> ```latex
> \[\mqty(1 & 2 \\ 3 & 4)\]
> \[\ip{\psi}{\phi}\]
> ```
> \[\mqty(1 & 2 \\ 3 & 4)\]
> \[\ip{\psi}{\phi}\]

> [!Warning]
>
> `<` 后 **一定** 要接一个空格 (或使用 `\lt` 代替 `<` 以强制提醒自己加空格), 否则会当成 html 的标签而无法渲染.[^无法渲染]
> ```latex
> \[
>     x < y, x\lt y
> \]
> ```
> \[
      x < y, x\lt y
  \]

[^无法渲染]: Reference: [Math equations with the less than sign (<) can’t render correctly](https://discourse.gohugo.io/t/math-equations-with-the-less-than-sign-cant-render-correctly/52890)


> [!Example]- 超过3个大括号的公式
> 根据 [SonnyCalcr的博客](https://sonnycalcr.github.io/posts/build-a-blog-using-hugo-papermod-github-pages/#%E9%85%8D%E7%BD%AE%E6%95%B0%E5%AD%A6%E5%85%AC%E5%BC%8F) 所说:
>
> > ...数学公式如果有超过了三对花括号, 那么, 其解析和转义就会出问题...
>
> 但在本文中尚未遇到, 可能是此 bug 已被修复?
>
> ```LaTeX
> \[
>     \boldsymbol{x}_{i+1} + \boldsymbol{x}_{i+2} = \boldsymbol{x}_{i+3}
> \]
> ```
> \[
      \boldsymbol{x}_{i+1} + \boldsymbol{x}_{i+2} = \boldsymbol{x}_{i+3}
  \]

### 字符注音 或 注释

> FixIt 主题支持一种 字符注音或者注释 Markdown 扩展语法:
```md
[MMA]{?^}(Mathematica) 是一个很好用的计算软件.
```
> [!Example]-
> [MMA]^(Mathematica) 是一个很好用的计算软件.

### 分数

> FixIt 主题支持一种 分数 Markdown 扩展语法:
```md
[浅色]{?/}[深色]
[99]{?/}[100]
```
> [!Example]-
> [浅色]/[深色]<br>
> [99]/[100]


### Font Awesome

> FixIt 主题使用 [Font Awesome V6](https://fontawesome.com/) 作为图标库, 可以轻松使用其中的图标:
```md
:(fa-sharp fa-solid fa-circle-user{?)}:
:(fa-regular fa-circle-user{?)}:
```
> [!Example]-
> :(fa-sharp fa-solid fa-circle-user):<br>
> :(fa-regular fa-circle-user):

### 转义字符

> 在某些特殊情况下 (编写这个主题文档时 :(fa-regular fa-grin-squint-tears):), 你的文章内容会与 Markdown 的基本或者扩展语法冲突, 并且无法避免. 转义字符语法可以帮助你渲染出想要的内容:
> ```md
> {?{}?X}->X
> ```

```md
[link{?]}(#escape-character)
```
> [!Example]-
> [link{?]}(#escape-character)

### Markdown 属性

Hugo 支持图像和块元素上的 [Markdown 属性](https://gohugo.io/content-management/markdown-attributes/), 包括块引用、围栏代码块、标题、水平线、列表、段落和表格.

在大多数情况下, 将属性列表放置在标记元素下方. 对于标题和围栏代码块, 将属性列表放在右侧.
```md
some Markdown content
{#id .class1 .class2 key1="value1" key2="value2"}
```

#### 分割线

```md
<!-- 带有 CSS 类的分割线 -->
---
{.awesome-hr}
```
呈现的输出如下所示:

---
{.awesome-hr}

#### 引用

```md
<!-- 带有 CSS 类的分割线 -->
> The quick brown fox jumps over the lazy dog.
{.blockquote-center}
```
呈现的输出如下所示:

> The quick brown fox jumps over the lazy dog.
{.blockquote-center}

#### 表格 和 列表

目前有一些限制: 对于表格, 你目前只能将其应用于完整表格; 而对于列表, 仅适用于 `<ul>`/`<ol>` 节点, 例如:

```md
- 水果
  - 苹果
  - 橙子
  - 香蕉
  {.text-success}
- 乳制品
  - 牛奶
  - 奶酪
  {.text-warning}
{.text-primary}
```
呈现的输出如下所示:
- 水果
  - 苹果
  - 橙子
  - 香蕉
  {.text-success}
- 乳制品
  - 牛奶
  - 奶酪
  {.text-warning}
{.text-primary}

#### 代码块

请注意, [code fences](https://gohugo.io/content-management/syntax-highlighting/#highlighting-in-code-fences) 中的属性和其他高亮处理指令必须位于开始标记之后, 例如:
````md {data-open=true}
<!-- title -->
```js {title="test.js"}
console.log('hello FixIt!');
```

<!-- highlight -->
```go {hl_lines=[3,"6-8"]}
package main

import "fmt"

func main() {
    for i := 0; i < 3; i++ {
        fmt.Println("Value of i:", i)
    }
}
```

<!-- no-header -->
```js {.no-header}
function forEach(elements, handler) {
  elements = elements || [];
  for (let i = 0; i < elements.length; i++) {
    handler(elements[i]);
  }
}
```

<!-- data-open -->
```js {data-open=false}
console.log('hello FixIt!');
```
````

> [!Example]-
> title
> ```js {title="test.js"}
> console.log('hello FixIt!');
> ```
>
> highlight
> ```go {hl_lines=[3,"6-8"]}
> package main
>
> import "fmt"
>
> func main() {
>     for i := 0; i < 3; i++ {
>         fmt.Println("Value of i:", i)
>     }
> }
> ```
>
> no-header
> ```js {.no-header}
> function forEach(elements, handler) {
>   elements = elements || [];
>   for (let i = 0; i < elements.length; i++) {
>     handler(elements[i]);
>   }
> }
> ```
>
> data-open
> ```js {data-open=false}
> console.log('hello FixIt!');
> ```

### 代码块拓展语法

#### GoAT

[[GoAT]^(Go ASCII Tool)](https://github.com/bep/goat) 是 [markdeep.mini.js](https://casual-effects.com/markdeep/) 图像生成器的 Go 语言实现.

要使用 GoAT, 只需将 ASCII 输入放在代码块中, 并将语言设置为 goat.

> [!Example]-
> Trees:
> ````md {data-open=false}
> ```goat
>       .               .                .               .--- 1          .-- 1     / 1
>      / \              |                |           .---+            .-+         +
>     /   \         .---+---.         .--+--.        |   '--- 2      |   '-- 2   / \ 2
>    +     +        |       |        |       |    ---+            ---+          +
>   / \   / \     .-+-.   .-+-.     .+.     .+.      |   .--- 3      |   .-- 3   \ / 3
>  /   \ /   \    |   |   |   |    |   |   |   |     '---+            '-+         +
>  1   2 3   4    1   2   3   4    1   2   3   4         '--- 4          '-- 4     \ 4
> ```
> ````
> ```goat
>       .               .                .               .--- 1          .-- 1     / 1
>      / \              |                |           .---+            .-+         +
>     /   \         .---+---.         .--+--.        |   '--- 2      |   '-- 2   / \ 2
>    +     +        |       |        |       |    ---+            ---+          +
>   / \   / \     .-+-.   .-+-.     .+.     .+.      |   .--- 3      |   .-- 3   \ / 3
>  /   \ /   \    |   |   |   |    |   |   |   |     '---+            '-+         +
>  1   2 3   4    1   2   3   4    1   2   3   4         '--- 4          '-- 4     \ 4
> ```
>
> Overlaps:
> ````md {data-open=false}
> ```goat
>        .-.           .-.           .-.           .-.           .-.           .-.
>       |   |         |   |         |   |         |   |         |   |         |   |
>    .---------.   .--+---+--.   .--+---+--.   .--|   |--.   .--+   +--.   .------|--.
>   |           | |           | |   |   |   | |   |   |   | |           | |   |   |   |
>    '---------'   '--+---+--'   '--+---+--'   '--|   |--'   '--+   +--'   '--|------'
>       |   |         |   |         |   |         |   |         |   |         |   |
>        '-'           '-'           '-'           '-'           '-'           '-'
> ```
> ````
> ```goat
>        .-.           .-.           .-.           .-.           .-.           .-.
>       |   |         |   |         |   |         |   |         |   |         |   |
>    .---------.   .--+---+--.   .--+---+--.   .--|   |--.   .--+   +--.   .------|--.
>   |           | |           | |   |   |   | |   |   |   | |           | |   |   |   |
>    '---------'   '--+---+--'   '--+---+--'   '--|   |--'   '--+   +--'   '--|------'
>       |   |         |   |         |   |         |   |         |   |         |   |
>        '-'           '-'           '-'           '-'           '-'           '-'
> ```
>
> Line Decorations:
> ````md {data-open=false}
> ```goat
>               ________                            o        *          *   .--------------.
>  *---+--.    |        |     o   o      |         ^          \        /   |  .----------.  |
>      |   |    '--*   -+-    |   |      v        /            \      /    | |  <------.  | |
>      |    '----->       .---(---'  --->*<---   /      .+->*<--o----'     | |          | | |
>  <--'  ^  ^             |   |                 |      | |  ^    \         |  '--------'  | |
>         \/        *-----'   o     |<----->|   '-----'  |__|     v         '------------'  |
>         /\                                                               *---------------'
> ```
> ````
> ```goat
>               ________                            o        *          *   .--------------.
>  *---+--.    |        |     o   o      |         ^          \        /   |  .----------.  |
>      |   |    '--*   -+-    |   |      v        /            \      /    | |  <------.  | |
>      |    '----->       .---(---'  --->*<---   /      .+->*<--o----'     | |          | | |
>  <--'  ^  ^             |   |                 |      | |  ^    \         |  '--------'  | |
>         \/        *-----'   o     |<----->|   '-----'  |__|     v         '------------'  |
>         /\                                                               *---------------'
> ```
>
> Line Ends:
> ````md {data-open=false}
> ```goat
>  o--o    *--o     /  /   *  o  o o o o   * * * *   o o o o   * * * *      o o o o   * * * *
>  o--*    *--*    v  v   ^  ^   | | | |   | | | |    \ \ \ \   \ \ \ \    / / / /   / / / /
>  o-->    *-->   *  o   /  /    o * v '   o * v '     o * v \   o * v \  o * v /   o * v /
>  o---    *---
>                                ^ ^ ^ ^   . . . .   ^ ^ ^ ^   \ \ \ \      ^ ^ ^ ^   / / / /
>  |  |   *  o  \  \   *  o      | | | |   | | | |    \ \ \ \   \ \ \ \    / / / /   / / / /
>  v  v   ^  ^   v  v   ^  ^     o * v '   o * v '     o * v \   o * v \  o * v /   o * v /
>  *  o   |  |    *  o   \  \
>
>  <--o   <--*   <-->   <---      ---o   ---*   --->   ----      *<--   o<--   -->o   -->*
> ```
> ````
> ```goat
>  o--o    *--o     /  /   *  o  o o o o   * * * *   o o o o   * * * *      o o o o   * * * *
>  o--*    *--*    v  v   ^  ^   | | | |   | | | |    \ \ \ \   \ \ \ \    / / / /   / / / /
>  o-->    *-->   *  o   /  /    o * v '   o * v '     o * v \   o * v \  o * v /   o * v /
>  o---    *---
>                                ^ ^ ^ ^   . . . .   ^ ^ ^ ^   \ \ \ \      ^ ^ ^ ^   / / / /
>  |  |   *  o  \  \   *  o      | | | |   | | | |    \ \ \ \   \ \ \ \    / / / /   / / / /
>  v  v   ^  ^   v  v   ^  ^     o * v '   o * v '     o * v \   o * v \  o * v /   o * v /
>  *  o   |  |    *  o   \  \
>
>  <--o   <--*   <-->   <---      ---o   ---*   --->   ----      *<--   o<--   -->o   -->*
> ```
>
> Dot Grids:
> ````md {data-open=false}
> ```goat
>  o o o o o  * * * * *  * * o o *    o o o      * * *      o o o     · * · · ·     · · ·
>  o o o o o  * * * * *  o o o o *   o o o o    * * * *    * o * *    · * * · ·    · · · ·
>  o o o o o  * * * * *  o * o o o  o o o o o  * * * * *  o o o o o   · o · · o   · · * * ·
>  o o o o o  * * * * *  o * o o o   o o o o    * * * *    o * o o    · · · · o    · · * ·
>  o o o o o  * * * * *  * * * * o    o o o      * * *      o * o     · · · · ·     · · *
> ```
> ````
> ```goat
>  o o o o o  * * * * *  * * o o *    o o o      * * *      o o o     · * · · ·     · · ·
>  o o o o o  * * * * *  o o o o *   o o o o    * * * *    * o * *    · * * · ·    · · · ·
>  o o o o o  * * * * *  o * o o o  o o o o o  * * * * *  o o o o o   · o · · o   · · * * ·
>  o o o o o  * * * * *  o * o o o   o o o o    * * * *    o * o o    · · · · o    · · * ·
>  o o o o o  * * * * *  * * * * o    o o o      * * *      o * o     · · · · ·     · · *
> ```
>
> Large Nodes:
> ````md {data-open=false}
> ```goat
>  .---.       .-.        .-.       .-.                                       .-.
>  | A +----->| 1 +<---->| 2 |<----+ 4 +------------------.                  | 8 |
>  '---'       '-'        '+'       '-'                    |                  '-'
>                          |         ^                     |                   ^
>                          v         |                     v                   |
>                         .-.      .-+-.        .-.      .-+-.      .-.       .+.       .---.
>                        | 3 +---->| B |<----->| 5 +---->| C +---->| 6 +---->| 7 |<---->| D |
>                         '-'      '---'        '-'      '---'      '-'       '-'       '---'
> ```
> ````
> ```goat
>  .---.       .-.        .-.       .-.                                       .-.
>  | A +----->| 1 +<---->| 2 |<----+ 4 +------------------.                  | 8 |
>  '---'       '-'        '+'       '-'                    |                  '-'
>                          |         ^                     |                   ^
>                          v         |                     v                   |
>                         .-.      .-+-.        .-.      .-+-.      .-.       .+.       .---.
>                        | 3 +---->| B |<----->| 5 +---->| C +---->| 6 +---->| 7 |<---->| D |
>                         '-'      '---'        '-'      '---'      '-'       '-'       '---'
> ```
>
> Small Grids:
> ````md {data-open=false}
> ```goat
>       ___     ___      .---+---+---+---+---.     .---+---+---+---.  .---.   .---.
>   ___/   \___/   \     |   |   |   |   |   |    / \ / \ / \ / \ /   |   +---+   |
>  /   \___/   \___/     +---+---+---+---+---+   +---+---+---+---+    +---+   +---+
>  \___/ b \___/   \     |   |   | b |   |   |    \ / \a/ \b/ \ / \   |   +---+   |
>  / a \___/   \___/     +---+---+---+---+---+     +---+---+---+---+  +---+ b +---+
>  \___/   \___/   \     |   | a |   |   |   |    / \ / \ / \ / \ /   | a +---+   |
>      \___/   \___/     '---+---+---+---+---'   '---+---+---+---'    '---'   '---'
> ```
> ````
> ```goat
>       ___     ___      .---+---+---+---+---.     .---+---+---+---.  .---.   .---.
>   ___/   \___/   \     |   |   |   |   |   |    / \ / \ / \ / \ /   |   +---+   |
>  /   \___/   \___/     +---+---+---+---+---+   +---+---+---+---+    +---+   +---+
>  \___/ b \___/   \     |   |   | b |   |   |    \ / \a/ \b/ \ / \   |   +---+   |
>  / a \___/   \___/     +---+---+---+---+---+     +---+---+---+---+  +---+ b +---+
>  \___/   \___/   \     |   | a |   |   |   |    / \ / \ / \ / \ /   | a +---+   |
>      \___/   \___/     '---+---+---+---+---'   '---+---+---+---'    '---'   '---'
> ```
>
> Big Grids:
> ````md {data-open=false}
> ```goat
>    .----.        .----.
>   /      \      /      \            .-----+-----+-----.
>  +        +----+        +----.      |     |     |     |          .-----+-----+-----+-----+
>   \      /      \      /      \     |     |     |     |         /     /     /     /     /
>    +----+   B    +----+        +    +-----+-----+-----+        +-----+-----+-----+-----+
>   /      \      /      \      /     |     |     |     |       /     /     /     /     /
>  +   A    +----+        +----+      |     |  B  |     |      +-----+-----+-----+-----+
>   \      /      \      /      \     +-----+-----+-----+     /     /  A  /  B  /     /
>    '----+        +----+        +    |     |     |     |    +-----+-----+-----+-----+
>          \      /      \      /     |  A  |     |     |   /     /     /     /     /
>           '----'        '----'      '-----+-----+-----'  '-----+-----+-----+-----+
> ```
> ````
> ```goat
>    .----.        .----.
>   /      \      /      \            .-----+-----+-----.
>  +        +----+        +----.      |     |     |     |          .-----+-----+-----+-----+
>   \      /      \      /      \     |     |     |     |         /     /     /     /     /
>    +----+   B    +----+        +    +-----+-----+-----+        +-----+-----+-----+-----+
>   /      \      /      \      /     |     |     |     |       /     /     /     /     /
>  +   A    +----+        +----+      |     |  B  |     |      +-----+-----+-----+-----+
>   \      /      \      /      \     +-----+-----+-----+     /     /  A  /  B  /     /
>    '----+        +----+        +    |     |     |     |    +-----+-----+-----+-----+
>          \      /      \      /     |  A  |     |     |   /     /     /     /     /
>           '----'        '----'      '-----+-----+-----'  '-----+-----+-----+-----+
> ```
>
> Complicated:
> ````md {data-open=false}
> ```goat
> +-------------------+                           ^                      .---.
> |    A Box          |__.--.__    __.-->         |      .-.             |   |
> |                   |        '--'               v     | * |<---        |   |
> +-------------------+                                  '-'             |   |
>                        Round                                       *---(-. |
>   .-----------------.  .-------.    .----------.         .-------.     | | |
>  |   Mixed Rounded  | |         |  / Diagonals  \        |   |   |     | | |
>  | & Square Corners |  '--. .--'  /              \       |---+---|     '-)-'       .--------.
>  '--+------------+-'  .--. |     '-------+--------'      |   |   |       |        / Search /
>     |            |   |    | '---.        |               '-------'       |       '-+------'
>     |<---------->|   |    |      |       v                Interior                 |     ^
>     '           <---'      '----'   .-----------.              ---.     .---       v     |
>  .------------------.  Diag line    | .-------. +---.              \   /           .     |
>  |   if (a > b)     +---.      .--->| |       | |    | Curved line  \ /           / \    |
>  |   obj->fcn()     |    \    /     | '-------' |<--'                +           /   \   |
>  '------------------'     '--'      '--+--------'      .--. .--.     |  .-.     +Done?+-'
>     .---+-----.                        |   ^           |\ | | /|  .--+ |   |     \   /
>     |   |     | Join        \|/        |   | Curved    | \| |/ | |    \    |      \ /
>     |   |     +---->  o    --o--        '-'  Vertical  '--' '--'  '--  '--'        +  .---.
>  <--+---+-----'       |     /|\                                                    |  | 3 |
>                       v                             not:line    'quotes'        .-'   '---'
>   .-.             .---+--------.            /            A || B   *bold*       |        ^
>  |   |           |   Not a dot  |      <---+---<--    A dash--is not a line    v        |
>   '-'             '---------+--'          /           Nor/is this.            ---
> ```
> ````
> ```goat
> +-------------------+                           ^                      .---.
> |    A Box          |__.--.__    __.-->         |      .-.             |   |
> |                   |        '--'               v     | * |<---        |   |
> +-------------------+                                  '-'             |   |
>                        Round                                       *---(-. |
>   .-----------------.  .-------.    .----------.         .-------.     | | |
>  |   Mixed Rounded  | |         |  / Diagonals  \        |   |   |     | | |
>  | & Square Corners |  '--. .--'  /              \       |---+---|     '-)-'       .--------.
>  '--+------------+-'  .--. |     '-------+--------'      |   |   |       |        / Search /
>     |            |   |    | '---.        |               '-------'       |       '-+------'
>     |<---------->|   |    |      |       v                Interior                 |     ^
>     '           <---'      '----'   .-----------.              ---.     .---       v     |
>  .------------------.  Diag line    | .-------. +---.              \   /           .     |
>  |   if (a > b)     +---.      .--->| |       | |    | Curved line  \ /           / \    |
>  |   obj->fcn()     |    \    /     | '-------' |<--'                +           /   \   |
>  '------------------'     '--'      '--+--------'      .--. .--.     |  .-.     +Done?+-'
>     .---+-----.                        |   ^           |\ | | /|  .--+ |   |     \   /
>     |   |     | Join        \|/        |   | Curved    | \| |/ | |    \    |      \ /
>     |   |     +---->  o    --o--        '-'  Vertical  '--' '--'  '--  '--'        +  .---.
>  <--+---+-----'       |     /|\                                                    |  | 3 |
>                       v                             not:line    'quotes'        .-'   '---'
>   .-.             .---+--------.            /            A || B   *bold*       |        ^
>  |   |           |   Not a dot  |      <---+---<--    A dash--is not a line    v        |
>   '-'             '---------+--'          /           Nor/is this.            ---
> ```

#### Mermaid

[Mermaid](https://mermaid.js.org/) 是一个基于 JavaScript 的图表工具, 它允许你使用文本和代码创建图表和可视化.

要使用 Mermaid, 只需将 Mermaid 的代码输入放在代码块中, 并将语言设置为 mermaid.

> [!Example]-
> Flowchart:
> ````md {data-open=false}
> ```mermaid
> graph TD;
>     A-->B;
>     A-->C;
>     B-->D;
>     C-->D;
> ```
> ````
> ```mermaid
> graph TD;
>     A-->B;
>     A-->C;
>     B-->D;
>     C-->D;
> ```
>
> Sequence diagram:
> ````md {data-open=false}
> ```mermaid
> sequenceDiagram
>     participant Alice
>     participant Bob
>     Alice->>John: Hello John, how are you?
>     loop HealthCheck
>         John->>John: Fight against hypochondria
>     end
>     Note right of John: Rational thoughts <br/>prevail!
>     John-->>Alice: Great!
>     John->>Bob: How about you?
>     Bob-->>John: Jolly good!
> ```
> ````
> ```mermaid
> sequenceDiagram
>     participant Alice
>     participant Bob
>     Alice->>John: Hello John, how are you?
>     loop HealthCheck
>         John->>John: Fight against hypochondria
>     end
>     Note right of John: Rational thoughts <br/>prevail!
>     John-->>Alice: Great!
>     John->>Bob: How about you?
>     Bob-->>John: Jolly good!
> ```
>
> Gantt diagram:
> ````md {data-open=false}
> ```mermaid
> gantt
> dateFormat  YYYY-MM-DD
> title Adding GANTT diagram to mermaid
> excludes weekdays 2014-01-10
>
> section A section
> Completed task            :done,    des1, 2014-01-06,2014-01-08
> Active task               :active,  des2, 2014-01-09, 3d
> Future task               :         des3, after des2, 5d
> Future task2               :         des4, after des3, 5d
> ```
> ````
> ```mermaid
> gantt
> dateFormat  YYYY-MM-DD
> title Adding GANTT diagram to mermaid
> excludes weekdays 2014-01-10
>
> section A section
> Completed task            :done,    des1, 2014-01-06,2014-01-08
> Active task               :active,  des2, 2014-01-09, 3d
> Future task               :         des3, after des2, 5d
> Future task2               :         des4, after des3, 5d
> ```
>
> Class diagram:
> ````md {data-open=false}
> ```mermaid
> classDiagram
> Class01 <|-- AveryLongClass : Cool
> Class03 *-- Class04
> Class05 o-- Class06
> Class07 .. Class08
> Class09 --> C2 : Where am i?
> Class09 --* C3
> Class09 --|> Class07
> Class07 : equals()
> Class07 : Object[] elementData
> Class01 : size()
> Class01 : int chimp
> Class01 : int gorilla
> Class08 <--> C2: Cool label
> ```
> ````
> ```mermaid
> classDiagram
> Class01 <|-- AveryLongClass : Cool
> Class03 *-- Class04
> Class05 o-- Class06
> Class07 .. Class08
> Class09 --> C2 : Where am i?
> Class09 --* C3
> Class09 --|> Class07
> Class07 : equals()
> Class07 : Object[] elementData
> Class01 : size()
> Class01 : int chimp
> Class01 : int gorilla
> Class08 <--> C2: Cool label
> ```
>
> Git graph
> ````md {data-open=false}
> ```mermaid
> gitGraph
>     commit
>     branch hotfix
>     checkout hotfix
>     commit
>     branch develop
>     checkout develop
>     commit id:"ash" tag:"abc"
>     branch featureB
>     checkout featureB
>     commit type:HIGHLIGHT
>     checkout main
>     checkout hotfix
>     commit type:NORMAL
>     checkout develop
>     commit type:REVERSE
>     checkout featureB
>     commit
>     checkout main
>     merge hotfix
>     checkout featureB
>     commit
>     checkout develop
>     branch featureA
>     commit
>     checkout develop
>     merge hotfix
>     checkout featureA
>     commit
>     checkout featureB
>     commit
>     checkout develop
>     merge featureA
>     branch release
>     checkout release
>     commit
>     checkout main
>     commit
>     checkout release
>     merge main
>     checkout develop
>     merge release
> ```
> ````
> ```mermaid
> gitGraph
>     commit
>     branch hotfix
>     checkout hotfix
>     commit
>     branch develop
>     checkout develop
>     commit id:"ash" tag:"abc"
>     branch featureB
>     checkout featureB
>     commit type:HIGHLIGHT
>     checkout main
>     checkout hotfix
>     commit type:NORMAL
>     checkout develop
>     commit type:REVERSE
>     checkout featureB
>     commit
>     checkout main
>     merge hotfix
>     checkout featureB
>     commit
>     checkout develop
>     branch featureA
>     commit
>     checkout develop
>     merge hotfix
>     checkout featureA
>     commit
>     checkout featureB
>     commit
>     checkout develop
>     merge featureA
>     branch release
>     checkout release
>     commit
>     checkout main
>     commit
>     checkout release
>     merge main
>     checkout develop
>     merge release
> ```
>
> Entity Relationship Diagram(❗experimental):
> ````md {data-open=false}
> ```mermaid
> erDiagram
>     CUSTOMER ||--o{ ORDER : places
>     ORDER ||--|{ LINE-ITEM : contains
>     CUSTOMER }|..|{ DELIVERY-ADDRESS : uses
> ```
> ````
> ```mermaid
> erDiagram
>     CUSTOMER ||--o{ ORDER : places
>     ORDER ||--|{ LINE-ITEM : contains
>     CUSTOMER }|..|{ DELIVERY-ADDRESS : uses
> ```
>
> User Journey Diagram
> ````md {data-open=false}
> ```mermaid
> journey
>     title My working day
>     section Go to work
>       Make tea: 5: Me
>       Go upstairs: 3: Me
>       Do work: 1: Me, Cat
>     section Go home
>       Go downstairs: 5: Me
>       Sit down: 5: Me
> ```
> ````
> ```mermaid
> journey
>     title My working day
>     section Go to work
>       Make tea: 5: Me
>       Go upstairs: 3: Me
>       Do work: 1: Me, Cat
>     section Go home
>       Go downstairs: 5: Me
>       Sit down: 5: Me
> ```
>
> Quadrant Chart:
> ````md {data-open=false}
> ```mermaid
> quadrantChart
>     title Reach and engagement of campaigns
>     x-axis Low Reach --> High Reach
>     y-axis Low Engagement --> High Engagement
>     quadrant-1 We should expand
>     quadrant-2 Need to promote
>     quadrant-3 Re-evaluate
>     quadrant-4 May be improved
>     Campaign A: [0.3, 0.6]
>     Campaign B: [0.45, 0.23]
>     Campaign C: [0.57, 0.69]
>     Campaign D: [0.78, 0.34]
>     Campaign E: [0.40, 0.34]
>     Campaign F: [0.35, 0.78]
> ```
> ````
> ```mermaid
> quadrantChart
>     title Reach and engagement of campaigns
>     x-axis Low Reach --> High Reach
>     y-axis Low Engagement --> High Engagement
>     quadrant-1 We should expand
>     quadrant-2 Need to promote
>     quadrant-3 Re-evaluate
>     quadrant-4 May be improved
>     Campaign A: [0.3, 0.6]
>     Campaign B: [0.45, 0.23]
>     Campaign C: [0.57, 0.69]
>     Campaign D: [0.78, 0.34]
>     Campaign E: [0.40, 0.34]
>     Campaign F: [0.35, 0.78]
> ```
>
> XY Chart:
> ````md {data-open=false}
> ```mermaid
> xychart-beta
>     title "Sales Revenue"
>     x-axis [jan, feb, mar, apr, may, jun, jul, aug, sep, oct, nov, dec]
>     y-axis "Revenue (in $)" 4000 --> 11000
>     bar [5000, 6000, 7500, 8200, 9500, 10500, 11000, 10200, 9200, 8500, 7000, 6000]
>     line [5000, 6000, 7500, 8200, 9500, 10500, 11000, 10200, 9200, 8500, 7000, 6000]
> ```
> ````
> ```mermaid
> xychart-beta
>     title "Sales Revenue"
>     x-axis [jan, feb, mar, apr, may, jun, jul, aug, sep, oct, nov, dec]
>     y-axis "Revenue (in $)" 4000 --> 11000
>     bar [5000, 6000, 7500, 8200, 9500, 10500, 11000, 10200, 9200, 8500, 7000, 6000]
>     line [5000, 6000, 7500, 8200, 9500, 10500, 11000, 10200, 9200, 8500, 7000, 6000]
> ```
>
> Pie chart diagrams:
> ````md {data-open=false}
> ```mermaid
> pie title Pets adopted by volunteers
>     "Dogs" : 386
>     "Cats" : 85
>     "Rats" : 15
> ```
> ````
> ```mermaid
> pie title Pets adopted by volunteers
>     "Dogs" : 386
>     "Cats" : 85
>     "Rats" : 15
> ```
>
> Requirement Diagram:
> ````md {data-open=false}
> ```mermaid
>     requirementDiagram
>
>     requirement test_req {
>     id: 1
>     text: the test text.
>     risk: high
>     verifymethod: test
>     }
>
>     element test_entity {
>     type: simulation
>     }
>
>     test_entity - satisfies -> test_req
> ```
> ````
> ```mermaid
>     requirementDiagram
>
>     requirement test_req {
>     id: 1
>     text: the test text.
>     risk: high
>     verifymethod: test
>     }
>
>     element test_entity {
>     type: simulation
>     }
>
>     test_entity - satisfies -> test_req
> ```
>
> Mindmap:
> ````md {data-open=false}
> ```mermaid
> mindmap
>   root((mindmap))
>     Origins
>       Long history
>       ::icon(fa fa-book)
>       Popularisation
>         British popular psychology author Tony Buzan
>     Research
>       On effectiveness<br/>and features
>       On Automatic creation
>         Uses
>             Creative techniques
>             Strategic planning
>             Argument mapping
>     Tools
>       Pen and paper
>       Mermaid
> ```
> ````
> ```mermaid
> mindmap
>   root((mindmap))
>     Origins
>       Long history
>       ::icon(fa fa-book)
>       Popularisation
>         British popular psychology author Tony Buzan
>     Research
>       On effectiveness<br/>and features
>       On Automatic creation
>         Uses
>             Creative techniques
>             Strategic planning
>             Argument mapping
>     Tools
>       Pen and paper
>       Mermaid
> ```
>
> Packet Diagram:
> ````md {data-open=false}
> ```mermaid
> packet-beta
> title UDP Packet
> 0-15: "Source Port"
> 16-31: "Destination Port"
> 32-47: "Length"
> 48-63: "Checksum"
> 64-95: "Data (variable length)"
> ```
> ````
> ```mermaid
> packet-beta
> title UDP Packet
> 0-15: "Source Port"
> 16-31: "Destination Port"
> 32-47: "Length"
> 48-63: "Checksum"
> 64-95: "Data (variable length)"
> ```
>
> Architecture Diagrams Documentation:
> ````md {data-open=false}
> ```mermaid
> architecture-beta
>     group api(cloud)[API]
>
>     service db(database)[Database] in api
>     service disk1(disk)[Storage] in api
>     service disk2(disk)[Storage] in api
>     service server(server)[Server] in api
>
>     db:L -- R:server
>     disk1:T -- B:server
>     disk2:T -- B:db
> ```
> ````
> ```mermaid
> architecture-beta
>     group api(cloud)[API]
>
>     service db(database)[Database] in api
>     service disk1(disk)[Storage] in api
>     service disk2(disk)[Storage] in api
>     service server(server)[Server] in api
>
>     db:L -- R:server
>     disk1:T -- B:server
>     disk2:T -- B:db
> ```
> 还有许多其他类型的图, 具体内容可查看 [mermaid 官网](https://mermaid.js.org/).

#### Timeline

Timeline 可拆分成多个按照时间戳正序或倒序排列的事件, 时间戳和内容是必填项. 更多内容请查看 [FixIt 官网](https://fixit.lruihao.cn/zh-cn/documentation/content-management/timeline-support/).

> [!Example]-
> ````md
> ```timeline {reverse=true, animation=true}
> events:
>   - timestamp: 2021-12-18T16:15:22+08:00
>     content: "Feat: [LoveIt](https://github.com/dillonzq/LoveIt) => [FixIt](https://github.com/hugo-fixit/FixIt)"
>     type: primary
>   - timestamp: 2021-12-19T19:48:23+08:00
>     content: "⬆️ Chore: update 0.2.11"
>   - timestamp: 2021-12-19T19:48:23+08:00
>     content: "<span class=\"text-secondary\">:(fa-regular fa-comment-dots): Developed for a long time...</span>"
>     hideTimestamp: true
>     type: secondary
>   - timestamp: 2024-01-01T14:54:19+08:00
>     content: "🔖 Chore(release): 0.3.0"
>     type: success
>   - timestamp: 2024-05-20T14:54:19+08:00
>     content: "<span class=\"text-secondary\">:(fa-regular fa-comment-dots): Half a year later...</span>"
>     hideTimestamp: true
>     type: secondary
>   - timestamp: 2024-07-20T22:28:19+08:00
>     content: "🎉 Feat: add timeline support for code blocks"
>     type: danger
> ```
> ````
> ```timeline {reverse=true, animation=true}
> events:
>   - timestamp: 2021-12-18T16:15:22+08:00
>     content: "Feat: [LoveIt](https://github.com/dillonzq/LoveIt) => [FixIt](https://github.com/hugo-fixit/FixIt)"
>     type: primary
>   - timestamp: 2021-12-19T19:48:23+08:00
>     content: "⬆️ Chore: update 0.2.11"
>   - timestamp: 2021-12-19T19:48:23+08:00
>     content: "<span class=\"text-secondary\">:(fa-regular fa-comment-dots): Developed for a long time...</span>"
>     hideTimestamp: true
>     type: secondary
>   - timestamp: 2024-01-01T14:54:19+08:00
>     content: "🔖 Chore(release): 0.3.0"
>     type: success
>   - timestamp: 2024-05-20T14:54:19+08:00
>     content: "<span class=\"text-secondary\">:(fa-regular fa-comment-dots): Half a year later...</span>"
>     hideTimestamp: true
>     type: secondary
>   - timestamp: 2024-07-20T22:28:19+08:00
>     content: "🎉 Feat: add timeline support for code blocks"
>     type: danger
> ```

## Shortcodes

### Hugo 内置 Shortcodes

参考 [FixIt 文档](https://fixit.lruihao.cn/zh-cn/documentation/content-management/shortcodes/built-in/).

#### figure

```markdown
{{</* figure
  src="/images/cover.webp"
  alt="A photograph of Zion National Park"
  link="https://www.nps.gov/zion/index.htm"
  caption="Zion National Park"
  class="ma0 w-75"
*/>}}
```

建议使用 markdown 默认图片语法 或 FixIt 提供的 [image shortcode](#image-shortcode).

{{< figure src="https://t.alcy.cc/ycy" alt="随机图床" link="https://t.alcy.cc/ycy" caption="随机图床" class="ma0 w-75" >}}

#### gist

Hugo 将不再内置 Gist shortcode[^gist]:

> The gist shortcode was deprecated in version 0.143.0 and will be removed in a future release.

[^gist]: Reference: [Gist shortcode](https://gohugo.io/shortcodes/gist/).

#### Instagram

```markdown
{{</* instagram CxOWiQNP2MO */>}}
```
{{< instagram CxOWiQNP2MO >}}

#### QR

```markdown
{{</* qr text="https://wvw-voids.github.io" level="high"/*/>}}
```
{{< qr text="https://wvw-voids.github.io" level="high"/>}}

或者
```markdown
{{</* qr level="high" scale=4 alt="QR code example"*/>}}
Hello, this is vOiDs.
{{</* /qr */>}}
```
{{< qr level="high" scale=4 alt="QR code example">}}
Hello, this is vOiDs.
{{< /qr >}}

#### X

```markdown
{{</* x user="SanDiegoZoo" id="1453110110599868418" */>}}
```
> [!Warning]
> 目前无法渲染.

#### Vimeo

```markdown
{{</* vimeo 146022717 */>}}
```
{{< vimeo 146022717 >}}

#### Youtube

```markdown
{{</* youtube id=0RKpf3rK57I mute=true */>}} <!-- 最好默认加入 `mute=true`, 保护大家听力, 人人有责! -->
```
{{< youtube id=0RKpf3rK57I mute=true >}}

### FixIt 扩展 Shortcodes

参考 [FixIt 文档](https://fixit.lruihao.cn/zh-cn/documentation/content-management/shortcodes/extended/).

#### link

普通链接用 markdown 语法即可, 这个 shortcode 主要是提供了卡片式链接:
```markdown
{{</* link href="https://wvw-voids.github.io/blog" content="WvW-vOiDs 的 blog 主页" title="悬停在链接上时显示的文字" card=true card-icon="https://wvw-voids.github.io/blog/icons/favicon.svg"*/>}}
```
{{< link href="https://wvw-voids.github.io/blog" content="WvW-vOiDs 的 blog 主页" title="悬停在链接上时显示的文字" card=true card-icon="https://wvw-voids.github.io/blog/icons/favicon.svg">}}

也可以表示可下载资源:
```markdown
{{</* link href="images/cover.webp" content="本文的 cover. 图片来自于https://t.alcy.cc/ycy" card=true download="下载文件名"*/>}}
```
{{< link href="images/cover.webp" content="本文的 cover. 图片来自于https://t.alcy.cc/ycy" card=true download="下载文件名" >}}

#### image <a id="image-shortcode"></a>

```markdown
{{</* image src="/images/cover.webp" alt="本文的 cover" caption="本文的 cover. 图片来自于<https://t.alcy.cc/ycy>" */>}}
```

{{< image src="/images/cover.webp" alt="本文的 cover" caption="本文的 cover. 图片来自于<https://t.alcy.cc/ycy>" >}}

> [!Note]
> 也可以用 markdown 格式的图片引用, 大部分情况下足够满足需求. 如果有更多需求不如直接写 html.

#### mapbox

由于没有 accessToken 所以具体内容见 [FixIt 文档](https://fixit.lruihao.cn/zh-cn/documentation/content-management/shortcodes/extended/mapbox/).

#### music

详情见 [FixIt 文档](https://fixit.lruihao.cn/zh-cn/documentation/content-management/shortcodes/extended/music/).

```markdown
{{</* music auto="https://music.163.com/#/playlist?id=644299359" */>}}
```

> [!Warning]
> 当前使用 music shortcode 后页面目录会卡住, 详情见 {{< link href="https://github.com/hugo-fixit/FixIt/issues/577" content="[BUG] 使用 music shortcode 后会导致目录卡死" title="[BUG] 使用 music shortcode 后会导致目录卡死" card=true card-icon="fa-brands fa-github fa-fw" >}}

#### spotify

详情见 [FixIt 文档](https://fixit.lruihao.cn/zh-cn/documentation/content-management/shortcodes/extended/spotify/).
```markdown
{{</* spotify type="album" id="6Nws2NAPuxaHzB7MfD1lhg" */>}}
```
{{< spotify type="album" id="6Nws2NAPuxaHzB7MfD1lhg" >}}

#### bilibili

```markdown
{{</* bilibili id="BV1qM411k79Z" t=6317 */>}}
```
{{< bilibili id="BV1qM411k79Z" t=6317 >}}

#### douyin

```markdown
{{</* douyin 7471079764552371494 */>}}
```
{{< douyin 7471079764552371494 >}}

#### typeit

```markdown
{{</* typeit tag=h5 loop=true */>}}
这一个带有基于 [TypeIt](https://typeitjs.com/) 的 **打字动画** 的 *段落*……
{{</* /typeit */>}}

{{</* typeit code=java */>}}
public class HelloWorld {
    public static void main(String []args) {
        System.out.println("Hello World");
    }
}
{{</* /typeit */>}}

{{</* typeit group=paragraph */>}}
**首先**, 这个段落开始
{{</* /typeit */>}}

{{</* typeit group=paragraph */>}}
**然后**, 这个段落开始
{{</* /typeit */>}}
```
{{< typeit tag=h5 loop=true >}}
这一个带有基于 [TypeIt](https://typeitjs.com/) 的 **打字动画** 的 *段落*……
{{< /typeit >}}

{{< typeit code=java >}}
public class HelloWorld {
    public static void main(String []args) {
        System.out.println("Hello World");
    }
}
{{< /typeit >}}

{{< typeit group=paragraph >}}
**首先**, 这个段落开始
{{< /typeit >}}

{{< typeit group=paragraph >}}
**然后**, 这个段落开始
{{< /typeit >}}

#### script

```markdown
{{</* script */>}}
console.log('Hello FixIt!');
{{</* /script */>}}
```
{{< script >}}
console.log('Hello FixIt!');
{{< /script >}}

#### details

```markdown
{{</* details summary="这里可以写 _markdown_ 语法" open=true */>}}
展开内容是正常 _markdown_ 格式.
{{</* /details */>}}
```
{{< details summary="这里可以写 _markdown_ 语法" open=true >}}
展开内容是正常 _markdown_ 格式.
{{< /details >}}

#### fixit-encrypt

{{% fixit-encryptor password="1212" message="密码是 1212" %}}

加密部分中的公式暂时 **无法正确渲染**: \(\mathrm{e}^{\mathrm{i}\pi}=-1\)

{{% /fixit-encryptor %}}

#### raw

如果需要在引用块中使用公式, 最好用 `{?{}{< raw >}}` 和 `{?{}{< /raw >}}` 包裹.

> [!Example]- 使用 raw 才能正常显示
> {{< raw >}}
\[
  E=mc^2
\]{{< /raw >}}

### 自定义 Shortcodes

> [!TODO]
> - [ ] 插入 [GeoGebra](https://geogebra.github.io/docs/reference/en/GeoGebra_Apps_Embedding/)
> - [x] 插入 [Slidev](https://sli.dev)

#### slidev

> [Slidev](https://sli.dev) (slide + dev, /slaɪdɪv/) 是一个为开发者设计的基于 Web 的幻灯片制作工具。它帮助您以 Markdown 的形式专注于编写幻灯片的内容，并制作出具有交互式演示功能的、高度可自定义的幻灯片。 --- Slidev

```markdown
{{</* slidev src="https://sli.dev/demo/starter" aspect_ratio="16/9" */>}} <!-- 默认值 必须要有引号! -->
```

{{< slidev >}}

> [个人 slidev 仓库](https://github.com/WvW-vOiDs/slides) 的搭建参考了 [Thomas Boerger](https://github.com/tboerger/talks), [Anthony Fu](https://github.com/antfu/talks), [Haili Zhang](https://github.com/webup/openfunction-talks) 等人的项目.

> [!beamer]-
>
> 暂时没找到比较好的演示加教程, 先用随便找的一篇占位.
>
> {{< slidev "https://wvw-voids.github.io/slides/The-beamer-class-for-LATEX" "4/3" >}}

## 常用 html 代码

### 缩放

```markdown
<small>这是一段缩小文本</small> vs. 普通大小 vs. <big>放大文本</big>
```
<small>这是一段缩小文本</small> vs. 普通大小 vs. <big>放大文本</big>

### 颜色

```markdown
<font color=orange>橘色文本</font> vs. <font color=teal>水鸭色文本</font>
```
<font color=orange>橘色文本</font> vs. <font color=teal>水鸭色文本</font>

### 空格与换行

```markdown
文本间的&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;多个空格, 通过 html代码`&nbsp;` 实现.

文本间的换行<br><br><br><br><br>使用`<br>`实现.
```
文本间的&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;多个空格, 通过 html代码`&nbsp;` 实现.

文本间的换行<br><br><br><br><br>使用`<br>`实现.

## 其他细节展示

- 中文“引号” vs. 英文"引号"

- :smile: vs. 😄

  > [!Note]
  > 如果在配置文件里设置了 enableEmoji: true 则可以通过左边的方式输入emoji. 但无论true or false 都不影响直接输入 unicode版 emoji.

---
## References

- [Hugo.](https://github.com/gohugoio/hugo)
- [Hugo-PaperMod theme.](https://adityatelange.github.io/hugo-PaperMod/)
- [Hugo-FixIt theme.](https://fixit.lruihao.cn/)
- [随机图床.](https://t.alcy.cc/ycy)
- [The configuration block.](https://docs.mathjax.org/en/latest/options/input/tex.html#the-configuration-block)

## TODO

- [x]完善文章结构, 把测试内容更加完善更加有逻辑的整理完成.
- [ ]在本文基础上, 整理建站过程.
  - 修改字体引用文章: [1](https://github.com/adityatelange/hugo-PaperMod/discussions/506#discussioncomment-1205452), [2](https://huuuuuuo.github.io/post/hugo%E8%87%AA%E5%AE%9A%E4%B9%89%E5%AD%97%E4%BD%93/), [3](https://discourse.gohugo.io/t/what-is-the-preferred-way-to-change-the-default-font-in-the-hugo-book-theme/36130/2)
  - 个人隐私 blog 通过 submodule 导入到 repository 中, 并通过 .gitignore 不部署到网站上. submodule 通过[本地加密](https://github.com/AGWA/git-crypt)更新.