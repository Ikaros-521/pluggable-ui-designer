# Pluggable UI Designer

> **Next-generation AI Agent Frontend UI & Prototype Design Skill built upon the "Universal Aesthetic Core + Composable Slot Mixins" architecture.**

[![Spec v1.0 Compliant](https://img.shields.io/badge/Spec-v1.0-blue.svg)](https://github.com/Ikaros-521/pluggable-skills)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Zero-Config HTML](https://img.shields.io/badge/Delivery-Single--File%20HTML-orange.svg)]()

[中文文档 (README.md)](README.md) | [Specification Core Repo (pluggable-skills)](https://github.com/Ikaros-521/pluggable-skills)

---

## 💡 Why Pluggable UI Designer?

### The Problems with Traditional AI-Generated UI
1. **Pervasive "AI Slop" Aesthetic Fatigue**: Predictable purple-to-indigo gradients, generic white cards with blurry black drop shadows, and oversized bubbly rounded containers.
2. **Monolithic & Brittle System Prompts**: Adjusting a single detail (e.g., swapping elevation shadows for hairline borders or converting layouts to a Bento Grid) often causes the AI to rewrite the entire interface and break layout hierarchy.

### Our Solution: Composable Slot Mixins
Modern LLMs already possess strong foundational aesthetic capabilities. This skill decouples the **Base Aesthetic Core** from **Detail-Level Slot Mixins**:
* **Base Aesthetic Engine**: Enforces strict modern UI standards (micro-typography scaling, WCAG AA contrast, mobile-first responsive flex/grid layouts).
* **4 Composable Slots**: Elevation, layout archetype, color palette, and micro-interactions are isolated into lightweight, single-file Markdown plugins. Users can hot-swap specific details with a single sentence!

---

## 🧩 Plugins Matrix

| Slot Category | Plugin | Aesthetic Highlights |
| :--- | :--- | :--- |
| **Elevation & Texture**<br>`slot_elevation` | **`plugin_fine_hairline.md`** | **Precision Hairline**: 1px subtle borders + top specular inset highlight. Linear / Raycast precision. |
| | **`plugin_soft_diffusion.md`** | **Soft Diffusion**: Dual-layer multi-blur ambient shadows for an Apple / Stripe floating aesthetic. |
| | **`plugin_flat_zen.md`** | **Flat Zen**: Zero shadows. Relies purely on background surface steps and neat dividers. |
| **Layout Archetype**<br>`slot_layout` | **`plugin_bento_grid.md`** | **Bento Grid**: Asymmetric hero cards (2x2) and compact 1x1 stat cards for rhythmic data presentation. |
| | **`plugin_sidebar_dock.md`** | **Sidebar Dock**: Icon-first floating dock + expansive canvas for pro desktop productivity. |
| **Color Palette**<br>`slot_palette` | **`plugin_warm_stone.md`** | **Warm Stone**: Warm stone neutral scale + paper off-white for a comfortable Notion/Substack reading feel. |
| | **`plugin_cold_slate.md`** | **Cold Slate**: High-contrast slate neutrals with electric blue accents for enterprise SaaS consoles. |
| **Micro-Interactions**<br>`slot_interaction` | **`plugin_tactile_bounce.md`** | **Tactile Bounce**: Hover lift (`-translate-y-0.5`) + physical press feedback (`active:scale-[0.97]`). |
| | **`plugin_subtle_glow.md`** | **Subtle Glow**: Gentle breathing beacon pulses (`animate-ping`) and focus glow halos. |

---

## 🎨 Progressive Evolution Examples

Using the same **AI Agent Orchestrator Dashboard** scenario, 3 self-contained, zero-dependency HTML files are provided in [`examples/`](examples/):

1. **Base Prototype: Universal Modern Aesthetic** ([`examples/01_default_base.html`](examples/01_default_base.html))
   * Default base aesthetic without plugin overrides.
2. **Detail Swap 1: Hairline Borders + Warm Stone Palette** ([`examples/02_fine_hairline_warm_stone.html`](examples/02_fine_hairline_warm_stone.html))
   * Business metrics and structure remain 100% intact; only texture and color palette are hot-swapped.
3. **Detail Swap 2: Bento Grid + Tactile Bounce Interaction** ([`examples/03_bento_grid_tactile_bounce.html`](examples/03_bento_grid_tactile_bounce.html))
   * Layout morphs into a rhythmic Bento Grid with springy tactile press effects and status breathing pulses.

---

## 🚀 Natural Language Agent Interaction

* **Default Brief**: *"Design a Kubernetes container cluster monitoring dashboard."* $\to$ Renders using the modern base aesthetic engine.
* **Single-Slot Swap**: *"Keep everything the same, but change the shadows to fine hairline borders and use a warm stone color palette."* $\to$ Hot-swaps `plugin_fine_hairline` + `plugin_warm_stone`.
* **Layout & Interaction Mixin**: *"Rearrange the cards into a Bento Grid with tactile click feedback."* $\to$ Mounts `plugin_bento_grid` + `plugin_tactile_bounce`.

---

## 📄 License

Distributed under the [MIT License](LICENSE).
