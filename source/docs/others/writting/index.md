---
title: 文档额外语法
description: 除 Markdown 标准语法外的其他用法
type: docs
author_info: 由 negoces 编写
last_updated: 2021-11-18
---

## 提示信息

<https://doku.skk.moe/tag-plugins.html>

语法：

```js
{% note [可选参数] %} 插件的内容 {% endnote %}
```

样式列表：

- none(留空)

```js
{% note %} 这是一条普通的提示信息 {% endnote %}
```

{% note %} 这是一条普通的提示信息 {% endnote %}

- dark

```js
{% note dark %} 这是一条普通的提示信息 {% endnote %}
```

{% note dark %} 这是一条普通的提示信息 {% endnote %}

- primary

```js
{% note primary %} 这是一条普通的提示信息 {% endnote %}
```

{% note primary %} 这是一条普通的提示信息 {% endnote %}

- link

```js
{% note link %} 这是一条普通的提示信息 {% endnote %}
```

{% note link %} 这是一条普通的提示信息 {% endnote %}

- info

```js
{% note info %} 这是一条普通的提示信息 {% endnote %}
```

{% note info %} 这是一条普通的提示信息 {% endnote %}

- success

```js
{% note success %} 这是一条可以用来标注推荐内容的提示信息 {% endnote %}
```

{% note success %} 这是一条可以用来标注推荐内容的提示信息 {% endnote %}

- warning

```js
{% note warning %} 这是一条可以用来标注警告内容的提示信息 {% endnote %}
```

{% note warning %} 这是一条可以用来标注警告内容的提示信息 {% endnote %}

- danger

```js
{% note danger %} 这是一条可以用来标注危险内容的提示信息 {% endnote %}
```

{% note danger %} 这是一条可以用来标注危险内容的提示信息 {% endnote %}

- 带标题(默认样式)

```js
{% note '' 你可以忽略这条消息 %} 这是一条普通的提示信息 {% endnote %}
```

{% note ' ' 你可以忽略这条消息 %} 这是一条普通的提示信息 {% endnote %}

- 带标题

```js
{% note warning 你应当注意这条消息 %} 这是一条可以用来标注警告内容的提示信息 {% endnote %}
```

{% note warning 你应当注意这条消息 %} 这是一条可以用来标注警告内容的提示信息 {% endnote %}
