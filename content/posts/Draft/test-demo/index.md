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

# h1
## h2
### h3
#### h4
##### h5
###### h6

# Markdown 语法测试

## 基本 markdown 语法

1. 有序列表
    1. 有序列表
        1. 有序列表
            1. 有序列表
2. 有序列表
3. 有序列表


---

- 无序列表
    - 无序列表
        - 无序列表
            - 无序列表
- 无序列表
- 无序列表

---

正常|**加粗**|_斜体_|***粗斜体***|_斜体**包含粗体**斜体_|__粗体*包含斜体*粗体__.[^粗斜体]

[^粗斜体]: 粗中有斜和斜中有粗只能外面`_`, 里面`*`.

~~删除线~~

<u>下划线</u> (html `<u>` 实现)

---

> 引用
>> 引用一级缩进
>>> 引用二级缩进
>>
>>>引用二级缩进
>
>> 引用一级缩进

---

网页链接测试: [哔哩哔哩](https://www.bilibili.com/ "哔哩哔哩 干杯!").

---

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

<!-- <iframe
    src="https://sli.dev/demo/starter"
    style="width: 100%; aspect-ratio: 16/9; border: none;"
></iframe> -->

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

上标^测试^ vs. 下标~测试~

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

[extras:](https://gohugo.io/getting-started/configuration-markup/#extras):

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


### 预格式化文本 (preformatted text)

*code*:
```html
<pre>
这是一些
    预格式化的文本.
    空格 和 换行符
        都会被保留.111
</pre>
```

*output*:
<pre>
这是一些
    预格式化的文本.
    空格 和 换行符
        都会被保留.111
</pre>


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
- [hugo-PaperMod.](https://github.com/adityatelange/hugo-PaperMod)
- [随机图床.](https://t.alcy.cc/ycy)
- [MarkDown语法 超详细教程.](https://forum-zh.obsidian.md/t/topic/435)
- [The configuration block.](https://docs.mathjax.org/en/latest/options/input/tex.html#the-configuration-block)

# TODO

- 完善文章结构, 把测试内容更加完善更加有逻辑的整理完成.
- 在本文基础上, 整理建站过程.
    - 修改字体引用文章: [1](https://github.com/adityatelange/hugo-PaperMod/discussions/506#discussioncomment-1205452), [2](https://huuuuuuo.github.io/post/hugo%E8%87%AA%E5%AE%9A%E4%B9%89%E5%AD%97%E4%BD%93/), [3](https://huuuuuuo.github.io/post/hugo%E8%87%AA%E5%AE%9A%E4%B9%89%E5%AD%97%E4%BD%93/), [4](https://discourse.gohugo.io/t/what-is-the-preferred-way-to-change-the-default-font-in-the-hugo-book-theme/36130/2)
    - slug: [1](https://gohugo.io/content-management/urls/#slug)
- 插入 [GeoGebra](https://geogebra.github.io/docs/reference/en/GeoGebra_Apps_Embedding/).