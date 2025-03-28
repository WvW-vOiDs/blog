---
# **************************************************************************** #
#                                 main settings                                #
# **************************************************************************** #

title: '必要的数学知识'
# subtitle: ""
slug: 'Foundational Math Knowledge' # 确保只有英文数字和空格

# =============================== taxonomies ================================= #
tags: []
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
draft: false
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
## Fourier 变换

### 基本知识和记号

1. 定义域有限 \(\implies\) 周期性.

1. 原胞默认 [Wigner-Seitz 原胞](https://en.wikipedia.org/wiki/Wigner%E2%80%93Seitz_cell).

1. 不写积分域的默认全空间 \( \mathbb{R}^d \) 积分.

1. 三角函数形式不再给出, 如有需要通过 Euler 公式 \( e^{i\theta} = \cos \theta + i \sin \theta \) 自行推导.

1. 实空间和倒空间一方的离散将导致另一方的周期性, 反之亦然. (离散间隔 \( \Leftrightarrow \) 周期)

1. 正交归一性由指数函数给出:

    \[\begin{aligned}
    & \int_{1Bz} \frac{\dd[d]{k}}{\Omega} e^{ik\cdot(R_l-R_{l^\prime})} = \delta_{l,l^\prime} ,\\
    & \int \frac{\dd[d]{k}}{(2\pi)^d} e^{ik\cdot (x-x^\prime)} = \delta(x-x^\prime).
    \end{aligned}\]

1. 任意维度的倒格矢: \( (b_i)_j = 2\pi \qty(A^{-1})_{ji} \). 其中,  \( a_i \) 为原胞基矢, \( A_{ij} \equiv (a_i)_j \).

1. 实空间原胞的体积为 \( V = \abs{\det A} \), 倒空间原胞 (1st Brillouin Zone) 的体积为: \( \Omega = (2\pi)^d / \abs{\det A} \).

1. Fourier 的一般形式 (1 dimensional 为例)[^一般形式]:

    \[\left\{\begin{aligned}
    F(k) &= \sqrt{(2\pi)^{a-1}\abs{b}} \int_{\mathbb{R}} \dd{x} f(x) \exp(i b k x),\\
    f(x) &= \sqrt{(2\pi)^{-a-1}\abs{b}} \int_{\mathbb{R}} \dd{k} F(k) \exp(-i b k x).
    \end{aligned}\right.\]
    - My Preferences (\( a=1,b=\pm 1 \)):
    \[\begin{aligned}
        F(k)=\int \dd{x} f(x) e^{-ikx} \quad \text{or} \quad F(\omega)=\int \dd{t} f(t) e^{i \omega t}.
    \end{aligned}\]
    - Engineering (**maybe** \( a=0 , b=-2\pi \)):
    \[
        F(\nu) = \int \dd{t} f(t) e^{-i 2\pi \nu t},\quad f(t)=\int \dd{\omega} F(\omega)  e^{i \omega t}.
    \]

[^一般形式]: Ref: [Mathematica](<https://reference.wolfram.com/language/ref/FourierTransform.html>)

### 实, 倒空间取值都连续: Fourier 变换

\[
\left\{
\begin{aligned}
    & f(x) = \int \frac{\dd[d]{k}}{(2\pi)^d} F(k) \exp(i k \cdot x) ,\\
    & F(k) = \int \dd[d]{x} f(x) \exp(-i k \cdot x).
\end{aligned}
\right.
\Leftrightarrow
\left\{
\begin{aligned}
    & f(x) = \int \frac{\dd[d]{k}}{\Omega} F(k) \exp(i k \cdot x) ,\\
    & F(k) = \int \frac{\dd[d]{x}}{V} f(x) \exp(-i k \cdot x).
\end{aligned}
\right.
\]

### 实, 倒空间取值一个离散一个连续: Fourier 级数

\[\left\{\begin{aligned}
    & f(x) = \sum_{h \in \mathbb{Z}^d}\frac{\Omega}{(2\pi)^d} F(k \equiv G_h) \exp(i G_h \cdot x)  = f(x+R_l),\\
    & F(k \equiv G_h) = \int_{V} \dd[d]{x} f(x) \exp(-i G_h \cdot x).
\end{aligned}\right.\]

\[\left\{\begin{aligned}
    & f(x \equiv R_l) = \int_{\Omega} \frac{\dd[d]{k}}{(2\pi)^d} F(k) \exp(i k \cdot R_l),\\
    & F(k) = \sum_{l \in \mathbb{Z}^d} V f(x \equiv R_l) \exp(-i k \cdot R_l) = F(k+G_h).
\end{aligned}\right.\]

### 实, 倒空间取值都离散: Discrete Fourier Transform (DFT)
\(Z_N=\qty{ n \mod N | n \in \mathbb{Z} }\) 是循环群, \( Z \equiv Z_{N_1}\bigotimes \cdots \bigotimes Z_{N_d} = \qty{n| n_i = h_i \;\text{mod}\; N_i , \forall h \in \mathbb{Z}^d, i=1,\cdots ,d } \).

\[
\begin{aligned}
    & f(x \equiv R_l) = \sum_{h \in Z } F(G_h) \exp( 2\pi i \sum_{j=1}^{d} h_j l_j/N_j),\\
    & F(k \equiv K_h) = \frac{1}{N_1 \cdots N_d} \sum_{l \in Z } f(R_l) \exp(-2\pi i \sum_{j=1}^{d} h_j l_j/N_j).
\end{aligned}
\]

### Some Examples

#### Delta 函数

\[
    \delta(x) = \int \frac{\dd[d]{k}}{(2\pi)^d} \; 1 \; e^{i k \cdot x}
\]

#### Dirac 梳

\[
    f(x) = \sum_{l \in \mathbb{Z}^d} \delta \qty(x-R_l) = \sum_{h \in \mathbb{Z}^d} \frac{1}{V} e^{i G_h \cdot x}
\]

## Dirac Delta 函数 和 Heaviside Step 函数

- \( \delta(a x) = \delta(x)/\abs{a} \).

- \( \int \dd{x} f(x) \; \delta^{(m)}(x-a) = (-1)^m f^{(m)}(a) \).

- 若 \( \phi(x)=0 \) 的实根 \( x_k \) 全是 **单根**, 则

    \[
        \delta\qty(\phi(x)) = \sum_{k} \frac{\delta(x-x_k)}{\abs{\phi^\prime(x_k)}}
    \]

- \( \ln(x) = \ln \abs{x} + i \pi H(-x) \qc{\forall x \in \mathbb{R}/\qty{0}} \).


## 其他

### 多元函数 Taylor 展开

\[
    f^\mu(x)=\exp(x^\nu \partial_\nu|_0) \; f^\mu.
\]


<!-- ============================ end document ============================= -->

<!-- =========================== begin appendix ============================ -->
---
## References

Some references.

## TODO

- [这里](#实-倒空间取值都离散-discrete-fourier-transform-dft) DFT 有没有更好的写法?