---
title: 目录结构
description:
type: docs
author_info: 由 negoces 编写
last_updated: 2021-12-05
---

```bash
docs
├── _config.doku.yml    # 主题设置机目录
├── _config.yml         # 站点设置
├── LICENSE             # 开源协议
├── package.json        # 项目元数据、依赖项
├── README.md           # 项目介绍
├── scaffolds           # 脚手架、模板
├── source              # md 源目录
│   ├── 404.md          # 404 页
│   ├── docs            # 文档
│   │   ├── others      # 其他
│   │   ├── readme      # 必读
│   │   └── stm32       # STM32
│   ├── img             # 全局图片，404页，入口页使用
│   └── index.md        # 入口页
└── themes              # 主题
```

正常编写只需修改下列文件：

- `_config.doku.yml`
- `source/docs/*`
