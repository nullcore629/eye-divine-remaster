# E.Y.E: Divine Cybermancy — Remastered

The main goal is to remaster the maps of the awesome game E.Y.E: Divine Cybermancy.

Simply put, this project definitely aims to fix all blatant visual bugs across the maps, as shown in the examples below:

### 🛠️ Visual Bug Fixes
*(Screenshots with red circles highlighting the problem areas will be placed here)*

1. **[Screenshot 1]** — Description of the visual bug in the first screenshot (e.g., a huge prop stands directly under a lamp, but due to a Source lighting origin bug, it is pitch black).
2. **[Screenshot 2]** — Description of the flaw (e.g., a texture breaking at a geometry seam or clipping right through).
3. **[Screenshot 3]** — Another example of a bug.

### 👁️ Scene Readability and Depth
I also want to improve the readability and depth of many scenes in rooms or open spaces on the maps... for example...

* **[Example 1]:** Huge halls where everything blends into a gray mush. I will be adding proper fog (`env_fog_controller`) for depth and volume.
* **[Example 2]:** Rooms where it is impossible to tell where to go. I will set up proper lighting accents on doors and pathways so players don't get lost in broad daylight.

### 🧰 Tools
I am using:
* **Hammer++** (for Garry's Mod) — because the original Hammer is way too ancient and constantly crashes.
* **BSPSource** — to decompile the game's original maps.
* **VIDE** — to extract texture packs and models so nothing gets lost.
* ...and other minor workarounds and tweaks.

### 🔄 Development Process
The main challenge here is **not** tweaking the graphics. The real nightmare starts right after decompiling with `bspsource`. The maps break, and you have to manually rebuild all the logic, triggers, and scripts that were lost or turned into pure chaos during the decompilation process. Hammer++ and VIDE are used precisely to fix this mess.

### 📊 Remaster Progress
*Current development status by stages and maps:*

| Task / Map | Status | Comment |
| :--- | :---: | :--- |
| **Toolchain** | ✅ Done | Hammer++ is configured, and suitable compilers for the game's BSP format have been found. |
| **Compilation Test** | ✅ Done | The map was successfully decompiled, recompiled, and runs in E.Y.E. `buildcubemaps` works, reflections are intact. |
| **Logic: `cm_warp_d.bsp`** | ⏳ In Progress | Restoring broken triggers, scripts, and overall level logic after decompilation. Nothing works yet. |
| **Graphics: `cm_warp_d.bsp`** | ❌ Not Started | Eliminating obvious, stupid visual bugs (black props, broken shadows). |
| **Light & Depth: `cm_warp_d.bsp`** | ❌ Not Started | Improving lighting, setting up fog, and enhancing room readability. |

*(Statuses: ✅ Done | ⏳ In Progress | ❌ Not Started)*



