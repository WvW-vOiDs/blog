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
<!-- *********************************************************************** -->
<!--                              begin summary                              -->
<!-- *********************************************************************** -->

<!-- If nothing is written here, only the title and author will appear on the listing page. -->

**Summary:** 本文总结了个人觉得应该知道的数学内容.

<!-- ============================= end summary ============================= -->
<!--more-->
---
<!-- *********************************************************************** -->
<!--                             begin document                              -->
<!-- *********************************************************************** -->
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
        F(\nu) = \int \dd{t} f(t) e^{-i 2\pi \nu t},
        \quad
        f(t) = \int \dd{\nu} F(\nu)  e^{i 2\pi \nu t}.
    \]


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

#### Dirac Delta 函数

\[
    \delta(x) = \int \frac{\dd[d]{k}}{(2\pi)^d} \; 1 \; e^{i k \cdot x}
\]

#### Heaviside Step 函数

\[
    H(x) = \int \frac{\dd{k}}{2\pi} \; \qty\Big( \pi \delta(k) + \PV{\frac{1}{ik}} ) \; e^{i k x}
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
- \( \nabla^2(1/r) = -4\pi \delta(r) \).

- \( \ln x= \ln \abs{x} + i \pi H(-x) \implies (\ln x)^\prime = 1/x - i\pi \delta(x) \qc{\forall x \in \mathbb{R}/\qty{0}}.  \)
    \( \abs{x} = x \qty(H(x) - H(-x)) \implies (\abs{x})^\prime = H(x) - H(-x).\)

## 矩阵

### 行列式 与 迹



\[
    \det \exp A = \exp \tr A \; \Leftrightarrow \; \ln \det A = \tr \ln A.
\]

> [!Note]- Explicit form
> {{< raw >}}
\[\begin{aligned}
    & \det A = \exp \tr \ln A,\\
    & \tr A = \ln \det \exp A.
\end{aligned}\]
{{< /raw >}}

> [!Note]- 行列式的导数
> {{< raw >}}
\[
    \pdv{\det A}{t} = \det(A) \tr(A^{-1}\pdv{A}{t}).
\]
{{< /raw >}}

### 分解

#### 奇异值分解

[奇异值分解]^(Singular Value Decomposition). TODO...

#### 极分解

[极分解]^(Polar Decomposition) , 旨在将矩阵像复数那样分解成 **模** 和 **相因子** 之积的形式: \( z = r \exp(i\theta) \).

\(\forall \) [可逆的]^(invertible) \( A \in \mathbb{C}^{n\times n}, \exists !\) [幺正的]^(unitary) \( \exp(i\Theta )\) and [厄米的]^(Hermitian)  [半正定的]^(positive semi-definite) \( R \in \mathbb{C}^{n\times n} \) s.t.

\[
    A = R \exp(i\Theta).
\]
其中, \( R = \sqrt{A^\dagger A} \), \( \exp(i\Theta) = R^{-1}A \).

### Pauli 矩阵

#### 基础

- 定义

    {{< raw >}}
    \[
        \sigma_1 = \mqty(& 1\\1 &),
        \sigma_2 = \mqty(& -i\\i &),
        \sigma_3 = \mqty(1 &\\ & -1).
    \]
    {{< /raw >}}

- [厄米性]^(Hermiticity)

    {{< raw >}}
    \[
        \sigma_i = \sigma_i^\dagger.
    \]
    {{< /raw >}}

- 对易/反对易关系

    {{< raw >}}
    \[
    \begin{aligned}
        &\comm{\sigma_i}{\sigma_j} = 2i\, \epsilon^k{}_{ij}\, \sigma_k,\\
        &\acomm{\sigma_i}{\sigma_j} = 2\, \delta_{ij}\, 1_2.
    \end{aligned}
    \]
    {{< /raw >}}

    > [!note]- 推论
    > {{< raw >}}
    \[
        \sigma_i \sigma_j = \delta_{ij} 1_2 + i \epsilon^k{}_{ij}\,\sigma_k
    \]
    {{< /raw >}}
    >
    > {{< raw >}}
    \[
        \sigma_i = \sigma_i^\dagger = \sigma_i^{-1}
    \]
    {{< /raw >}}

#### 推论

\[
    (\va{a} \cdot \va{\sigma})(\va{b} \cdot \va{\sigma}) = \va{a}\cdot\va{b}\; 1_2 + \va{a}\times\va{b}\cdot\va{\sigma}.
\]

\[
    \exp(i\theta A) = \cos \theta \; 1_m + i \sin \theta A \qc{\forall A \in \mathbb{C}^{m\times m}, A^2 = 1_m}.
\]


## 其他

### 多元函数 Taylor 展开

\[
    f^\mu(x)=\exp(x^\nu \partial_\nu|_0) \; f^\mu.
\]

### Gauss 积分

对于正定的\( A \in \mathbb{R}^{d\times d} \), 有

\[
    \int_{\mathbb{R}^d} \dd[d]{x} \exp(-\frac{1}{2} x^T A x + B^T x + C) = \qty(\frac{(2\pi)^d}{\det A})^{1/2} \exp(\frac{1}{2} B^T A^{-1} B + C).
\]

其中, 由于只有 \( A \) 的对称部分才会对积分结果有影响, 故不妨令 \( A_{\mu\nu} \rightarrow A_{(\mu\nu)} \equiv [(A+A^T)/2]_{\mu\nu} \).
> [!note]- 补充
> {{< raw >}}
\[
    \partial_{B_{\mu}} \text{l.h.s.} = \int_{\mathbb{R}^d} \dd[d]{x} x_\mu \exp(-\frac{1}{2} x^T A x + B^T x + C)
\]
{{< /raw >}}


<!-- ============================ end document ============================= -->

---
<!-- *********************************************************************** -->
<!--                             begin appendix                              -->
<!-- *********************************************************************** -->
## References

- \( \det(\exp(A)) = \exp(\tr(A)) \) 的证明可以参考 [苏剑林's Blog](https://spaces.ac.cn/archives/6377).

## TODO

- [这里](#实-倒空间取值都离散-discrete-fourier-transform-dft) DFT 有没有更好的写法?

<!-- ============================ end appendix ============================= -->

<!-- *********************************************************************** -->
<!--                             begin footnotes                             -->
<!-- *********************************************************************** -->
[^一般形式]: Ref: [Mathematica](<https://reference.wolfram.com/language/ref/FourierTransform.html>).