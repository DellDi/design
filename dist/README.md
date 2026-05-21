# 静态 HTML 可直接引入的 CSS

本目录是面向设计素材、静态 HTML、截图稿和非工程化页面的默认入口。

## 文件

- `pc-design.css`：PC 设计稿直接引入。
- `mobile-design.css`：移动端设计稿直接引入。

## HTML 引入

PC 页面：

```html
<link rel="stylesheet" href="./dist/pc-design.css">
```

移动端页面：

```html
<link rel="stylesheet" href="./dist/mobile-design.css">
```

## 规则

- 静态 HTML 设计稿优先使用本目录的编译 CSS。
- HTML 中优先使用 `.pc-*` 和 `.mobile-*` 语义类。
- 只使用已编译进本目录 CSS 的少量辅助类，例如 `.mt-3`、`.grid-cols-2`、`.hidden`。
- 不要在静态 HTML 中直接引入 `styles/*.tailwind.css`，那是 Tailwind v4 源文件，需要构建。
- 修改 `styles/*.tailwind.css` 后，需要重新生成本目录的 CSS。
