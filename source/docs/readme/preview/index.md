---
title: 本地预览
description:
type: docs
author_info: 由 negoces 编写
last_updated: 2021-12-05
---

<style>strong{color:red;}</style>

{% note warning 注意 %}
本文档并不会讲述 Node.JS 如何安装如何使用，请自行学习。

如果依赖下载过慢可以尝试设置镜像：`npm config set registry https://repo.nju.edu.cn/repository/npm/`
{% endnote %}

1. 在项目文件夹执行 `npm install` 下载并补全依赖。
2. 使用 `npm run server` 启动预览服务。
3. 前往 <http://localhost:4000/> 查看新增文章有无渲染错误。

**注意事项：**

1. 创建、修改、删除文章不需要重启预览服务即可生效。
2. 对于目录 `_config.doku.yml` 文件的修改需要重启预览服务才能生效。
3. 使用 `Crtl` + `C` 键可以停止预览服务。
