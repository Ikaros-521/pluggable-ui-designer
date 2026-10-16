---
name: plugin_bento_grid
slot: slot_layout
version: "1.0.0"
description: "细节点插件：Bento 便签错落智能网格，通过不同跨度（col-span/row-span）的卡片编排，打破平铺直叙，构建极具节奏感的信息布局"
---

# Bento Grid Layout Plugin (Bento 错落智能网格)

## 1. 核心布局哲学
借鉴日本便当盒（Bento Box）的紧凑分区智慧，通过现代 CSS Grid 的多跨度特性（`col-span-1`、`col-span-2`、`row-span-2` 等），让核心亮点具备视觉统治力，次要指标紧凑分布，打破千篇一律的等宽方块列表。

## 2. 覆盖布局规则 (Layout Rules)

* **容器基准**：`grid grid-cols-1 md:grid-cols-3 lg:grid-cols-4 gap-4 md:gap-5`
* **主角卡片 (Hero Card)**：占据 `md:col-span-2 md:row-span-2`，容纳主要趋势图表或核心操作流。
* **高频次要指标 (Stat Metric)**：占据 `col-span-1 row-span-1`，容纳单一重要数字与微型趋势箭头。
* **长条通栏条目 (Wide Strip)**：占据 `md:col-span-2`，容纳时间线、最近日志或快捷任务清单。

## 3. 标准布局脚手架 (Tailwind Grid Scaffold)

```html
<div class="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-4 gap-4">
  <!-- 核心大卡片：跨 2 列 2 行 -->
  <div class="md:col-span-2 md:row-span-2 rounded-2xl p-6 flex flex-col justify-between">
    <div>
      <span class="text-xs uppercase font-semibold tracking-wider text-muted">主要看板</span>
      <h3 class="text-xl font-bold mt-1">实时业务吞吐量</h3>
    </div>
    <!-- 图表或主要画布 -->
    <div class="h-48 w-full mt-4 flex items-end gap-2">
      <!-- 动态数据柱状条 -->
    </div>
  </div>

  <!-- 次要指标 1：1x1 -->
  <div class="rounded-2xl p-5 flex flex-col justify-between">
    <span class="text-xs text-muted">成功率</span>
    <div class="text-2xl font-bold font-mono">99.94%</div>
  </div>

  <!-- 次要指标 2：1x1 -->
  <div class="rounded-2xl p-5 flex flex-col justify-between">
    <span class="text-xs text-muted">平均延迟</span>
    <div class="text-2xl font-bold font-mono">14ms</div>
  </div>

  <!-- 横向通栏条目：跨 2 列 -->
  <div class="md:col-span-2 rounded-2xl p-5 flex items-center justify-between">
    <span class="text-sm font-medium">最新服务告警事件</span>
    <span class="text-xs font-mono">3分钟前</span>
  </div>
</div>
```

## 4. 负向约束 (Negative Rules)
* 严禁所有卡片尺寸完全相同（必须有至少 1 个大卡和 2 个小卡的对比节奏）。
* 严禁无响应式降级（在手机屏 `grid-cols-1` 必须顺畅单列流动）。
