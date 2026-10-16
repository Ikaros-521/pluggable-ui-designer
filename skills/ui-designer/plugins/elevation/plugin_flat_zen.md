---
name: plugin_flat_zen
slot: slot_elevation
version: "1.0.0"
description: "细节点插件：零阴影极简扁平，完全依靠色阶微差与素雅线框分层，提供清爽不花哨的纯粹功能美感"
---

# Flat Zen Elevation Plugin (素雅纯扁平质感)

## 1. 核心视觉哲学
彻底摒弃任何形式的阴影与高光模拟，返璞归真。仅依靠**背景表面的色阶层次阶梯（Surface Steps）**与**极简分割线**来构建清晰的功能区隔，使用户的注意力100%聚焦在数据与操作本身。

## 2. 覆盖设计代币 (Token Overrides)

### 通用规则
* **阴影全清空**：`shadow-none`
* **层次依赖色阶阶梯**：
  - 基础背景：`bg-slate-50` (浅色) / `bg-zinc-950` (深色)
  - 卡片表面：`bg-white` (浅色) / `bg-zinc-900` (深色)
  - 嵌套区块：`bg-slate-100/70` (浅色) / `bg-zinc-800/50` (深色)
* **线框**：`border border-slate-200` (浅色) / `border border-zinc-800` (深色)
* **交互态**：仅进行底色微调，`hover:bg-slate-50` (浅色) / `hover:bg-zinc-800/80` (深色)

## 3. 标准组件实现片段 (Tailwind Class Pattern)

```html
<!-- 扁平素雅卡片 -->
<div class="rounded-lg border border-slate-200 bg-white p-5 shadow-none transition-colors duration-150 hover:border-slate-300">
  <div class="flex items-center justify-between border-b border-slate-100 pb-3">
    <span class="text-xs font-medium text-slate-500 uppercase tracking-wider">节点状态</span>
    <span class="inline-flex items-center rounded bg-emerald-50 px-2 py-0.5 text-xs font-medium text-emerald-700">运行中</span>
  </div>
  <div class="mt-4 text-2xl font-semibold text-slate-900">12 / 12 在线</div>
</div>
```

## 4. 负向约束 (Negative Rules)
* 严禁任何带有 `shadow-*` 的投影类。
* 严禁拟物光晕或反光。
