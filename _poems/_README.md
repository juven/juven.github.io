---
# This file is ignored by Jekyll because of the leading underscore.
# Acts as inline doc for how to add poems to this collection.
---

# 怎么加一首诗

在 `_poems/` 下新建 `.md` 文件（**不要**用 `_` 开头）。文件名就是 URL 的 slug。

## Front matter 范例

```yaml
---
title: 五月的雨
date: 2026-05-14
place: 杭州          # 可选
subtitle: 给 H        # 可选
---
```

## 正文 / 怎么处理换行

诗歌里换行的语义和散文不一样，约定如下：

- **节内的换行**：每行末尾打 **两个空格**，再回车（Markdown 的 hard break 语法）
- **节之间**：一个空行（Markdown 的段落间隔）

例子：

```
山中何所有  
岭上多白云  
只可自怡悦  
不堪持赠君

后一节第一行  
后一节第二行
```

如果懒得数空格，也可以直接写 `<br>` 在每行末尾：

```
山中何所有<br>
岭上多白云<br>
```

CSS 上 `.poem-body` 用 `white-space: normal` + 标准段落，所以**节的视觉间距**取决于段落 margin，约定一致即可。
