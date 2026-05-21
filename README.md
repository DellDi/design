# 标准设计内容库

本项目用于沉淀企业级业务系统的标准设计内容，核心规范包括 PC 端 [DESIGN.md](./DESIGN.md) 和移动端 [MOBILE_DESIGN.md](./MOBILE_DESIGN.md)。

## 定位

- 面向 PC 后台管理、门户首页、驾驶舱模板、数据看板、大屏，以及移动端业务首页、工单、工作台、移动驾驶舱场景
- 作为设计、前端、AI 生成、低代码平台和代码生成器的统一约束来源
- 优先保证系统一致性、业务可用性和组件体系稳定

## 目录

```text
.
├── DESIGN.md
├── MOBILE_DESIGN.md
├── README.md
├── AGENTS.md
├── CHANGELOG.md
├── tokens
│   ├── mobile-design.tokens.json
│   ├── mobile-design.tokens.css
│   ├── pc-design.tokens.json
│   └── pc-design.tokens.css
├── dist
│   ├── README.md
│   ├── mobile-design.css
│   └── pc-design.css
├── styles
│   ├── README.md
│   ├── mobile-design.tailwind.css
│   └── pc-design.tailwind.css
├── examples
│   ├── mobile-static-html-template.html
│   └── pc-static-html-template.html
├── resources
│   ├── README.md
│   └── pc
│       └── cockpit-template-management
│           ├── README.md
│           ├── album-ui.html
│           ├── dialogs.html
│           └── model-notes.md
└── prompts
    ├── mobile-design-prompt.md
    └── pc-design-prompt.md
```

## 使用方式

1. PC 端设计评审时，以 `DESIGN.md` 作为视觉和交互判断依据。
2. 移动端设计评审时，以 `MOBILE_DESIGN.md` 作为视觉和交互判断依据。
3. 前端实现时，可从 `tokens/` 读取颜色、背景、边框和文字变量。
4. 使用 AI 生成 PC 页面时，先引用 `prompts/pc-design-prompt.md`，再补充具体业务需求。
5. 使用 AI 生成移动端页面时，先引用 `prompts/mobile-design-prompt.md`，再补充具体业务需求。
6. 生成静态 HTML 或设计素材时，优先引入 `dist/` 中的编译 CSS，并使用语义类控制视觉一致性。
7. 工程化项目需要二次构建时，再引入 `styles/` 中的 Tailwind v4 源文件。
8. 可从 `examples/` 复制最小 HTML 模板开始设计。
9. 具体业务设计资源放入 `resources/<端类型>/<业务域>/`，不要直接放在项目根目录。
10. 规范变更需要同步更新 `CHANGELOG.md`，并尽量保持 token、样式和正文一致。

## 维护原则

- `DESIGN.md` 是 PC 主规范，`MOBILE_DESIGN.md` 是移动端主规范，其他文件是辅助落地材料。
- 根目录只放规范、索引和全局配置；业务设计素材必须放入 `resources/`。
- `examples/` 只放通用最小模板，不放具体业务页面。
- 新增内容先判断是否适用于长期复用，避免把一次性页面需求写入标准。
- token 命名保持稳定，必要变更需要说明兼容影响。
- `dist/` 是静态 HTML 设计稿默认入口，`styles/` 是 Tailwind v4 源文件入口。
- Tailwind 样式层服务于规范落地，不替代 `DESIGN.md` 和 `MOBILE_DESIGN.md`。
- 生成 HTML 时优先使用 `dist/` 中编译出的语义类，Tailwind utility 只做少量局部微调。
- 大屏视觉与常规后台视觉分域管理，不强行合并变量。
- PC 与移动端视觉分域管理，不互相套用页面结构和组件密度。
