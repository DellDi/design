# Changelog

## 2026-05-12

- 初始化标准设计内容库结构。
- 新增项目说明、AI 协作规则、可机读 token 和 AI 页面生成提示词模板。
- 修正 `DESIGN.md` 末尾未关闭的 Markdown 代码块。
- 新增移动端主规范 `MOBILE_DESIGN.md`。
- 新增移动端 token 和移动端 AI 页面生成提示词模板。
- 新增 Tailwind v4 落地层 `styles/pc-design.tailwind.css` 和 `styles/mobile-design.tailwind.css`。
- 更新提示词和协作规则，要求生成 HTML 时优先使用标准语义类，减少长串 utility class。
- 新增 `dist/pc-design.css` 和 `dist/mobile-design.css`，支持静态 HTML 设计稿直接 `<link>` 引入。
- 新增 `examples/` 静态 HTML 最小模板。
- 调整默认工作流为优先产出静态 HTML 设计界面，工程化项目再使用 `styles/*.tailwind.css`。
- 新增 `resources/` 业务设计资源目录规则。
- 将驾驶舱模板管理相关资源从根目录迁移到 `resources/pc/cockpit-template-management/`。

## 2026-05-21

- 新增 PC 端和移动端设计规范、token、Tailwind 落地层及静态 HTML 示例。
- 新增 `resources/` 业务设计资源目录规则。
- 将驾驶舱模板管理相关资源从根目录迁移到 `resources/pc/cockpit-template-management/`。
