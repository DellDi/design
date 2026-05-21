# PC 设计规范提示词模板

你正在为一个企业级 PC 业务系统生成页面、组件或设计方案。必须遵守本项目 `DESIGN.md` 中的设计规范。

## 必须遵守

- 使用企业级后台系统语言，优先保证稳定、清晰、高效和一致。
- 默认采用 Element UI 二次封装体系的组件习惯。
- 常规后台页面使用浅色、规整、中高信息密度布局。
- 门户首页允许轻内容化和轻品牌感，但不能变成营销页。
- 模板管理和资源管理优先卡片陈列、缩略图和批量操作。
- 亮色看板使用指标卡、图表和表格联动。
- 深色大屏使用独立视觉域，不直接套用后台浅色 token。
- 主操作只能有一个，使用主蓝色；危险操作必须可识别并带确认。
- 不自创陌生交互，不使用过度装饰，不牺牲业务可读性。
- 默认产出静态 HTML 设计稿，优先引入 `dist/pc-design.css` 编译 CSS。
- 若 HTML 位于 `resources/pc/<business-domain>/`，使用 `<link rel="stylesheet" href="../../../dist/pc-design.css">`。
- 生成 HTML 或原型时，优先使用 `.pc-page`、`.pc-card`、`.pc-filter-bar`、`.pc-table-shell`、`.pc-btn-primary` 等语义类。
- Tailwind utility 只用于少量间距、栅格、显示隐藏等局部微调，不用长串 utility 重写标准卡片、按钮、表格和主布局。
- 具体业务设计稿应放入 `resources/pc/<business-domain>/`，不要直接放在项目根目录。

## 输出要求

- 先给出页面结构，再给出关键组件与状态。
- 若生成文件，先确定业务域目录，例如 `resources/pc/cockpit-template-management/`。
- 明确使用到的 token、颜色、布局密度和操作分级。
- 若生成静态 HTML，优先按文件位置正确引入 `dist/pc-design.css` 并使用已有语义类；确需自定义样式时，再使用 `tokens/pc-design.tokens.css` 中的变量。
- 只有在明确要求工程化项目时，才直接使用 `styles/pc-design.tailwind.css` 作为 Tailwind v4 源文件。
- 若需求与规范冲突，先指出冲突，再给出符合规范的替代方案。

## 业务需求

在这里补充具体页面、组件或场景需求。
