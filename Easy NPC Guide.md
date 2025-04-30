# 🧑‍🎨 EasyNPC Customization Guide – Journals of Jyggalag

Welcome, Champion of Order.

This guide walks you through how to **rebuild or customize your NPC appearance merge** using [EasyNPC](https://www.nexusmods.com/skyrimspecialedition/mods/56095). This tool gives you full visual control over how characters appear in your game.

---

## 🧠 What is EasyNPC?

EasyNPC is a GUI-based tool that lets you:

- Compare NPC overhauls side-by-side  
- Resolve mod conflicts easily  
- Generate your own merged plugin and FaceGen data  
- Eliminate blackface bugs and reduce plugin count  

---

## ✨ Why It’s Included

After repeated requests from v1.0.0 users, the latest version of **Journals of Jyggalag** includes **all the NPC overhauls** used in the original merge. This gives you the freedom to:

- Use the default setup  
- Customize your aesthetics  
- Build your own merge safely  

---

### ⚠️ DISCLAIMER – Rule 11

> **You are modifying the modlist at your own risk.**

While support may be available on our [Discord](https://discord.gg/8ZCa7w8BZQ), we are not obligated to help troubleshoot issues resulting from custom edits.

---

## 📸 Step 0: Install Mugshots for EasyNPC

1. Before opening **EasyNPC**, go to my Nexus page:  
   [Journals of Jyggalag](https://www.nexusmods.com/skyrimspecialedition/mods/146771?tab=files) and download the file **"JOJ - NPC Mugshots"**  
2. Unzip this file and place the **`Mugshots`** folder (the entire folder) into: `Journals of Jyggalag > tools > EasyNPC`  
3. This download also includes a file called **`JOJ - NPC Merge profile 2.0.txt`**.  
   You will use this in **Step 4** below, and it can remain in the same `EasyNPC` folder along with the Mugshots  
4. This will allow you to see the faces of the NPCs you are trying to select, making the selection process much easier  
5. Note: This pack only includes mugshots for NPC overhauls already included in Journals of Jyggalag. If you're adding your own NPC overhauls, you'll need to find mugshots for those separately.  
   You can find a community-made mugshot collection here: [Natural Lighting Mugshots (for EasyNPC)](https://www.nexusmods.com/skyrimspecialedition/mods/97595)  

---

## 🛠️ Step 1: Enable NPC Overhaul Mods

1. In **MO2**, scroll to the `EasyNPC` separator in the left panel.  
2. **Enable each mod one at a time, in order**, from top to bottom. Enabling mods one-by-one ensures the plugin order in the right panel mirrors the order of mods in the left panel, which helps preserve a clean and consistent plugin load order during the merge process.

![easynpc1](https://github.com/user-attachments/assets/405ba829-8a56-4411-8446-34b9465408d3)

3. Do the same in the right panel (Plugins):  
   - Click the first EasyNPC plugin, hold **Shift**, and click the last  
   - Right-click > **Create Group** > Name it `EasyNPC`  
   - Move this group just above the “Outputs” group for clarity  

![easynpc2](https://github.com/user-attachments/assets/2bfb065f-46e7-49d1-a9a3-f56358e0b17c)

---

## 🛹 Step 2: Clean Previous Merge

1. In the **right panel**, disable:  
   - `JOJ - Synthesis Patch.esp, ParallaxGen.esp, PG_1.esp, Occlusion.esp, DynDOLOD.esp` *(temporarily)*

2. In the **left panel**, locate `JOJ - NPC Merge` under the `Outputs` separator  
   - Right-click > **Open in Explorer**  
   - Delete **everything inside the folder**  

3. Close and Reopen MO2 to fully refresh

---

## ▶️ Step 3: Run EasyNPC

1. Launch **EasyNPC** from the MO2 dropdown  
2. Let it load fully  
3. **Deselect all plugins** (easiest way to do this is click the box next to "Load?" which will highlight everything, then press spacebar to deselect everything), then manually select only the following:
   - `Skyrim.esm`, `Update.esm`, `Dawnguard.esm`, `HearthFires.esm`, `Dragonborn.esm`  
   - All **Creation Club plugins** (Plugins 1–80)  
   - `_ResourcePack.esl`, `Unofficial Skyrim Special Edition Patch.esp`, and `Unofficial Skyrim Creation Club Content Patch.esl` (Plugins 87–88)  
   - `Wyrmstooth.esm`, `CS_Visions.esm`, and `AI Overhaul.esm`  
   - Any additional **NPC overhaul mods** that you intend to merge (they will be towards the bottom if you included your NPC mods in the EasyNPC plugin group that we created in Step 1)  
   - Be careful **not** to set `AI Overhaul.esm` as the default data source for any NPCs manually. If you're using the provided `JOJ - NPC Merge profile 2.0.txt`, this has already been set up correctly—but it's still a 
     good idea to double check. It should only be enabled to ensure compatibility with Sons of Nirn during the merge process.  
   - When enabling `Project ja-Khajay`, `Children of the Pariah`, and `Argonian Overhaul`, **do not** select their patch plugins—only enable the **masters**.  
 

![easynpc3](https://github.com/user-attachments/assets/93e3ed5c-8104-4232-bec5-fd7315a16d21)
![easynpc4](https://github.com/user-attachments/assets/ba5eacbf-7f7f-47e1-8331-34726f336a12)
![easynpc10](https://github.com/user-attachments/assets/cfb2120d-e89a-49cf-9fa6-a87b4f9d151b)
![easynpc11](https://github.com/user-attachments/assets/7f256593-ff6c-4ba6-ac99-a03a5b41da01)
![easynpc12](https://github.com/user-attachments/assets/f4cf6af2-c722-49b1-9fc8-f30128856237)
![easynpc12 5](https://github.com/user-attachments/assets/49278c33-46ed-457a-9723-ba3ed5a117a9)
![easynpc13](https://github.com/user-attachments/assets/798d6939-a0e6-4765-84b3-966650f6f03a)

---

## 🎨 Step 4: Build Your Profile

1. Go to the **Profiles** tab  
2. Select NPCs and choose the visual appearance you'd like for each  

> You are free to mix and match faces from any available overhaul.

---

### 🧠 How This Works

- **Blue Box** = Default Source (determines FaceGen assets)  
- **Green Crown** = Face Source (determines face appearance)

✅ **Only change the Face Source**  
🚫 Do **not** change the Default Source

> Ignore “Plugin not loaded” warnings unless it’s for an NPC you’re actively editing. These are safe to skip if mugshots don’t load.

![easynpc5](https://github.com/user-attachments/assets/17932b3a-1a40-452f-b5c0-b49ba6e2b82b)

---

## 🛡️ Step 5: Build the Merge File

1. Go to the **Build** tab  
2. Review the **Alerts** tab:
   - Warnings about "suspicious masters" can typically be ignored unless you're encountering build errors  
   - If any required NPC records are missing or unresolved, resolve those before continuing  

3. Under **Output Settings**:
   - **Mod Name**: `JOJ - NPC Merge`  
   - ✅ **Pack files into archives** (recommended)  
   - ✅ **Attempt conversion of wigs to head parts**  

4. When ready, click **Build Anyway** in the upper right corner  

![easynpc6](https://github.com/user-attachments/assets/cb4d4a18-e2b0-4d68-8ba6-51e4e715688c)

---

## ✅ Step 6: Finalize and Organize

After the build completes, you'll get a success message:

> “Your NPC Merge is ready at:  
> `YourDrive:\Journals of Jyggalag\mods\JOJ - NPC Merge`” Please note that my picture output path is slightly different, as this was just an example.

![easynpc7](https://github.com/user-attachments/assets/eadea260-d5bd-4977-8750-1d5fc4abef78)

---

### 📦 Post-Build Steps in MO2

1. Close EasyNPC  
2. Enable `JOJ - NPC Merge` in MO2  
3. Refresh your MO2 panels  

You’ll now see **4–5 new plugins** appear at the bottom of your plugin list.

- Select all of them, then right-click > **Create Group** > Name it `EasyNPC Merge`  
- Move this new group just **above** the `Outputs` plugin group  
- Enable all the plugins inside the new `EasyNPC Merge` group  

![easynpc8](https://github.com/user-attachments/assets/8abc82e4-aa91-4fa8-a31f-9b96dd027322)

---

### ❌ Final Cleanup (IMPORTANT)

Once the new merge is active:

- **Disable ALL mods under the EasyNPC separator**  
  These were only needed for the merge. Leaving them enabled will cause plugin duplication, blackface bugs, and instability.

![easynpc9](https://github.com/user-attachments/assets/5b2898a1-c307-47e9-bced-a934df69c591)

---

## 🗞️ Conclusion

You're done!

Your NPCs are now fully customized with FaceGen data, clean plugin architecture, and no blackface bugs.

### 🔥 REMINDER – RULE 11

You chose to modify the modlist:

- You are responsible for any issues this causes  
- Re-read this guide carefully if something breaks  
- Support is not guaranteed

---

Thanks for taking the time to customize your experience — that’s the spirit of modding. Enjoy your tailored adventure in the Journals of Jyggalag. 👑

-Herr Schtevie
![Jyggalag red](https://github.com/user-attachments/assets/16abb99e-2b78-45b9-8896-4969ebd1e38d)
