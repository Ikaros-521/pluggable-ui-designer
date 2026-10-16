---
name: plugin_warm_stone
slot: slot_palette
version: "1.0.0"
description: "细节点插件：温润暖调石系（Warm Stone），摒弃生硬冷冽黑白，营造如 Notion/Substack 般的纸质舒适感与人文亲和力"
---

# Warm Stone Palette Plugin (温润暖石调色板)

## 1. 核心色彩哲学
脱离冰冷刺眼的纯白（`#FFFFFF`）与极夜纯黑（`#000000`），全面引入**暖调天然石色阶（Tailwind Stone 系）**与微暖琥珀色，为长时间注视界面的用户带来如高级纸张般的温润、宁静与专注感。

## 2. 覆盖设计代币 (Token Overrides)

### 浅色模式 (Light - 核心体验)
* **全局背景**：`bg-stone-100` 或 `bg-[#fbfaf8]` (天然纸张米白)
* **卡片表面**：`bg-white` (微暖柔白)
* **高亮次级背景**：`bg-stone-200/70`
* **主文本**：`text-stone-900` (深石墨暖黑，比纯黑更护眼)
* **次级文字**：`text-stone-500`
* **边界描边**：`border-stone-200`
* **品牌焦点强调色**：`bg-stone-900 text-white hover:bg-stone-800`，辅以琥珀暖金点缀 `text-amber-700 bg-amber-50`

### 暗色模式 (Warm Dark)
* **全局背景**：`bg-stone-950` (炭石暖黑)
* **卡片表面**：`bg-stone-900`
* **主文本**：`text-stone-100`
* **边界描边**：`border-stone-800`

## 3. 标准组件实现片段 (Tailwind Class Pattern)

```html
<!-- 暖石色系卡片示例 -->
<div class="rounded-xl border border-stone-200 bg-white p-6 shadow-sm">
  <div class="flex items-center justify-between">
    <span class="text-xs font-medium uppercase tracking-wider text-stone-500">知识库同步</span>
    <span class="rounded-full bg-amber-100 px-2.5 py-0.5 text-xs font-semibold text-amber-800">已整理</span>
  </div>
  <h4 class="mt-3 text-lg font-semibold text-stone-900">工程架构设计笔记 2026</h4>
  <p class="mt-1 text-sm text-stone-600 leading-relaxed">包含微内核设计、槽位契约定义与端到端实操经验沉淀。</p>
</div>
```

## 4. 负向约束 (Negative Rules)
* 严禁使用发蓝、发紫的冷灰底色（如 `slate`、`zinc`、`gray`）。
* 严禁高饱和霓虹荧光色。
