# 静态 HTML 可直接引入的 CSS

本目录是面向设计素材、静态 HTML、截图稿和非工程化页面的标准语义组件入口。

静态 HTML 设计稿默认还需要同时引入 Tailwind Play CDN，用于补足临时布局、间距、状态和响应式 utility。

## 文件

- `pc-design.css`：PC 设计稿直接引入。
- `mobile-design.css`：移动端设计稿直接引入。

## HTML 引入

PC 页面：

```html
<script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
<link rel="stylesheet" href="./dist/pc-design.css">
```

移动端页面：

```html
<script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
<link rel="stylesheet" href="./dist/mobile-design.css">
```

## 规则

- 静态 HTML 设计稿默认使用 Tailwind Play CDN + 本目录编译 CSS。
- HTML 中优先使用 `.pc-*` 和 `.mobile-*` 语义类。
- 默认语义类无法覆盖时，优先使用 Tailwind utility class，例如 `grid`、`grid-cols-2`、`gap-3`、`mt-4`、`text-right`。
- 不优先新增内联 `<style>` 或临时 CSS 类。
- 不要在静态 HTML 中直接引入 `styles/*.tailwind.css`，那是 Tailwind v4 源文件，需要构建。
- 修改 `styles/*.tailwind.css` 后，需要重新生成本目录的 CSS。
