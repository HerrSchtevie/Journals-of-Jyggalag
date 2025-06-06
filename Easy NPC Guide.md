# 🧑‍🎨 EasyNPC Customization Guide – Journals of Jyggalag

---

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

### 📸 Step 0: (Optional) Add Mugshots for EasyNPC

EasyNPC works perfectly without mugshots — but having them makes it much easier to visually select NPC appearances during customization. If you’d like to add mugshots, follow these steps:

1. Download community-made mugshot packs from the following Nexus pages:
   - [SirLach's EasyNPC Mugshot Packs](https://www.nexusmods.com/skyrimspecialedition/mods/74398?tab=description)  
     *Includes mugshots for many major NPC overhauls used in JOJ.*
   - [Natural Lighting Mugshots (for EasyNPC)](https://www.nexusmods.com/skyrimspecialedition/mods/97595)  
     *Well-lit mugshots with a clean background for a variety of NPCs.*

2. Create the following folder structure inside your modlist tools directory:

`Journals of Jyggalag > tools > EasyNPC > Mugshots`

3. Extract all mugshot folders into the `Mugshots` folder. Make sure each folder name matches the mod/plugin name used in your load order.

> ⚠️ **Note:** Mugshots are not required for EasyNPC to function. They simply make it easier to preview NPC faces while customizing.

> 🎯 If you're adding your own NPC overhauls not included in JOJ, you'll need to find or generate mugshots for those separately.

---

## 🛠️ Step 1: Enable NPC Overhaul Mods

1. In **MO2**, scroll to the `Easy NPC` separator in the left panel.  
2. **Enable each mod one at a time, in order**, from top to bottom. Enabling mods one-by-one ensures the plugin order in the right panel mirrors the order of mods in the left panel, which helps preserve a clean and consistent plugin load order during the merge process.

![easynpc1](https://github.com/user-attachments/assets/4088ef1b-a394-41cd-932d-2312781d33b7)

3. In the right panel (Plugins), the plugins can just stay at the very bottom below `Outputs`:  

![image](https://github.com/user-attachments/assets/e71da6fc-1df4-40c0-a768-c09f74fad2b2)

---

## 🛹 Step 2: Clean Previous Merge

> 💡 **Note:**  
> The **Lord's Vision** and **Performance** profiles share the `JOJ - NPC Merge (Lord's Vision)` mod file.  
> The **Reserved Vision** and **Reserved Performance** profiles share the `JOJ - NPC Merge (Reserved Vision)` mod file.

> ⚠️ **Disclaimer:**  
> This guide was created using the **Journals of Jyggalag - Lord's Vision** profile.  
> Some **plugin numbers, filenames, or output folders** may differ slightly in the other profiles.
> Adjust accordingly based on your selected profile.

1. In the **right panel**, disable:  
   - `All Synthesis Patches, ParallaxGen.esp, PG_1.esp, Occlusion.esp, DynDOLOD.esp` *(temporarily)*

2. In the **left panel**, locate `JOJ - NPC Merge (Your Profile)` under the `Outputs` separator  
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
   - `3DNPC.esp`, `Wyrmstooth.esm`, `AI Overhaul.esm`, `Immersive Wenches.esp`, `ICNs_ImmersiveCollegeNPCs.esp`, and `CS_Visions.esm`
   - Any additional **NPC overhaul mods** that you intend to merge (they will be at the very bottom). 
   - Be careful **not** to set `AI Overhaul.esm` as the default data source for any NPCs manually.
 
![easynpc3](https://github.com/user-attachments/assets/93e3ed5c-8104-4232-bec5-fd7315a16d21)
![easynpc4](https://github.com/user-attachments/assets/ba5eacbf-7f7f-47e1-8331-34726f336a12)
![easynpc3](https://github.com/user-attachments/assets/c2459a4a-5758-420f-b331-19662ce79fd3)
![easynpc11](https://github.com/user-attachments/assets/7f256593-ff6c-4ba6-ac99-a03a5b41da01)
![image](https://github.com/user-attachments/assets/6943c11a-90a6-4a8c-8faf-fda18e92eb53)
![image](https://github.com/user-attachments/assets/e50bf6c5-8190-4909-8846-bab0156df703)
![image](https://github.com/user-attachments/assets/15b8189e-379f-4c03-99d2-324776d0a3fb)

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

> **IMPORTANT:** None of your NPCs should have `AI Overhaul.esm` selected as their **Default Source** (Blue Box).  

> Ignore “Plugin not loaded” warnings unless it’s for an NPC you’re actively editing. These are safe to skip if mugshots don’t load.

![3](https://github.com/user-attachments/assets/21f08565-e7d3-4c00-8d22-f851c935ea2c)

---

## 🛡️ Step 5: Build the Merge File

1. Go to the **Build** tab  
2. Review the **Alerts** tab:
   - Warnings about "suspicious masters" can typically be ignored unless you're encountering build errors
   - The Archives `StrangeRunes - Textures.bsa`, `StrangeRunes.bsa`, and `Wintersun - Faiths of Skyrim - Textures.bsa`, alerts can be safely disregarded.   
   - If any required NPC records are missing or unresolved, resolve those before continuing  

3. Under **Output Settings**:
   - **Mod Name**: `JOJ - NPC Merge (Your Profile)`  
   - ✅ **Pack files into archives** (recommended)  
   - ✅ **Attempt conversion of wigs to head parts**  

4. When ready, click **Build** in the upper right corner  

![image](https://github.com/user-attachments/assets/7fc66196-9af3-4ea8-b890-a26230eb51e2)

---

## ✅ Step 6: Finalize and Organize

After the build completes, you'll get a success message:

> “Your NPC Merge is ready at:  
> `YourDrive:\Journals of Jyggalag\mods\JOJ - NPC Merge (Lord's Vision)` or `YourDrive:\Journals of Jyggalag\mods\JOJ - NPC Merge (Reserved Vision)` depending on your profile.

![image](https://github.com/user-attachments/assets/b241093d-2649-4bcb-9b02-2a9dab64fcc0)

---

### 📦 Post-Build Steps in MO2

1. Close EasyNPC  
2. Enable **`JOJ - NPC Merge Profile (Lord's Vision).txt` or `JOJ - NPC Merge Profile (Reserved Vision).txt`** depedning on your profile in MO2  
3. Refresh your MO2 panels  

You’ll now see **4 new plugins** appear at the bottom of your plugin list.

- Select all of them, then right-click > **Create Group** > Name it `JOJ NPC Merge`  
- Move this new group just **above** the `Alternate Perspective` plugin group  
- Enable all the plugins inside the new `Easy NPC Merge` group
- Be sure to re-enable to Output plugins that we disabled in step 2!
`All Synthesis Patches, ParallaxGen.esp, PG_1.esp, DynDOLOD.esp, and Occlusion.esp`  

![image](https://github.com/user-attachments/assets/02bfbad5-1cfe-4c15-8716-30562ac7c5bb)

---

### ❌ Final Cleanup (IMPORTANT)

Once the new merge is active:

- **Disable ALL mods under the EasyNPC separator**  
  These were only needed for the merge. Leaving them enabled will cause plugin duplication, blackface bugs, and instability.

![Screenshot 2025-06-02 170139](https://github.com/user-attachments/assets/a548b61b-eb14-41e5-b084-513d8cdf4d57)

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
