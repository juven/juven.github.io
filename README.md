# juven.github.io

许晓斌的个人主页 / Personal site of Xu Xiaobin.

- Live: https://juven.github.io
- Source: [`juven/juven.github.io`](https://github.com/juven/juven.github.io)
- 在 wiki 中作为 submodule 挂在 `site/`

## 本地预览

```sh
bundle install
bundle exec jekyll serve
# http://localhost:4000
```

## 添加博文

文件放在 `_posts/`，命名 `YYYY-MM-DD-title.md`，front matter 示例：

```yaml
---
layout: post
title: "标题"
date: 2026-05-13 23:30:00 +0800
categories: tag
---
```

## 主题 / 工具

- [Jekyll](https://jekyllrb.com/) + [minima](https://github.com/jekyll/minima)
- GitHub Pages 原生构建（无需 Actions）
