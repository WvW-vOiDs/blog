# 常用命令

- 本地 build

```bash
 hugo server -D --disableFastRender --environment production --ignoreCache
```

- 手动更新主题

```bash
git submodule update --remote --merge themes/FixIt
```

# Conventional commit

| 标准类型         | 功能                                                                 |
|-----------------|----------------------------------------------------------------------|
| `post`          | **发布新文章** (替代 `feat`, 专用于内容创作)                              |
| `update`        | **更新已有文章** (如补充段落、修正过时信息)                                |
| `fix`           | **修正错误** (如文章中的技术错误、死链修复等)                              |
| `media`         | **媒体文件更新** (新增/替换图片、视频、音频等)                             |
| `refactor`      | **内容重构** (重新组织文章结构, 优化逻辑流)                               |
| `translate`     | **翻译内容** (新增或更新多语言版本)                                       |
| `docs`          | **项目文档更新**                                       |
| `feat`          | **技术功能新增**                                     |
| `meta`          | **元数据修改** (如调整文章分类、标签、SEO关键词等)                         |
| `seo`           | **SEO 优化** (如添加 Alt 文本、优化标题、调整 sitemap)                    |
| `style`         | **排版或样式调整** (如 Markdown 格式、代码高亮、CSS 美化)                 |
| `chore`         | **维护性任务** (如更新依赖、清理冗余文件)                                 |