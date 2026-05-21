# AGENTS.md

## 语言

始终使用中文回复。

## 项目定位

这是一个标准设计内容库，不是业务应用工程。`DESIGN.md` 是 PC 主规范，`MOBILE_DESIGN.md` 是移动端主规范，其他文件用于索引、落地、机器读取或 AI 使用。

## 工作规则

- 修改 PC 设计规范前，先阅读 `DESIGN.md`，保持新增内容与既有企业级后台风格一致。
- 修改移动端设计规范前，先阅读 `MOBILE_DESIGN.md`，保持新增内容与既有物业移动端业务风格一致。
- 不引入营销站、活动页或强品牌视觉规则，除非用户明确要求扩展范围。
- 不为了视觉创新破坏后台管理页、门户首页、模板管理、看板和大屏之间的风格分层。
- 不把 PC 表格、PC 看板或 PC 弹窗结构直接缩小搬到移动端。
- 维护 PC token 时，同时检查 `tokens/pc-design.tokens.json` 和 `tokens/pc-design.tokens.css` 是否需要同步。
- 维护移动端 token 时，同时检查 `tokens/mobile-design.tokens.json` 和 `tokens/mobile-design.tokens.css` 是否需要同步。
- 维护 Tailwind 落地层时，同时检查 `styles/pc-design.tailwind.css`、`styles/mobile-design.tailwind.css` 和 `styles/README.md` 是否需要同步。
- 维护 Tailwind 源文件后，需要同步重新生成 `dist/pc-design.css` 或 `dist/mobile-design.css`。
- 大部分产物优先做静态 HTML 设计稿，默认通过 `<link>` 引入 `dist/pc-design.css` 或 `dist/mobile-design.css`。
- 业务资源目录下的 HTML 通常位于 `resources/<端类型>/<业务域>/`，引入根目录 `dist/` 时要使用正确相对路径，例如 `../../../dist/pc-design.css`。
- 生成 HTML 或原型时，优先使用 `dist/` 编译 CSS 中已有的语义类，Tailwind utility 只用于少量局部微调。
- 不在 HTML 中临时自创颜色、圆角、阴影和主布局密度。
- 变更标准、token、Tailwind 样式、编译 CSS 或提示词模板后，更新 `CHANGELOG.md`。
- 不把项目初始化为前端应用，除非用户明确要求创建可运行示例或组件库。

## 资源目录规则

- 根目录只保留规范、索引和全局配置文件，例如 `README.md`、`DESIGN.md`、`MOBILE_DESIGN.md`、`AGENTS.md`、`CHANGELOG.md`。
- 通用最小模板放入 `examples/`。
- 具体业务设计资源必须放入 `resources/<端类型>/<业务域>/`。
- 端类型优先使用 `pc`、`mobile`、`screen`。
- 业务域目录使用小写英文和连字符，例如 `cockpit-template-management`。
- 不要把业务 HTML、页面 notes、模型说明、截图说明直接放在项目根目录。
