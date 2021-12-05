---
title: 编写文档
description: 参与修改本文档的详细操作
type: docs
author_info: 由 negoces 编写
last_updated: 2021-12-05
---

<style>strong{color:red;}</style>

增加、修改文档分为修改文章文件和修改目录文件两步：

文章以**目录为单位**存放在 `sources/docs` 文件夹。创建或添加文章时请注意路径规范，要**凸显其分类**，比如：

STM32 的 GPIO 教程分类在(包含图片存放路径)：

- `sources/docs/stm32/GPIO/index.md`
- `sources/docs/stm32/GPIO/1.png`
- `sources/docs/stm32/GPIO/2.png`
- `sources/docs/stm32/GPIO/3.jpg`

**其中 `index.md` 为入口文件，并存放文章，头部需添加下列参数：(`---`需要加上)**

```yml
---
title: 标题
description: 描述
type: docs # 类型
author_info: 由 xxx 编写 # 作者信息(可选)
last_updated: 2021-11-19 # 最后编辑日期(可选)
---
## 标题（必须从二级开始）

这里写正文

引入图片使用相对路径：![png1](1.png)
```

**文档不会自己生成目录，需要自己添加：**

目录则保存在 `_config.doku.yml` 文件的 `sidebar.zh-CN.docs.items` 数组内，格式如下：

```yaml
items:
  - STM32:
      - 1.开发环境搭建 | docs/stm32/setup_devenv/
      - 2.GPIO使用 | docs/stm32/GPIO/
  - 其他:
      - 编写文档 | docs/others/writting/
      - 额外语法 | docs/others/shortcut/
```

其中 `|` 符号前的为文章在目录内显示的标题，后面的为文章相对于 `sources` 文件夹的相对路径。

**相对路径最后注意不要遗漏 `/`，否则会导致图片无法加载。**这与 Hexo 的渲染有关，举 `GPIO使用` 这篇文章为例子，Hexo 最终会生成下列文件：

- `/docs/stm32/GPIO/index.html`
- `/docs/stm32/GPIO/1.png`

> 在使用 `docs/stm32/GPIO` 路径时，`/docs/stm32/GPIO/index.html` 被正常加载，但是文章会尝试寻找 `/docs/stm32/1.png` 路径的图片，这显然会导致 404，在使用 `docs/stm32/GPIO/` 路径时，文章会尝试寻找 `/docs/stm32/GPIO/1.png` 路径的图片，图片被正常加载。

---

**对于有子章节的文章：**

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

很遗憾，本文档的主题不支持以下目录排版模式：

- 2 GPIO 的使用
  - 2.1 使用 GPIO 点亮 LED
  - 2.2 使用 GPIO 使 LED 闪烁

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
