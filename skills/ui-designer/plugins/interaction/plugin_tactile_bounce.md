---
name: plugin_tactile_bounce
slot: slot_interaction
version: "1.0.0"
description: "细节点插件：物理弹性微触感（Tactile Bounce），赋予卡片悬浮浮起与按钮按压微凹陷的真实物理按键手感"
---

# Tactile Bounce Interaction Plugin (物理弹性微触感交互)

## 1. 核心交互哲学
拒绝机械、生硬的颜色瞬间切换。利用精细计算的**位移（Translation）**与**形变缩放（Scale）**微动效，模拟真实世界中微动开关和悬浮机械按键的触感反馈，让界面极具生命力与操控愉悦感。

## 2. 覆盖设计代币 (Token Overrides)

* **可点击卡片悬浮 (Card Hover)**：
  - 类名：`transition-all duration-200 ease-out hover:-translate-y-1 hover:shadow-md cursor-pointer`
* **主操作按钮按压 (Button Press)**：
  - 类名：`transition-transform duration-100 ease-in-out active:scale-[0.97]`
* **列表项目交互态 (List Item)**：
  - 类名：`transition-transform duration-150 hover:translate-x-1`

## 3. 标准组件实现片段 (Tailwind Class Pattern)

```html
<!-- 具备物理触感反馈的交互按钮 -->
<button class="inline-flex items-center justify-center rounded-xl bg-zinc-900 px-4 py-2.5 text-sm font-medium text-white shadow-sm transition-all duration-150 ease-out hover:bg-zinc-800 hover:-translate-y-0.5 hover:shadow-md active:scale-[0.97] active:translate-y-0">
  部署新版本
</button>

<!-- 具备悬浮微浮动的卡片 -->
<div class="rounded-xl border border-zinc-200 bg-white p-5 transition-all duration-200 ease-out hover:-translate-y-1 hover:shadow-lg cursor-pointer">
  <div class="text-sm font-medium text-zinc-900">点击进入详情</div>
</div>
```

## 4. 负向约束 (Negative Rules)
* 严禁大幅度、夸张的晃动（位移严禁超过 `4px`，避免廉价卡通感）。
* 严禁无过渡时长的生硬帧跳变。
