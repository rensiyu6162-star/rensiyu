---
name: Feedback - UI layout preferences
description: User's repeated corrections on filter bar layout, iframe nesting, and equal-width filter items
type: feedback
---

筛选项等宽要求：每个筛选项（label + 控件）整体占相同固定宽度，日期范围要合并成一个带边框的容器（两个 date input + 至，共享一个外框），总宽与其他单个筛选项相同。

**Why:** 用户明确说"相当于每个筛选框加上他的隐形外框，他们宽度一样"，并多次纠正直到效果正确。

**How to apply:** 使用固定 px 宽度的 `.fi` class 包裹 label + 控件，日期范围用 `.fi-date` + `.date-range` 合并框，宽度与 `.fi` 一致。

---

iframe 嵌套：预览入口页面（index.html）用 iframe 加载各业务页面时，业务页面本身不能带顶部导航和左侧菜单，否则会出现双层导航嵌套。

**Why:** 用户看到截图中有两层菜单，直接指出"页面有嵌套"。

**How to apply:** 业务 HTML 页面只保留 `<body>` 内容区（标题 + 筛选 + 表格），顶部 header 和 sidebar 统一由 index.html 外壳提供。

---

筛选行布局：筛选项之间要有间距（column-gap: 16px），筛选框要够宽（300px），查询/重置按钮 margin-left:auto 靠右，放不下自动换行到下一行最右，不能硬挤同一行。

**Why:** 用户截图反馈间距太密、按钮挤不下。

**How to apply:** toolbar 用 `flex-wrap:wrap; row-gap:10px; column-gap:16px`，按钮组加 `flex-shrink:0`。
