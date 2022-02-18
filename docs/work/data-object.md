---
tags: sl-admin
---

# Shopline Data Object

## Theme Object
* ThemeInfo - 主题基础信息
  * route - `GET /editor/theme/:themeId`
* ThemeUsableSection - 主题可用配置块
  * route - `GET /editor/theme/:themeId/sections`
* ThemePages - 主题可配置页面
  * route - `GET /editor/theme/:themeId/pages`
* ThemeSettings - 主题全局配置
  * route - `GET /editor/theme/:themeId/settings`

## Product Object
* Collection - 商品集合
  * route - `GET /api/product/sortation/query/list?sortationType=ALL`

## Merchant Object
* DomainList - 商店域名配置
  * route - `GET /api/merchant/setting/domain`