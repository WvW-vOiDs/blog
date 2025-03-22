---
# **************************************************************************** #
#                                 main settings                                #
# **************************************************************************** #

title: '必要的数学知识'
# subtitle: ""
slug: 'Foundational Math Knowledge' # 确保只有英文数字和空格

# =============================== taxonomies ================================= #
tags: ["TODO"]
categories: ["Math"] # 文件夹结构
collections: [] # 合集: 用于更新系列文章, 如: "量子力学抄书笔记"

# ========================== additional information ========================== #
# keywords: ""
# description: "" # 鼠标悬停在 cover 上显示的文字
# summary: "" # 如果想只让 summary 出现在 list page 且不在文章前出现, 则写在这里 且 删掉正文前的 more 注释, 否则写在下面的正文前.
# ---------------------------------------------------------------------------- #


# **************************************************************************** #
#                               optional settings                              #
# **************************************************************************** #

# =================================== cover ================================== #
# featuredImage: "https://t.alcy.cc/ycy" # 文章的特色图片 在文章开始展示
# featuredImagePreview: "images/cover.jpg" # 用在主页预览的文章特色图片, 不设置则默认和 featuredImage 相同

# ================================== author ================================== #
# author:
#     name: "Me" # 文章作者
#     link: "https://example.com" # 文章作者的链接
#     email: "me@me.com" # 文章作者的邮箱，用于设置 Gravatar 头像，优先于 `author.avatar`
#     avatar: "" # 文章作者的头像

# ================================== mathjax ================================= #
# mathjax: false # 禁止 mathjax 渲染 latex 公式

# ================================ encryption ================================ #
# password: "1234" # [必需] 加密页面内容的密码
# message: "密码是 1234" # [可选] 加密提示信息
# ---------------------------------------------------------------------------- #


# **************************************************************************** #
#                              blog configuration                              #
# **************************************************************************** #

# =================================== model ================================== #
type: posts
draft: true
# weight: 1 # 需要置顶时使用

# ================================= component ================================ #
# ShowToc: false # 默认 true
# TocOpen: false # 默认 true

# readingTime: false # 默认 true
# wordCount: false # 默认 true
# expirationReminder: true # 默认 false, 若设为 true, 则如果文章最后更新于 90 天之前, 显示提醒; 如果文章最后更新于 180 之前, 显示警告.

# linkToMarkdown: true # 默认 false, 如果设为 true, 内容的页脚将显示指向原始 Markdown 文件的链接
# linkToSource: false # 默认 true, 如果设为 true, 内容的页脚将显示指向源码的链接
# linkToEdit: false # 默认 true, 如果设为 true, 内容的页脚将显示指向编辑页面的链接
# linkToReport: false # 默认 true, 如果设为 true, 内容的页脚将显示指向报告问题的链接

# ================================== hidden ================================== #
# hiddenFromHomePage: true # 默认 false, 如果设为 true, 这篇文章将不会显示在主页上
# hiddenFromSearch: true # 默认 false, 如果设为 true, 这篇文章将不会显示在搜索结果中
# hiddenFromRelated: true # 默认 false, 如果设为 true, 这篇文章将不会显示在相关文章中
# hiddenFromFeed: true # 默认 false, 如果设为 true, 这篇文章将不会显示在 RSS、ATOM 和 JSON Feed 中
# ---------------------------------------------------------------------------- #


# **************************************************************************** #
#                            ​preset configurations                             #
# **************************************************************************** #
date: 2025-02-21T15:54:59+08:00
# ---------------------------------------------------------------------------- #
---
<!-- ============================ begin summary ============================ -->
<!-- If nothing is written here, only the title and author will appear on the listing page. -->

**Summary:** 本文总结了个人觉得应该知道的数学内容.

<!-- ============================= end summary ============================= -->
<!--more-->
---
<!-- =========================== begin document ============================ -->
## Fourier 级数 和 Fourier 变换

### 周期函数的 Fourier 级数

#### 一维情况

若函数 \(f(x)\) 的周期为 \(\lambda\) (\(k \equiv 2\pi/\lambda\)), 则

\[
\begin{aligned}
    f(x)&=\qty(\frac{a_0}{2}+\sum_{n=1}^{\infty}\qty( a_n \cos(nk\,x) + b_n \sin(nk\,x) ) )\frac{k}{2\pi}\\
    &= \sum_{n=-\infty}^{\infty}\qty\Big( c_n \cos(nk\,x) + d_n \sin(nk\,x) ) \cdot \frac{k}{2\pi}\\
    &= \sum_{n=-\infty}^{\infty} \qty(g_n e^{ink\,x}) \frac{k}{2\pi}.
\end{aligned}
\]

其中,

\[
\left\{
\begin{aligned}
    a_n&= 2 \int_0^\lambda  f(y)\cos(nk\,y) \, \dd y,\\
    b_n&= 2 \int_0^\lambda  f(y)\sin(nk\,y) \, \dd y.
\end{aligned}
\right.
\]

\[
\left\{
\begin{aligned}
    c_n&= \int_0^\lambda  f(y)\cos(nk\,y) \, \dd y,\\
    d_n&= \int_0^\lambda  f(y)\sin(nk\,y) \, \dd y.
\end{aligned}
\right.
\]

\[
    g_n= \int_0^\lambda  f(y)e^{-ink\,y} \, \dd y.
\]

#### 高维情况

若 \(f(x)\) 是 \(n\) 维周期函数, 周期为 \( a_1, a_2, \dots, a_n \).[^数量小于维数]

[^数量小于维数]: 若只有 \( k< n \) 个方向有周期, 则只需将 \( f(x) \) 视为 \( k \) 维函数, 剩下的\( n-k \) 维视作参数处理即可.



<!-- ============================ end document ============================= -->

<!-- =========================== begin appendix ============================ -->
---
## References

Some references.