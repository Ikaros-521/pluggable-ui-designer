---
name: plugin_soft_diffusion
slot: slot_elevation
version: "1.0.0"
description: "细节点插件：多层超大模糊半径柔和弥散阴影，营造类似 Stripe/Apple 官网的轻盈漂浮感与高级通透感"
---

# Soft Diffusion Elevation Plugin (柔和弥散轻盈质感)

## 1. 核心视觉哲学
通过**大半径、多层次、极低不透明度的环境光弥散（Ambient Diffusion）**，让卡片和操作区域如同悬浮在背景之上的柔光浮岛，给人亲和、优雅、呼吸感充沛的现代视觉享受。

## 2. 覆盖设计代币 (Token Overrides)

### 浅色模式 (Light Theme - 推荐基准)
* **卡片边框**：无边框或极淡环境光环 `border-0`（依靠弥散光区分边界）
* **多层弥散阴影**：`shadow-[0_20px_35px_-10px_rgba(0,0,0,0.06),0_10px_15px_-5px_rgba(0,0,0,0.02)]`
* **悬浮强化阴影**：`hover:shadow-[0_30px_50px_-15px_rgba(0,0,0,0.1),0_15px_20px_-8px_rgba(0,0,0,0.04)]`
* **卡片底色**：`bg-white/95 backdrop-blur-sm`

### 暗色模式 (Dark Theme)
* **卡片边框**：`border border-zinc-800/40`
* **环境微光光晕**：`shadow-[0_20px_40px_-15px_rgba(0,0,0,0.5),0_0_20px_0px_rgba(255,255,255,0.02)]`
* **卡片底色**：`bg-zinc-900/90`

## 3. 标准组件实现片段 (Tailwind Class Pattern)

```html
<!-- 柔和弥散浮岛卡片 -->
<div class="rounded-2xl bg-white p-6 shadow-[0_20px_35px_-10px_rgba(0,0,0,0.06),0_10px_15px_-5px_rgba(0,0,0,0.02)] transition-all duration-300 hover:-translate-y-1 hover:shadow-[0_30px_50px_-15px_rgba(0,0,0,0.1)]">
  <div class="text-sm font-semibold text-slate-900">核心资产概览</div>
  <p class="mt-1 text-xs text-slate-500">自上周以来增长稳健，无异常波动</p>
</div>
```

## 4. 负向约束 (Negative Rules)
* 严禁出现生硬的深色实线边框（如 `border-black`、`border-slate-400`）。
* 严禁无模糊半径的硬边缘阴影。
