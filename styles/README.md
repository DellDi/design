# Tailwind v4 落地层

本目录用于维护 Tailwind v4 源文件，把 `DESIGN.md` 和 `MOBILE_DESIGN.md` 翻译成可复制、可构建、可约束 AI 输出的样式层。

静态 HTML 设计稿默认不要直接引入本目录文件，应优先使用 Tailwind Play CDN + `dist/` 中的编译 CSS。

## 文件

- `pc-design.tailwind.css`：PC 后台、门户、模板管理、亮色看板的基础样式。
- `mobile-design.tailwind.css`：移动端业务首页、工单、工作台、移动驾驶舱的基础样式。

## 使用方式

在支持 Tailwind v4 的工程化项目中引入对应文件：

```css
@import "./styles/pc-design.tailwind.css";
```

或：

```css
@import "./styles/mobile-design.tailwind.css";
```

## 约束原则

- 生成 HTML 时优先使用语义类，例如 `.pc-card`、`.pc-table-shell`、`.mobile-card`、`.mobile-bottom-action`。
- Tailwind utility 或内置辅助类只用于少量页面级微调，例如 `mt-3`、`grid-cols-2`、`hidden`。
- 不在 HTML 中临时自创颜色、圆角、阴影和主布局密度。
- PC 与移动端样式分开引入，不在同一页面混用。

## 静态 HTML

设计素材、截图稿和非工程化页面请使用：

```html
<script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
<link rel="stylesheet" href="./dist/pc-design.css">
```

或：

```html
<script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
<link rel="stylesheet" href="./dist/mobile-design.css">
```
