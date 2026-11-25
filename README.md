# 单页分享

用于托管和分享独立页面的 GitHub Pages 仓库。每个页面都有自己的地址，图片等资源保存在仓库内。

入口：https://woo0ood.github.io/articles/

## 已有页面

- [如何在无数个标签页的潮汐里，记住一个人](https://woo0ood.github.io/articles/remembering-a-person-amid-tabs/)

## 添加页面

1. 新建 `page-slug/index.md`，front matter 设置 `layout: share`、`title`，填写 `description` 和封面 `image`；`date` 使用带时区的发布时间。
2. 将配图放到 `assets/images/page-slug/`，使用 `{{ '/assets/images/page-slug/image.png' | relative_url }}` 引用。
3. 也可以直接新建完整的 `page-slug/index.html`，不写 front matter，使用该页面自己的 HTML、CSS 和 JavaScript。
4. 推送到 `main`，GitHub Pages 自动发布。使用 `share` 布局的页面会在入口列出；独立 HTML 页面通过各自的地址分享。

每个分享页只呈现标题、发布时间、分隔线和自身内容，不显示站点导航、归档、分类或标签。

## 分享卡片

`share` 布局自动输出 Open Graph 和 Twitter/X 大图卡片标签。标题、概要、封面和页面地址写入静态 HTML，抓取时无需运行 JavaScript。

- 每页用 `title`、`description`、`image`、`image_alt` 定义分享内容，图片路径会转换为当前 GitHub Pages 站点的绝对 HTTPS 地址。
- 按图片的实际信息填写 `image_width`、`image_height`、`image_type`，例如 `image/png`。更换封面时一起更新。
- 未指定封面的页面使用 `_config.yml` 的默认图片；新页面最好单独指定与内容相关的封面。
- `date` 同时用于页面显示和 `article:published_time`。站点时区为 UTC+8。
- 使用完整 HTML 的独立页面需要自行提供这些标签；不经过共享布局。

## 本地预览

安装 Ruby 与 Bundler 后，在仓库目录运行：

```bash
bundle install
bundle exec jekyll serve --baseurl /articles
```

打开 `http://localhost:4000/articles/`。生成的 `_site/` 已被 Git 忽略。

正文与图片的权利归原作者所有。
