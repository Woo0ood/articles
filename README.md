# 单页分享

用于托管和分享独立页面的 GitHub Pages 仓库。每个页面都有自己的地址，图片等资源保存在仓库内。

入口：https://woo0ood.github.io/articles/

## 已有页面

- [如何在无数个标签页的潮汐里，记住一个人](https://woo0ood.github.io/articles/remembering-a-person-amid-tabs/)

## 添加页面

1. 新建 `page-slug/index.md`，front matter 设置 `layout: share`、`title`，按需填写 `description` 和 `image`。
2. 将配图放到 `assets/images/page-slug/`，使用 `{{ '/assets/images/page-slug/image.png' | relative_url }}` 引用。
3. 也可以直接新建完整的 `page-slug/index.html`，不写 front matter，使用该页面自己的 HTML、CSS 和 JavaScript。
4. 推送到 `main`，GitHub Pages 自动发布。使用 `share` 布局的页面会在入口列出；独立 HTML 页面通过各自的地址分享。

每个分享页只呈现自身内容，不显示站点导航、归档、分类或标签。

## 本地预览

安装 Ruby 与 Bundler 后，在仓库目录运行：

```bash
bundle install
bundle exec jekyll serve --baseurl /articles
```

打开 `http://localhost:4000/articles/`。生成的 `_site/` 已被 Git 忽略。

正文与图片的权利归原作者所有。
