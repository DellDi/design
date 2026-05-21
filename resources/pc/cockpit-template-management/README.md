# 驾驶舱模板管理设计资源

本目录存放 PC 端驾驶舱 BI 模板管理改造的静态原型和说明文档。

## 文件说明

- `album-ui.html`：主页面原型，包含分类树、专辑列表、模板列表、分页和模板卡片状态。
- `dialogs.html`：弹窗原型，包含模板编辑、批量操作、复制到当前页面、分类树节点编辑、批量选择状态等弹窗。
- `model-notes.md`：数据模型和交互规则说明，包含分类树表、专辑表、模板表、标签体系和删除校验规则。

## 打开方式

可直接用浏览器打开：

```text
resources/pc/cockpit-template-management/album-ui.html
resources/pc/cockpit-template-management/dialogs.html
```

## 设计口径

- 左侧展示分类树表数据。
- 分类节点下展示专辑表数据。
- 点击专辑后二级下钻进入模板表列表。
- 模板状态仅区分已被引用、未被引用。
- 被引用或内置模板禁止删除。
- 说明性内容放在 `model-notes.md`，不放在主页面右侧。
