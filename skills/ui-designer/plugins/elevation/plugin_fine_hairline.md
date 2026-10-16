---
name: plugin_fine_hairline
slot: slot_elevation
version: "1.0.0"
description: "细节点插件：极细发丝级单像素线与顶部微高光，去除大面积模糊暗影，营造类似 Linear/Raycast 的精工仪表感"
---

# Fine Hairline Elevation Plugin (精工发丝线质感)

## 1. 核心视觉哲学
摒弃传统大面积模糊投影的笨重感，通过**单像素精密描边（Hairline Border）**与**顶部内发光高光（Inset Highlight）**建立空间落差，传达坚实、精密、现代工业级的质感。

## 2. 覆盖设计代币 (Token Overrides)

### 暗色模式 (Dark Theme - 推荐基准)
* **卡片边框**：`border border-white/10` 或 `border border-zinc-800`
* **质感内阴影 (Inset Specular)**：`shadow-[inset_0_1px_0_0_rgba(255,255,255,0.08)]`
* **卡片表面底色**：`bg-zinc-900/80` (带微妙通透感)
* **悬浮态质感**：`hover:border-white/20 hover:shadow-[inset_0_1px_0_0_rgba(255,255,255,0.15)]`

### 浅色模式 (Light Theme)
* **卡片边框**：`border border-zinc-200/90`
* **质感内阴影**：`shadow-[inset_0_1px_0_0_rgba(255,255,255,1),0_1px_2px_rgba(0,0,0,0.03)]`
* **卡片表面底色**：`bg-white`
* **悬浮态质感**：`hover:border-zinc-300`

## 3. 标准组件实现片段 (Tailwind Class Pattern)

```html
<!-- 精工发丝线卡片结构 -->
<div class="relative rounded-xl border border-white/10 bg-zinc-900/80 p-5 shadow-[inset_0_1px_0_0_rgba(255,255,255,0.08)] transition-all duration-200 hover:border-white/20">
  <div class="text-xs font-medium text-zinc-400">系统指标</div>
  <div class="mt-2 text-2xl font-bold tracking-tight text-white font-mono">99.98%</div>
</div>
```

## 4. 负向约束 (Negative Rules)
* 严禁使用默认沉重的大黑影（如 `shadow-xl`、`shadow-2xl`）。
* 严禁超过 1px 的粗笨边框（避免 `border-2`）。
