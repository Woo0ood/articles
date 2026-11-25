# Wood 的文章

用于分享文章的 GitHub Pages 站点。使用 GitHub Pages 自带的 Jekyll 渲染 Markdown，正文和配图均保存在仓库内。

- 首页：https://woo0ood.github.io/articles/
- 博客：https://v2c.life

## 文章

- [如何在无数个标签页的潮汐里，记住一个人](https://woo0ood.github.io/articles/remembering-a-person-amid-tabs/) · 2026-11-25 21:49:32（UTC+8）

## 添加文章

1. 在 `_posts/` 新建 `YYYY-MM-DD-article-slug.md`。
2. 参考已有文章填写 front matter：`layout`、`title`、带时区的 `date`、`category`、`tags`、`description`。
3. 将配图放到 `assets/images/article-slug/`，用 `{{ '/assets/images/article-slug/image.png' | relative_url }}` 引用。可参考已有文章将图片链接到原图。
4. 如果同文也发布于博客，可填写 `original_url`；该地址用作 canonical 和原文链接。
5. 推送到 `main`，GitHub Pages 自动构建并发布，首页自动收录新文章。

## 本地预览

安装 Ruby 与 Bundler 后，在仓库目录运行：

```bash
bundle install
bundle exec jekyll serve --baseurl /articles
```

打开 `http://localhost:4000/articles/`。本地生成的 `_site/` 已被 Git 忽略。

正文与图片的权利归原作者所有。
