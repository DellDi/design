# Changelog

## 2026-05-21

- 新增 `resources/mobile/quality-cockpit/` 品质模块移动端驾驶舱设计资源，包含主页面、巡检完成详情页、整改闭环详情页和局部样式；页面结构贴近移动驾驶舱参考样式，沉淀可复用指标卡、趋势、环图和排行表组件。
- 新增 PC 端和移动端设计规范、token、Tailwind 落地层及静态 HTML 示例。
- 新增 `resources/` 业务设计资源目录规则。
- 将驾驶舱模板管理相关资源从根目录迁移到 `resources/pc/cockpit-template-management/`。
- 调整静态 HTML 设计稿规则为 Tailwind Play CDN + `dist/` 双入口。
- 明确默认语义类无法覆盖时，优先使用 Tailwind utility class，不优先新增页面内 `<style>`。
- 新增 `resources/pc/cockpit-template-management/README.md`，作为驾驶舱模板管理资源局部索引。

## 2026-05-12

- 初始化标准设计内容库结构。
- 新增项目说明、AI 协作规则、可机读 token 和 AI 页面生成提示词模板。
- 修正 `DESIGN.md` 末尾未关闭的 Markdown 代码块。
- 新增移动端主规范 `MOBILE_DESIGN.md`。
- 新增移动端 token 和移动端 AI 页面生成提示词模板。
