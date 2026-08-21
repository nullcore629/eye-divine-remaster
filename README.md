# E.Y.E: Divine Cybermancy - Remastered

The main goal is to remaster the maps of the awesome game E.Y.E: Divine Cybermancy.

### 🧰 Tools
I am using:
* **Hammer++** (for Garry's Mod) - because the original Hammer is way too ancient and constantly crashes.
* **BSPSource** - to decompile the game's original maps.
* **VIDE** - to extract texture packs and models so nothing gets lost.
* ...and other minor workarounds and tweaks.

### 🔄 Development Process
The main challenge here is **not** tweaking the graphics. The real nightmare starts right after decompiling with `bspsource`. The maps break, and you have to manually rebuild all the logic, triggers, and scripts that were lost or turned into pure chaos during the decompilation process. Hammer++ and VIDE are used precisely to fix this mess.

### 📊 Remaster Progress
*Current development status by stages and maps:*

| Task / Map | Status | Comment |
| :--- | :---: | :--- |
| **Toolchain** | ✅ Done | Hammer++ is configured, and suitable compilers for the game's BSP format have been found. |
| **Compilation Test** | ✅ Done | The map was successfully decompiled, recompiled, and runs in E.Y.E. `buildcubemaps` works, reflections are intact. |
| **Logic: `warp.bsp`** | ⏳ In Progress | Restoring broken triggers, scripts, and overall level logic after decompilation. Nothing works yet. |
| **Graphics: `warp.bsp`** | ❌ Not Started | Eliminating obvious, stupid visual bugs (black props, broken shadows). |
| **Light & Depth: `warp.bsp`** | ❌ Not Started | Improving lighting, setting up fog, and enhancing room readability. |

*(Statuses: ✅ Done | ⏳ In Progress | ❌ Not Started)*



