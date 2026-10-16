---
name: plugin_cold_slate
slot: slot_palette
version: "1.0.0"
description: "细节点插件：冷调工业蓝灰（Cold Slate），搭配高精密深空蓝阶梯，打造专业、严谨的大厂企业级 SaaS 生产力工具氛围"
---

# Cold Slate Palette Plugin (冷调工业蓝灰调色板)

## 1. 核心色彩哲学
采用**冷调工业蓝灰（Tailwind Slate 系）**作为主基调，搭配经典的**精密电光蓝（Electric Blue / Indigo）**作为点睛色，传递理智、高效、绝对稳定的生产力与工程级信赖感。

## 2. 覆盖设计代币 (Token Overrides)

### 暗色模式 (Dark - 极客专业首选)
* **全局背景**：`bg-slate-950`
* **卡片表面**：`bg-slate-900/90`
* **次级容器**：`bg-slate-800/60`
* **主文本**：`text-slate-100`
* **次级文字**：`text-slate-400`
* **边界描边**：`border-slate-800`
* **品牌焦点强调色**：`bg-blue-600 text-white hover:bg-blue-500 shadow-sm shadow-blue-500/20`

### 浅色模式 (Light)
* **全局背景**：`bg-slate-50`
* **卡片表面**：`bg-white`
* **主文本**：`text-slate-900`
* **边界描边**：`border-slate-200`

## 3. 标准组件实现片段 (Tailwind Class Pattern)

```html
<!-- 冷蓝灰控制台状态卡 -->
<div class="rounded-xl border border-slate-800 bg-slate-900/90 p-5">
  <div class="flex items-center justify-between">
    <span class="text-xs font-mono text-slate-400">NODE_US_EAST_01</span>
    <span class="inline-flex items-center gap-1.5 rounded-full bg-blue-500/10 px-2.5 py-0.5 text-xs font-medium text-blue-400">
      <span class="h-1.5 w-1.5 rounded-full bg-blue-400"></span> 活跃
    </span>
  </div>
  <div class="mt-3 flex items-baseline gap-2">
    <span class="text-2xl font-bold font-mono text-white">41.2%</span>
    <span class="text-xs text-slate-400">负载均衡健康度</span>
  </div>
</div>
```

## 4. 负向约束 (Negative Rules)
* 严禁泛黄或发绿的脏色调。
* 严禁低对比度蓝底蓝字。
