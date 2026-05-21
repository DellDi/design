# 品质移动驾驶舱设计资源

本目录用于沉淀品质模块移动端驾驶舱静态设计稿，基于品质综合巡检指标体系组织页面。

## 页面清单

- `index.html`：品质驾驶舱主页面，展示综合巡检总览、核心指标、指标板块和项目排名。
- `completion-detail.html`：巡检完成情况详情页，展开任务数、完成数、完成率及未完成跟进。
- `rectification-detail.html`：整改闭环情况详情页，展开整改完成、待整改、复核质量和整改合格率。
- `profile.html`：我的页面，承载账号信息、常用能力和权限信息。
- `quality-cockpit.css`：该业务资源的局部样式，仅服务本目录静态设计稿。

## 指标口径

- 巡检完成情况：综合巡检任务数、综合巡检完成数、综合巡检完成率。
- 完成质量情况：综合巡检合格数、综合巡检不合格数、综合巡检合格率。
- 整改闭环情况：综合巡检整改完成数、综合巡检待整改数、综合巡检整改完成率、综合巡检整改合格数、综合巡检整改不合格数、综合巡检整改合格率。

## 使用说明

静态 HTML 默认引入 Tailwind Play CDN 和 `../../../dist/mobile-design.css`。

优先使用移动端标准语义类。`quality-cockpit.css` 仅用于沉淀本业务目录内反复使用、且标准语义类无法经济表达的专属头图、指标卡、图表和排行样式。

## 可复用组件

- 顶部组织头图：`top-hero`、`hero-company`、`hero-filter`。
- 月度汇总卡：`work-summary`、`summary-main-value`、`summary-badges`。
- 指标信息板块：`card-section`、`info-grid`、`spotlight`、`mini-stat`。
- 详情指标宫格：`detail-grid`、`metric-card`、`metric-card wide`。
- 图表与排行：`trend-chart`、`donut-wrap`、`rank-table`。
- 底部模块导航：财务、工单为预留模块项，品质、我的为当前可跳转页面。
