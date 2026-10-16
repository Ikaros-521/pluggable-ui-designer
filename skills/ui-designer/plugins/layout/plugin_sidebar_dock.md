---
name: plugin_sidebar_dock
slot: slot_layout
version: "1.0.0"
description: "细节点插件：悬浮侧边 Dock 导航栏 + 自适应主工作区画布，兼顾桌面端宽屏沉浸感与紧凑操作路径"
---

# Sidebar Dock Layout Plugin (悬浮侧边 Dock 布局)

## 1. 核心布局哲学
脱离死板顶栏与笨重抽屉，在页面左侧常驻一个悬浮精致的**图标 Dock 导航栏（Icon-first Floating Dock）**，将 90% 以上的可视区域留给主工作区画布，极具生产力与现代专业软件（IDE/Figma 式）的沉浸感。

## 2. 覆盖布局规则 (Layout Rules)

* **外层容器**：`flex min-h-screen w-full flex-col md:flex-row p-3 md:p-5 gap-4`
* **悬浮侧边 Dock**：
  - 桌面端：`w-16 md:w-20 shrink-0 flex flex-col items-center justify-between py-6 rounded-2xl`
  - 移动端：自动吸附在底部变为 Bottom Navigation Bar（`fixed bottom-3 left-3 right-3 flex-row`）
* **主工作区画布 (Main Canvas)**：`flex-1 rounded-2xl p-6 md:p-8 overflow-y-auto`

## 3. 标准布局脚手架 (Tailwind Layout Scaffold)

```html
<div class="flex min-h-screen w-full bg-slate-950 p-3 md:p-5 gap-4">
  <!-- 侧边悬浮 Dock 栏 -->
  <aside class="w-16 md:w-20 shrink-0 flex flex-col items-center justify-between py-6 rounded-2xl border border-white/10 bg-zinc-900/80">
    <div class="flex flex-col items-center gap-6">
      <!-- Logo 标识 -->
      <div class="h-10 w-10 rounded-xl bg-indigo-600 flex items-center justify-center font-bold text-white">
        A
      </div>
      <!-- 快捷图标导航 -->
      <nav class="flex flex-col items-center gap-3">
        <button class="p-3 rounded-xl text-white bg-white/10 hover:bg-white/15 transition-colors">
          <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"/></svg>
        </button>
      </nav>
    </div>
    <!-- 底部设置/头像 -->
    <div class="h-9 w-9 rounded-full bg-zinc-800 border border-white/20"></div>
  </aside>

  <!-- 主工作区内容画布 -->
  <main class="flex-1 rounded-2xl border border-white/10 bg-zinc-900/50 p-6 md:p-8">
    <!-- 主界面内容 -->
  </main>
</div>
```

## 4. 负向约束 (Negative Rules)
* 严禁传统遮挡半屏的固定大宽度侧边栏。
