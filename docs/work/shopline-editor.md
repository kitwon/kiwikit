---
tags: sl-admin le-editor
---

# Shopline theme editor core

## Lifecycle

* 根据`themeId`初始化[主题数据](data-object.md#theme-object)
* 数据写入`redux`
* [渲染组件](##渲染组件)
* [加载主题iframe](##初始化iframe)

## 初始化iframe

* 获取商店域名
* 初始化iframe，插入dom 
* 监听iframe发送的消息

## 渲染组件

核心组件

* `src/feature/Design` - 显示 **页面配置项排序列表** ([[data-object###ThemeUsableSection]])
* `src/feature/Comp` - 添加页面组件
* `src/components/SchemaForm` - 添加页面组件
  * `src/components/SchemaForm/SchemaFormItem` - `section配置信息`
  * `src/components/BlockContainer` - `section block配置信息`