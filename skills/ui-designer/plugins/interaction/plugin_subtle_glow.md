---
name: plugin_subtle_glow
slot: slot_interaction
version: "1.0.0"
description: "细节点插件：呼吸微发光与焦点光晕（Subtle Glow），打造动态呼吸状态指示与沉浸式发光聚焦"
---

# Subtle Glow Interaction Plugin (呼吸微发光与光晕插件)

## 1. 核心交互哲学
在信息关键节点（如服务器健康态、实时在线指示灯、输入框聚焦）注入极其克制的**平缓呼吸光晕（Breathing Pulse）**与**发光边界（Glow Halo）**，使界面具备敏锐的环境感知度与沉浸感。

## 2. 覆盖设计代币 (Token Overrides)

* **实时状态呼吸灯 (Status Beacon)**：
  - 外圈脉冲光环：`relative flex h-2.5 w-2.5` 配合子元素 `<span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-emerald-400 opacity-75"></span>`
* **焦点发光环 (Focus Ring)**：
  - 聚焦光晕：`focus:outline-none focus:ring-2 focus:ring-emerald-500/30 focus:border-emerald-500`
* **卡片边缘微弱聚光 (Edge Glow Hover)**：
  - 类名：`transition-shadow duration-300 hover:shadow-[0_0_25px_rgba(16,185,129,0.15)]`

## 3. 标准组件实现片段 (Tailwind Class Pattern)

```html
<!-- 具备呼吸光晕的实时状态条目 -->
<div class="flex items-center gap-2 rounded-lg border border-zinc-800 bg-zinc-900/60 px-3 py-1.5 transition-all duration-300 hover:shadow-[0_0_20px_rgba(16,185,129,0.12)]">
  <span class="relative flex h-2 w-2">
    <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-emerald-400 opacity-75"></span>
    <span class="relative inline-flex rounded-full h-2 w-2 bg-emerald-500"></span>
  </span>
  <span class="text-xs font-medium text-zinc-300">集群节点实时同步中</span>
</div>
```

## 4. 负向约束 (Negative Rules)
* 严禁刺眼的超高亮霓虹光（阴影透明度严禁超过 0.25）。
* 严禁呼吸频率过快（避免使用容易引发视觉疲劳的急促闪烁）。
