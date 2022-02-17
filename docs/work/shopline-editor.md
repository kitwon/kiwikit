---
tags: sl-admin le-editor
---

# Shopline theme editor core

## Lifecycle

* 根据`themeId`初始化[主题数据](data-object.md#theme-object)
* 数据写入`redux`
* 渲染组件

## 初始化iframe

* 获取商店域名
* 初始化iframe，插入dom
* 监听iframe发送的消息