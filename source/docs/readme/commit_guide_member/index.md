---
title: 如何贡献(普通成员)
description:
type: docs
author_info: 由 negoces 编写
last_updated: 2021-12-05
---

<style>strong{color:red;}</style>

{% note warning 注意 %}
本文档并不会讲述 Git 如何安装如何使用，请自行学习。
{% endnote %}

普通成员不具备仓库修改权限，可通过先 fork 后 Pull Requests 的方式进行贡献：

---

1. 如果你是**第一次参与编辑**：
   1. 前往[仓库地址](https://github.com/negoces/docs)，[fork](https://github.com/login?return_to=/negoces/docs) 一份仓库。
   2. 将仓库克隆(clone)到本地。(**推荐使用 SSH 方式**)
   3. 对克隆下来的项目文件夹进行编辑，可以使用 VS Code 等编辑器打开项目文件夹以获得更好的编辑体验。
   4. 编辑过后进行本地渲染预览，**验证有无渲染错误**。(具体步骤参考本地预览)
   5. **按提交规范**在本地创建提交(commit)。(先暂存(add)后提交(commit)，自行学习)
   6. 推送(push)本地提交到远程。
   7. 前往[仓库地址](https://github.com/negoces/docs)创建[Pull Requests](https://github.com/negoces/docs/compare).(见参考链接 - 创建拉取请求)

**创建 Pull Requests 之前，请从上游仓库拉取最新更改，否则会导致 Pull Requests 被驳回。**

---

2. 如果你是第二次编辑:
   1. 从上游拉取最新更改。(见参考链接 - 同步复刻)
   2. 对项目文件夹进行编辑。
   3. 进行本地渲染预览，验证有无渲染错误。
   4. **按提交规范**在本地创建提交(commit)。
   5. 推送(push)本地提交到远程。
   6. 前往[仓库地址](https://github.com/negoces/docs)创建[Pull Requests](https://github.com/negoces/docs/compare).(见参考链接 - 创建拉取请求)

**创建 Pull Requests 之前，请从上游仓库拉取最新更改，否则会导致 Pull Requests 被驳回。**

---

参考链接：

- [同步复刻](https://docs.github.com/cn/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork)
- [创建拉取请求](https://docs.github.com/cn/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)
