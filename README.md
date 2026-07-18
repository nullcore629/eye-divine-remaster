# E.Y.E: Divine Cybermancy — Total Remaster Project

An ambitious, multi-disciplinary overhaul project designed to completely re-engineer the visual depth, level design readability, and rendering pipelines of *E.Y.E: Divine Cybermancy* (Source Engine).

## 🎯 The Vision

The retail version of *E.Y.E.* is a masterpiece of cyberpunk atmosphere, but many campaign levels were rushed. They suffer from flat lighting, poorly configured fog, and broken rendering bugs that completely destroy immersion. 

This project aims to deliver a definitive remaster by attacking the game from two fronts simultaneously:
1. **Campaign Map Overhaul:** Completely rebuilding and re-lighting the original campaign maps to maximize visual depth, atmosphere, and environmental storytelling.
2. **Engine & Asset Fixing:** Reverse-engineering the game binaries to patch hardcoded rendering limitations and broken visual shaders.

---

## 🛠️ Project Subsystems & Current Focus

### 1. 🗺️ Campaign Level Overhaul (Active)
I am systematically auditing and rebuilding the original campaign maps. The focus is on fixing the rushed level design by injecting:
* **Advanced Lighting:** Re-baking and fine-tuning lightmaps for realistic cyberpunk contrasts.
* **Atmospheric Fog:** Calibrating fog density and colors to give locations true scale and depth.
* **Prop & Detail Enhancement:** Adding environmental assets to make zones feel alive and visually readable.

*Current Stage:* 🔍 Auditing map files, testing lightmaps, and setting up the Source SDK mapping pipeline. The progress is slow, but precision takes time.

### 2. 🐛 The Bullet Decal Fog Rendering Fix (Active Research)
The most jarring engine bug: bullet impact decals (marks on walls) completely ignore active fog density and color. In heavy fog, they render with full pitch-black contrast, instantly ruining depth perception during firefights.

*Current Stage:* 🔍 Binary Research & String Mapping.
* **Objective:** Locate the decal rendering pipeline inside `client.dll` / `engine.dll` using IDA Pro / Ghidra and force it to multiply decal alpha/color by the active `GetFogFactor()`.

---

## 📊 Roadmap & Execution Log

| Subsystem | Target Task | Status | Output Type |
| :--- | :--- | :--- | :--- |
| **Campaign Maps** | Re-lighting, Fog Calibration, Prop Layouts | ⏳ Slow & Active Development | Updated `.bsp` Maps |
| **Asset Audit** | Fixing `.vmt` shader materials for decals | 🔍 In Progress | Modded VMT Patches |
| **Binary Patching**| Injecting Fog-Decal memory fix into DLLs | ⏳ Planned | ASI Plugin / Proxy DLL |

---

## 🎮 Development Environment

* **Level Design Tools:** Hammer Editor / Custom Source SDK setups.
* **Reverse Engineering Tools:** IDA Pro / Ghidra / Hex-Editors.
* **Target Engine Branch:** Source Engine 2007 (E.Y.E. Proprietary Branch).
