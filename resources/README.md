# 设计资源目录

本目录用于存放具体业务语义下的设计素材、静态 HTML、交互稿、模型说明和页面 notes。

## 目录规则

```text
resources/
├── pc/
│   └── <business-domain>/
├── mobile/
│   └── <business-domain>/
└── screen/
    └── <business-domain>/
```

## 命名规则

- 一级目录按终端或视觉域划分：`pc`、`mobile`、`screen`。
- 二级目录按业务语义命名，使用小写英文和连字符，例如 `cockpit-template-management`。
- 目录内文件按页面或内容类型命名，例如 `album-ui.html`、`dialogs.html`、`model-notes.md`。
- 通用最小模板放在 `examples/`，具体业务设计资源放在 `resources/`。
- 根目录只保留规范、索引和全局配置文件，不直接放业务设计资源。

## 当前资源

- `pc/cockpit-template-management/`：驾驶舱模板管理相关设计资源。

## 静态 HTML 样式引用

业务资源通常位于 `resources/<端类型>/<业务域>/`，静态 HTML 引入根目录 `dist/` 时需要使用相对路径。

PC 业务资源示例：

```html
<link rel="stylesheet" href="../../../dist/pc-design.css">
```

移动端业务资源示例：

```html
<link rel="stylesheet" href="../../../dist/mobile-design.css">
```
