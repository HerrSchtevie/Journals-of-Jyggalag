
# 📘 Journals of Jyggalag
## 🛠 A Prepper’s Guide to Rule-11
**Written by Aaronavich – 05/18/25**

---

### 🌀 So, you want to introduce a little chaos to order?
Read on…

---

## ⚙️ Preparing MO2

We all love a bit of chaos, but we can easily introduce too much and end up with no way to return to the safety of Order.  
Follow these steps to protect JOJ and ensure all changes are reversible!

### 1. Create a Custom JOJ Profile in Mod Organizer 2

- Click the profile dropdown menu in MO2.
- Select **Manage**.
- In the popup:
  - Choose your base profile (e.g., `Journals of Jyggalag`).
  - Click **Copy**.
  - Name it something like `JOJ - Custom`.
  - Click **Select**, then close the Profiles window.
- **✅ Make sure your custom profile is now selected in MO2!**

![Profile Creation Placeholder](https://github.com/YOUR_USERNAME/YOUR_REPO/blob/main/docs/images/profile_creation.png)

### 2. Make Your Own Output Folders

When you add/remove mods, tools like Synthesis, Pandora, and BodySlide must be re-run. **Don’t overwrite the original outputs**!

- Scroll to the bottom of the **left pane** in MO2.
- Right-click the separator **Not yet Installed**.
- Hover over **All Mods → Create Empty Mod Inside** and name it `Custom BodySlide Output`.
- Repeat for:
  - `Custom Synthesis Output`
  - `Custom Pandora Output`
  - `Custom EasyNPC Output`

Move each folder directly beneath its original and **activate** it.

![Output Mods Placeholder](https://github.com/YOUR_USERNAME/YOUR_REPO/blob/main/docs/images/output_mods.png)

### 3. Link the Tools to Your Custom Output Mods

- Click the ⚙️ **gear icon** in MO2 to open **Executables**.
- For each tool (e.g., BodySlide):
  - Check **Create files in mod instead of overwrite**.
  - Select the appropriate custom output mod.
  - Apply settings.

Also set the output paths inside each tool’s settings (e.g., BodySlide → Advanced → Output Path).

Finally, reorder columns in MO2’s left pane to: `Mod Name → Priority → Conflicts`.

---

## 🔄 Re-installing or Editing Mods

Creating a new profile does **not** protect original mod installs. Always:

1. Right-click and select **Reinstall Mod**.
2. Add the prefix `Custom` during the reinstall to avoid overwriting the original.
3. Match its **priority number** with the original and place it directly below in MO2.
4. **Activate the custom version before deactivating the original.**

> ❗ **Never merge or overwrite the original mod!**  
> Always verify plugin changes via the **Plugins tab** in the right pane.

---

## ➕ Adding New Mods

This section is generalized guidance—not exhaustive.

### Basic Steps:

- ✅ Use Discord search — someone might’ve added it before.
- 🛠 Read the mod page, check compatibility, comments, bug reports.
- 🧠 Use logic and caution. If it adds plugins, **run Synthesis.**
- 💾 Place it under a new separator like `Newly Added Mods`.

> 🎨 Right-click your separators and color-code them to track additions easily.

If unsure, ask in `#🛡️grey-aegis`.

---

## 🔌 Plugin Placement

> ❌ Do NOT run LOOT!

Manually position new plugins to match their placement in the **left pane**.

For accuracy:
- Learn to use **xEdit** to check conflicts.
- Or use **common sense** for rough placement.

---

## 🧰 What Tools to Re-Run When Adding Mods?

> ⚠️ **Non-exhaustive. Use your judgment.**

| Tool         | Re-run When…                                                                 |
|--------------|-------------------------------------------------------------------------------|
| **BodySlide** | Mods with armor, clothing, hair, etc.                                        |
| **Pandora**   | Mods with animation changes (OAR/DAR optional but recommended)               |
| **Synthesis** | Mods that add/remove/replace plugins                                         |
| **EasyNPC**   | Mods that affect NPC appearances                                              |
| **DynDOLOD**  | Exterior world changes (cities, homes, large overhauls)                      |
| **TexGen**    | When running DynDOLOD                                                         |
| **xLODGen**   | When terrain/LOD-related changes are made                                     |
| **ParallaxGen** | Armor/environment textures or anything involving DynDOLOD                   |

📚 Reference: [Tool Running Guide](https://github.com/HerrSchtevie/Journals-of-Jyggalag/blob/Guides/Tool%20Running%20Guide.md)

---

### Important Notes

- 🗑️ Before re-running tools, **deactivate** later output mods and **delete** contents of the relevant output folder.
- 🛑 Double-check tool outputs are linked to **your custom folders**, **not JOJ's originals**.
- 📦 **After DynDOLOD:** Ensure `Occlusion.esp` is placed **below** `DynDOLOD.esp`.

---

## 🚫 A Warning About Disabling Mods

**Just don’t.** If a mod bothers you:

- Disable it via **MCM**, **not** MO2.
- Ask a **Crusader or Arbiter** for help.

---

## 📎 Appendix: Further Learning

- [Reading Crash Logs](https://www.reddit.com/r/skyrimmods/comments/1d0r0f0/reading_crash_logs/)
- [xEdit – Conflict Checks](https://www.youtube.com/watch?v=cKU_R1Hqa4o)
- [xEdit – Simple Conflict Resolution](https://www.youtube.com/watch?v=WSZviB4jqE8)
- [Conflict Resolution & 3D Patching](https://www.nexusmods.com/skyrimspecialedition/mods/37651)
- [Bodyslide Quick Start](https://youtu.be/zil1RwoW3OE)
- [Outfit Studio Tutorial](https://youtube.com/playlist?list=PLrGqMZcWJgElCxyW6GnIlt9HAeeSFlkDI)
- [Creation Kit Basics](https://www.youtube.com/playlist?list=PLD5AA9F15CAA68B07)
- [Immersive Equipment Displays TLDR](https://wiki.wildlandermod.com/11Deep-Dives/Immersive-Equipment-Display/)

---

## ⚔️ Happy Rule 11 Modding  
**Aaronavich & the JOJ Support Team**
