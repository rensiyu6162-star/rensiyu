---
name: Project - 百战营销平台计费对账新增模块
description: Three new billing reconciliation pages being built for 百战营销平台
type: project
---

正在为百战营销平台（计费对账）新增三个页面，交付形式为纯 HTML 静态文件。

- 供应商账单（supplier_bill.html）
- 数据费减免（data_fee_discount.html）
- PO单商品拆解（po_split.html）
- 预览入口（index.html）：左侧菜单切换三个页面，业务页面通过 iframe 嵌入，不带自己的导航。

**Why:** 原网站为内网地址无法外部访问，用户需要 HTML 原型交付供评审/演示，PRD 来自 `PRD设计逻辑说明文档.md`。

**How to apply:** 始终交付可直接双击打开的 HTML 文件，不需要服务器。UI 规范对齐截图中的 百战营销平台 现有风格（白色顶导、白色左侧菜单、蓝色主色调）。
