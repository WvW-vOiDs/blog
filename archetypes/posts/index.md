---
# **************************************************************************** #
#                                 main settings                                #
# **************************************************************************** #

title: '{{ replace .ContentBaseName "-" " " | title }}'
# subtitle: ""
slug: '{{ replace .ContentBaseName "-" " " | title }}' # 确保只有英文数字和空格

# =============================== taxonomies ================================= #
tags: ["TODO"]
categories: ["Draft"] # 文件夹结构
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
# math: false # 禁止 mathjax 渲染 latex 公式

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
date: {{ .Date }}
# ---------------------------------------------------------------------------- #
---
<!-- *********************************************************************** -->
<!--                              begin summary                              -->
<!-- *********************************************************************** -->

<!-- If nothing is written here, only the title and author will appear on the listing page. -->

**Summary:**

<!-- ============================= end summary ============================= -->
<!--more-->
---
<!-- *********************************************************************** -->
<!--                             begin document                              -->
<!-- *********************************************************************** -->








<!-- ============================ end document ============================= -->
---
<!-- *********************************************************************** -->
<!--                             begin appendix                              -->
<!-- *********************************************************************** -->
## References

Some references.

## TODO

- [ ] TODO list items.

<!-- ============================ end appendix ============================= -->

<!-- *********************************************************************** -->
<!--                             begin footnotes                             -->
<!-- *********************************************************************** -->
