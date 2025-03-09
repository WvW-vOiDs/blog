---
# **************************************************************************** #
#                                   metadata                                   #
# **************************************************************************** #
date: "2024-12-30T12:03:13+08:00"
title: "Test Demo"
slug: "test-demo"


description: "Description 将会在 single page 展示. 本文用于测试网站功能."
summary: "Summary 将会在list page展示. 本文用于测试网站功能."
# hideSummary: false # 如果写summary就取消注释

tags: ["markdown", "Hugo", "TODO"] # 关键词
categories: ["Draft"] # 文件夹结构
collections: ["博客搭建"] # 合集: 用于更新系列文章, 如: "量子力学抄书笔记"

# **************************************************************************** #
#                                     页面设置                                     #
# **************************************************************************** #
# =================================== model ================================== #
draft: false
# weight: 1 # 需要置顶时使用

# ================================= component ================================ #
# ShowToc: false # 默认 true
# TocOpen: false # 默认 true

# ShowReadingTime: true # 默认 false
# ShowWordCount: true # 默认 false

# ================================== search ================================== #
# searchHidden: true # 默认 false

# =================================== cover ================================== #
cover:
    image: "https://t.alcy.cc/ycy" # image path/url
    # can also paste direct link from external site
    # ex. https://i.ibb.co/K0HVPBd/paper-mod-profilemode.png
    alt: "封面是随机图片" # alt text
    caption: "随机图片" # display caption under cover
    relative: false # To use relative path for cover image, used in hugo Page-bundles
    # hidden: true # only hide on current single page

# **************************************************************************** #
#                                     其他设置                                     #
# **************************************************************************** #

# ================================== mathjax ================================= #
# mathjax: false # 禁止 mathjax 渲染 latex 公式
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
> 前者会导致默认生成的锚点 (上例中即为 `#markdown-基本语法`) 无法使用, 取而代之为自定义的锚点名称 (上例中即为 `#custon-id`). 后者则是两个锚点名均可使用并且定位到相同位置.

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

本节内容为 FixIt 主题定制版语法. 与上节相同, 本节内容全部来自于 [FixIt 官方介绍文档](https://fixit.lruihao.cn/zh-cn/documentation/content-management/markdown-syntax/extended/).

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

### 下划线, 高亮 和 上下标

在 加粗, 斜体, 删除线 的基础 markdown 语法上, FixIt 定义了类似的扩展语法:
```md {data-open=true}
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
> 这是++下划线++.<br>
> 这是==高亮==.<br>
> 这是^上标^.<br>
> 这是~下标~.<br>
> <br>
> 其他高亮颜色:<br>
> ==Primary==[primary]
> ==Secondary==[secondary]
> ==Success==[success]
> ==Info==[info]
> ==Warning==[warning]
> ==Danger==[danger]

其中, 上标已禁用, 因为有时会和[文字上方标记](#字符注音或者注释)冲突.

### 数学公式

FixIt 原本使用 [KaTeX](https://katex.org/) 对 LaTeX 语法提供支持. 但由于个人对宏包有较多需求, 故暂时使用了一个 **破坏性的** 方法强制使用 [MathJax](https://www.mathjax.org/). 具体情况见:
{{< link href="https://github.com/hugo-fixit/FixIt/issues/574" content="[FEATURE] Add MathJax Support as an Alternative Renderer" title="[FEATURE] Add MathJax Support as an Alternative Renderer" card=true card-icon="fa-brands fa-github fa-fw" >}}

TO BE CONTINUED...



markdown 插入图片:

![随机图床](https://t.alcy.cc/ycy "随机图床")

Hugo short-code 插入图片:

{{< figure
    src="https://t.alcy.cc/ycy"
    alt="随机图床"
    link="https://t.alcy.cc/ycy"
    caption="随机图床"
    class="ma0 w-75"
>}}

html 插入图片:

<img
    src="https://t.alcy.cc/ycy"
    alt="随机图床"
    title="点击刷新"
    class="ma0 w-75"
    onclick="src=src+'?'+Math.random() * 5;">

总体来说越靠后的方法功能越全面, 但是语法也会越复杂.

---

插入 slides:

- [slidev](https://sli.dev)

<iframe
    src="https://sli.dev/demo/starter"
    style="width: 100%; aspect-ratio: 16/9; border: none;"
></iframe>

参考了 [Thomas Boerger](https://github.com/tboerger/talks), [Anthony Fu](https://github.com/antfu/talks), [Haili Zhang](https://github.com/webup/openfunction-talks) 等人的项目.

- beamer (deepseek-r1 生成)

<iframe
    id="deepseek-r1 生成"
    src="./slides/beamer/main.pdf#toolbar=1"
    style="width: 100%; aspect-ratio: 16/10; border: none;"
></iframe>

---

|这里是表头1|这里是表头2|这里是表头3|
|:-|:-:|-:|
|单元格数据1|单元格数据2|单元格数据3|
|居左|居中|居右|
|1|可以使用`<br>`<br>换行|1|

---

`````markdown
代码块的嵌套:
````markdown
可以再嵌套一层:
```markdown
中间的也是代码块
```
````
`````
``` 行内代码的`` 嵌套 `测试` `` ```

LaTeX 支持: \(\mathrm{e}^{\mathrm{i}x} = \cos x+ \mathrm{i}\sin x\)

---

博客内文章引用测试 (使用内置 short code 实现[^ 博客内引用]):

代码块更多效果见下文[代码测试]({{< ref "#代码测试" >}} "代码测试")

[^ 博客内引用]: https://gohugo.io/shortcodes/ref/ and https://gohugo.io/shortcodes/relref/
---

- [ ] 这是代办项目.
    - [ ] 缩进测试.
        - [x] 缩进测试.
- [x] 这是已办项目.

---
<!-- 单行注释测试 -->

<!--
多行
注释
测试
-->

```markdown
<!-- 单行注释测试 -->

<!--
多行
注释
测试
-->
```

---

```markdown
[哔哩哔哩][变量名]

[变量名]: https://www.bilibili.com
```

[哔哩哔哩][变量名]

[变量名]: https://www.bilibili.com

---

脚注测试[^变量名].

[^变量名]: 这是脚注.

---

常用 html 代码:

<small>这是一段缩小文本</small> vs. 普通大小 vs. <big>放大文本</big>

<font color=orange>橘色文本</font> vs. <font color=teal>水鸭色文本</font>

==高亮== vs. <mark>高亮</mark>

---

中文“引号” vs. 英文"引号"

---

:smile: vs. 😄

> PS: 如果在配置文件里设置了 enableEmoji: true 则可以通过左边的方式输入emoji. 但无论true or false 都不影响直接输入 unicode版 emoji.

---

转义字符测试:
\\ \* \_ \# \-

---

文本间的&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;多个空格, 通过 html代码`&nbsp;` 实现.

文本间的换行<br><br><br><br><br>使用`<br>`实现.

---

> [!NOTE]
> Useful information that users should know, even when skimming content.

> [!TIP]
> Helpful advice for doing things better or more easily.

> [!IMPORTANT]
> Key information users need to know to achieve their goal.

> [!WARNING]
> Urgent info that needs immediate user attention to avoid problems.

> [!CAUTION]
> Advises about risks or negative outcomes of certain actions.

> [!WARNING]+ Radiation hazard
> Do not approach or handle without protective gear.

---

- [ ] 未完成
- [x] 已完成
- [/] 进行中
- [-] 已取消
- [<] 已计划
- [>] 已重新计划
- [!] 重要
- [?] 问题

---

[extras](https://gohugo.io/getting-started/configuration-markup/#extras):

~~foo~~

++bar++

==baz==

H~2~O

1^st^

---
<!--
音频嵌入测试:

<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="//music.163.com/outchain/player?type=2&id=2614222287&auto=0&height=66"></iframe> -->

<!-- 视频嵌入测试:

<iframe width=720 height=400 src="https://player.bilibili.com/player.html?bvid=BV1aTvieqEfw&autoplay=0" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe> -->

<!-- 网页嵌入测试:

<iframe width=720 height=400 src="https://www.bilibili.com/" scrolling="auto" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe> -->

---

GoAT diagrams:
```goat
+-------------------+                           ^                      .---.
|    A Box          |__.--.__    __.-->         |      .-.             |   |
|                   |        '--'               v     | * |<---        |   |
+-------------------+                                  '-'             |   |
                       Round                                       *---(-. |
  .-----------------.  .-------.    .----------.         .-------.     | | |
 |   Mixed Rounded  | |         |  / Diagonals  \        |   |   |     | | |
 | & Square Corners |  '--. .--'  /              \       |---+---|     '-)-'       .--------.
 '--+------------+-'  .--. |     '-------+--------'      |   |   |       |        / Search /
    |            |   |    | '---.        |               '-------'       |       '-+------'
    |<---------->|   |    |      |       v                Interior                 |     ^
    '           <---'      '----'   .-----------.              ---.     .---       v     |
 .------------------.  Diag line    | .-------. +---.              \   /           .     |
 |   if (a > b)     +---.      .--->| |       | |    | Curved line  \ /           / \    |
 |   obj->fcn()     |    \    /     | '-------' |<--'                +           /   \   |
 '------------------'     '--'      '--+--------'      .--. .--.     |  .-.     +Done?+-'
    .---+-----.                        |   ^           |\ | | /|  .--+ |   |     \   /
    |   |     | Join        \|/        |   | Curved    | \| |/ | |    \    |      \ /
    |   |     +---->  o    --o--        '-'  Vertical  '--' '--'  '--  '--'        +  .---.
 <--+---+-----'       |     /|\                                                    |  | 3 |
                      v                             not:line    'quotes'        .-'   '---'
  .-.             .---+--------.            /            A || B   *bold*       |        ^
 |   |           |   Not a dot  |      <---+---<--    A dash--is not a line    v        |
  '-'             '---------+--'          /           Nor/is this.            ---
```

---

Hugo does not provide a built-in template for Mermaid diagrams.[^hugo_diagram]
[^hugo_diagram]: https://gohugo.io/content-management/diagrams/

---



## 数学公式测试

### 行内公式
*code*:
```LaTeX
这是一个行内公式 \(a^*=x-b^*\).
```

*output*:
这是一个行内公式 \(a^*=x-b^*\).


### 行间公式

这些是行间公式:

1.
*code*:
```latex
\[a^*=x-b^*.\]
```

*output*:

\[a^*=x-b^*.\]

2.
*code*:
```latex
\[ a^*=x-b^*. \]
```

*output*:

\[ a^*=x-b^*. \]

3.
*code*:
```LaTeX
\[
    a^*=x-b^*.
\]
```

*output*:

\[
    a^*=x-b^*.
\]

4.
*code*:
```latex
化学方程式：
\ce{CO2 + C -> 2CO}
```
\[
\ce{CO2 + C -> 2CO}
\]

### physics 宏包

现在用的 Mathjax 的cdn不是很稳定, 有时候本地渲染不出来.

1.
*code*:
```latex
\[
    \mqty(1 & 2 \\ 3 & 4)
\]
```

*output*:

\[
    \mqty(1 & 2 \\ 3 & 4)
\]

2.
*code*:
```latex
\[
    \ip{\psi}{\phi}
\]
```

*output*:

\[
    \ip{\psi}{\phi}
\]

3. 带有 `<` 的公式.

> 注意!
>
> `<` 后 **一定** 要接一个空格 (或使用 `\lt` 代替 `<` 以强制提醒自己加空格), 否则会当成 html 的标签而无法渲染.[^无法渲染]

[^无法渲染]: https://discourse.gohugo.io/t/math-equations-with-the-less-than-sign-cant-render-correctly/52890

*code*:
```latex
\[
    x < y, x\lt y
\]
```

*output*:

\[
    x < y, x\lt y
\]


### 超过3个大括号的公式

根据 [SonnyCalcr的博客](https://sonnycalcr.github.io/posts/build-a-blog-using-hugo-papermod-github-pages/#%E9%85%8D%E7%BD%AE%E6%95%B0%E5%AD%A6%E5%85%AC%E5%BC%8F) 所说:

> ...数学公式如果有超过了三对花括号, 那么, 其解析和转义就会出问题...

但在本文中尚未遇到, 可能是此 bug 已被修复?

*code*:
```LaTeX
\[
    \boldsymbol{x}_{i+1} + \boldsymbol{x}_{i+2} = \boldsymbol{x}_{i+3}
\]
```

*output*:

\[
    \boldsymbol{x}_{i+1} + \boldsymbol{x}_{i+2} = \boldsymbol{x}_{i+3}
\]


## 代码测试

### 行内代码

*code*:
```md
`This is Inline Code.`
```

*output*:
`This is Inline Code.`




### 行间代码

1. 普通\`\`\`代码块.

```
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>Example HTML5 Document</title>
        <meta
            name="description"
            content="Sample article showcasing basic Markdown syntax and formatting for HTML elements."
        />
    </head>
    <body>
        <p>Test</p>
    </body>
</html>
```

2. \`\`\`代码块加语言类型声明.

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>Example HTML5 Document</title>
        <meta
            name="description"
            content="Sample article showcasing basic Markdown syntax and formatting for HTML elements."
        />
    </head>
    <body>
        <p>Test</p>
    </body>
</html>
```

3. \`\`\`代码块加语言类型声明, 并且增加行号. [^行号]

[^行号]: 和上一个一样是因为我默认设置了代码块有行号.

```html {linenos=true}
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>Example HTML5 Document</title>
        <meta
            name="description"
            content="Sample article showcasing basic Markdown syntax and formatting for HTML elements."
        />
    </head>
    <body>
        <p>Test</p>
    </body>
</html>
```

4. \`\`\`代码块加语言类型声明, 有行号, 并且有 <mark>高亮</mark> 代码.

```html {linenos=true,hl_lines=["2-4",8,11]}
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>Example HTML5 Document</title>
        <meta
            name="description"
            content="Sample article showcasing basic Markdown syntax and formatting for HTML elements."
        />
    </head>
    <body>
        <p>Test</p>
    </body>
</html>
```

5. 还可以设置初始行号, 和代码行号 url 的前缀. (如果需要可以把前缀设置成这段 code 的文件名等)

```html {linenos=true,hl_lines=["2-4",8,11],linenostart=199,lineanchors=prefixOfCode}
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>Example HTML5 Document</title>
        <meta
            name="description"
            content="Sample article showcasing basic Markdown syntax and formatting for HTML elements."
        />
    </head>
    <body>
        <p>Test</p>
    </body>
</html>
```


### Github Gist

[The gist shortcode was deprecated in version 0.143.0 and will be removed in a future release. To continue embedding GitHub Gists in your content, you’ll need to create a custom shortcode](https://gohugo.io/shortcodes/gist/)

---
# References

- [hugo.](https://github.com/gohugoio/hugo)
- [hugo-PaperMod theme.](https://adityatelange.github.io/hugo-PaperMod/)
- [hugo-FixIt theme.](https://fixit.lruihao.cn/)
- [随机图床.](https://t.alcy.cc/ycy)
- [MarkDown语法 超详细教程.](https://forum-zh.obsidian.md/t/topic/435)
- [The configuration block.](https://docs.mathjax.org/en/latest/options/input/tex.html#the-configuration-block)

# TODO

- 完善文章结构, 把测试内容更加完善更加有逻辑的整理完成.
- 在本文基础上, 整理建站过程.
    - 修改字体引用文章: [1](https://github.com/adityatelange/hugo-PaperMod/discussions/506#discussioncomment-1205452), [2](https://huuuuuuo.github.io/post/hugo%E8%87%AA%E5%AE%9A%E4%B9%89%E5%AD%97%E4%BD%93/), [3](https://huuuuuuo.github.io/post/hugo%E8%87%AA%E5%AE%9A%E4%B9%89%E5%AD%97%E4%BD%93/), [4](https://discourse.gohugo.io/t/what-is-the-preferred-way-to-change-the-default-font-in-the-hugo-book-theme/36130/2)
    - slug: [1](https://gohugo.io/content-management/urls/#slug)
- 插入 [GeoGebra](https://geogebra.github.io/docs/reference/en/GeoGebra_Apps_Embedding/).