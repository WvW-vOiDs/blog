---
# **************************************************************************** #
#                                   metadata                                   #
# **************************************************************************** #

date: "2025-02-21T15:54:59+08:00"
title: "Should Know"
# author: "Me" # ["Me", "You"]
slug: "should-know"

tags: []
categories: ["Math"]

# description: "Description 将会在single page顶部展示."
# summary: "Summary 将会在list page展示."
# hideSummary: false # 如果写summary就取消注释

# **************************************************************************** #
#                                     页面设置                                     #
# **************************************************************************** #
# =================================== model ================================== #
draft: true
# weight: 1 # 需要置顶时使用

# ================================= component ================================ #
# ShowToc: false # 默认true
# TocOpen: false # 默认true

# ShowReadingTime: true # 默认false
# ShowWordCount: true # 默认false

# searchHidden: true # 默认false

# =================================== cover ================================== #
# cover:
#     image: "<image path/url>" # image path/url

#     alt: "<alt text>" # alt text
#     caption: "<text>" # display caption under cover
#     relative: false # To use relative path for cover image, used in hugo Page-bundles
#     hidden: true # only hide on current single page

# **************************************************************************** #
#                                     其他设置                                     #
# **************************************************************************** #

# ================================== mathjax ================================= #
# mathjax: false # 禁止 mathjax 渲染 latex 公式
---

<!-- ================================= 正文 ================================== -->
# Fourier 级数 和 Fourier 变换

## 周期函数的 Fourier 级数

### 一维情况

若函数 \(f(x)\) 的周期为 \(\lambda\) (\(k \equiv 2\pi/\lambda\)), 则

\[
\begin{aligned}
    f(x)&=\qty(\frac{a_0}{2}+\sum_{n=1}^{\infty}\qty( a_n \cos(nk\,x) + b_n \sin(nk\,x) ) )\frac{k}{2\pi}\\
    &= \sum_{n=-\infty}^{\infty}\qty( c_n \cos(nk\,x) + d_n \sin(nk\,x) ) \cdot \frac{k}{2\pi}\\
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

### 高维情况

若 \(f(x)\) 是 \(n\) 维周期函数, 周期为 \( a_1, a_2, \dots, a_n \).[^数量小于维数]

[^数量小于维数]: 若只有 \( k<n \) 个方向有周期, 则只需将 \( f(x) \) 视为 \( k \) 维函数, 剩下的\( n-k \) 维视作参数处理即可.

<!-- ================================ 参考文献 ================================= -->
# References

Some references.
