---
title: 提交规范
description: 无规矩不成方圆
type: docs
author_info: 由 negoces 编写
last_updated: 2021-11-24
---

## 文章路径规范

### 对于无子章节的文章

一篇文档以目录单位，Markdown 文件以 `index.md` 命名，如这篇文章为：

- `source/docs/readme/commit_spec/index.md`

如有添加图片的需求，请放在与 `index.md` 同级目录或子级目录。如：

- `source/docs/readme/commit_spec/1.png`
- `source/docs/readme/commit_spec/img/tree.png`

### 对于有子章节的文章

将子章节以目录为单位放在父章节目录下，如我有以下章节：

- 2 GPIO 的使用
- 2.1 使用 GPIO 点亮 LED
- 2.2 使用 GPIO 使 LED 闪烁

则按下列结构创建目录：

```bash
source
├── docs
│   ├── ...
│   └── stm32
│       ├── GPIO
│       │   ├── blink
│       │   │   ├── blink.png
│       │   │   └── index.md
│       │   ├── index.md
│       │   └── led
│       │       └── index.md
│       └── ...
├── ...
└── index.md
```

{% note warning %}
很遗憾，本文档的主题不支持以下目录排版模式：

- 2 GPIO 的使用
  + 2.1 使用 GPIO 点亮 LED
  + 2.2 使用 GPIO 使 LED 闪烁

但是你可以使用这种格式进行排版：

- 2 GPIO 的使用
- 2.1 使用 GPIO 点亮 LED
- 2.2 使用 GPIO 使 LED 闪烁

具体写法如下：
```yaml
items:
  - STM32:
    - 1.开发环境搭建 | docs/stm32/setup_devenv/
    - 2.GPIO使用 | docs/stm32/GPIO/
    - 2.1.使用 GPIO 点亮 LED | docs/stm32/GPIO/led/
    - 2.2.使用 GPIO 使 LED 闪烁 | docs/stm32/GPIO/blink/
```
{% endnote %}

## Git 提交(commit)规范

本文档的 Git 提交格式：

```bash
<操作>(<文章>): 修改摘要
具体信息
```

比如创建本篇文章时的提交信息是：

```bash
添加(readme/commit_spec): 新增提交规范文章
添加了提交规范文章以统一目录格式及提交格式
```

{% note warning 关于提交频率%}
**在本地预览时并不是提交才能生效，相反，你最好在本地预览确认无误后在进行提交操作。**

提交频率不要过于频繁或过少，以文章为单位，对一文章修改并验证完成后再进行提交，不要一次性提交多篇文章的修改或连续对一篇文章的修改进行多次提交，这样便于对文章修改历史记录的查找。

提交完后并不需要立即推送(push)，连续的推送可能会导致文档构建平台繁忙，当你编写完文档想去娱乐时，或准备关闭电脑处理其他事务时再进行推送，这样能使文档尽可能为最新版本，又不会导致构建平台繁忙。

**提示：每次push后平台将会自动构建，构建完成后会给最后提交者发送构建结果邮件，推送过于频繁会使你收到“邮件轰炸”**
{% endnote %}
