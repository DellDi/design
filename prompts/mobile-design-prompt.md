# 移动端设计规范提示词模板

你正在为企业级物业移动端业务系统生成页面、组件或设计方案。必须遵守本项目 `MOBILE_DESIGN.md` 中的移动端设计规范。

## 必须遵守

- 移动端服务于一线业务操作和管理看板，不做普通消费 App 风格。
- 视觉基调为蓝白浅色、卡片化、轻圆角、高可读、业务优先。
- 页面结构优先保证快速进入业务、快速扫读列表、快速处理工单。
- 移动驾驶舱优先展示关键指标、趋势、排名和对比，不把 PC 图表直接缩小搬运。
- 底部主操作可以固定，但不能遮挡核心内容。
- 底部中央 AI 入口可以突出，但不能干扰业务主流程。
- 避免过度营销风、玻璃拟态、复杂拟物、大面积渐变和多彩图标堆叠。
- 默认产出静态 HTML 设计稿，同时引入 Tailwind Play CDN 和 `dist/mobile-design.css` 编译 CSS。
- 若 HTML 位于 `resources/mobile/<business-domain>/`，使用 `<link rel="stylesheet" href="../../../dist/mobile-design.css">`。
- 生成 HTML 或原型时，优先使用 `.mobile-page`、`.mobile-card`、`.mobile-list-card`、`.mobile-bottom-action`、`.mobile-ai-entry` 等语义类。
- 默认语义类无法覆盖时，优先使用 Tailwind utility class 补足间距、栅格、显示隐藏、对齐、响应式和状态，不优先新增页面内 `<style>`。
- 具体业务设计稿应放入 `resources/mobile/<business-domain>/`，不要直接放在项目根目录。

## 输出要求

- 先说明页面所属场景：业务首页、业务列表、工单详情、工作台、移动驾驶舱或图表明细。
- 若生成文件，先确定业务域目录，例如 `resources/mobile/work-order/`。
- 再给出页面结构、关键组件、状态表达和主操作位置。
- 明确使用到的移动端 token、卡片层级和底部操作策略。
- 若生成静态 HTML，优先按文件位置正确引入 Tailwind Play CDN 和 `dist/mobile-design.css`，并使用已有语义类；确需自定义样式时，优先使用 Tailwind utility class，再考虑 `tokens/mobile-design.tokens.css` 中的变量。
- 只有在明确要求工程化项目时，才直接使用 `styles/mobile-design.tailwind.css` 作为 Tailwind v4 源文件。
- 若需求与移动端规范冲突，先指出冲突，再给出符合规范的替代方案。

## 业务需求

在这里补充具体页面、组件或场景需求。
