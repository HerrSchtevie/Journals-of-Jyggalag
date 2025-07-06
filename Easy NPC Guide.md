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

1. Launch **EasyNPC** from the MO2 executable dropdown.
2. Let it fully load.
3. **Deselect all plugins**:  
   - Click the checkbox next to **"Load?"** (this will highlight all plugins), then press **Spacebar** to deselect everything.
4. Manually **reselect only the following plugins**:
5. Your plugin numbers may be **slightly different** from mine.  
   - This depends on what **you’ve done to modify the list**, or honestly, what **I’ve changed since writing this guide**.  
   - Either way, your numbers will still be **close enough to follow along**.

### 🧩 Core Skyrim & Creation Club Plugins
**Plugins 1–80**:
- `Skyrim.esm`
- `Update.esm`
- `Dawnguard.esm`
- `HearthFires.esm`
- `Dragonborn.esm`
- All **Creation Club content plugins**
- `_ResourcePack.esl`

### 🛠 Unofficial Patches
- `Unofficial Skyrim Special Edition Patch.esp` *(Plugin 87)*
- `Unofficial Skyrim Creation Club Content Patch.esl` *(Plugin 88)*

### 🧑‍🎤 NPC & Quest Mods
- `3DNPC.esp` *(Plugin 150)*
- `Wyrmstooth.esm` *(Plugin 154)*
- `PAN_LamaesGaze.esp` *(Plugin 265)*
- `AI Overhaul.esm` *(Plugin 283)*  
  > ⚠️ **Do not** set this as the default data source for any NPCs.
- `Better Argonian Horns.esp` *(Plugin 449)*
- `CS_Visions.esm` *(Plugin 2517)*
- `ICNs_ImmersiveCollegeNPCs.esp` *(Plugin 2556)*
- `Children of the Hist.esp` *(Plugin 3237)*

### 🧝 NPC Overhauls & Replacers
- All plugins **below Plugin 3274 – Occlusion**  
  These will include all of your NPC overhauls and appearance replacers.  
  Your plugin numbers may differ slightly depending on which mods you're using.  
  If you followed all the instructions under **"Step 1: Enable NPC Overhaul Mods"**, they’ll all appear here.

---

> 🟡 **Note:**  
> If you see a **yellow warning icon** next to a plugin and you’re unable to enable it, **hover over the warning**. It will tell you what **master plugin** needs to be enabled in order to load it.
 
![easynpc3](https://github.com/user-attachments/assets/93e3ed5c-8104-4232-bec5-fd7315a16d21)
![easynpc4](https://github.com/user-attachments/assets/ba5eacbf-7f7f-47e1-8331-34726f336a12)
![image](https://github.com/user-attachments/assets/f81300ce-273f-446a-922a-cc33bebfa30d)
![image](https://github.com/user-attachments/assets/9564a088-b614-415e-9409-4f99c656576e)
![image](https://github.com/user-attachments/assets/61047918-5e06-4057-91cd-feaee19a1bfa)
![image](https://github.com/user-attachments/assets/6f2c74e1-7c18-43f8-9e58-4619753d7b9f)
![image](https://github.com/user-attachments/assets/984245e5-4883-4dd2-a399-11d8aa34c21e)
![image](https://github.com/user-attachments/assets/fc29ad99-f6a6-4122-bcf1-3e90fb0ef6b3)
![image](https://github.com/user-attachments/assets/43a5b017-bdf2-4381-9347-8c7c650da1e9)
![image](https://github.com/user-attachments/assets/cc24b631-81fc-4c2c-9ff8-88d17a9b5dfd)

---

## 🎨 Step 4: Prepare and Build Your Profile

### 🧹 Maintenance Before Merge

Before editing any NPCs, you need to **clear out leftover data** from any previous merges:

1. Go to the **Maintenance** tab.
2. Select the following options:
   - ✅ Reset NPC Defaults  
   - ✅ Reset Face Selection  
   - ✅ Delete Logs  
   - ✅ Trim Autosave  

![image](https://github.com/user-attachments/assets/1dc19c40-f794-4121-ac7f-3a1f31ba9a73)

Once done, return to the **Profiles** tab to begin customizing your NPCs.

---

### 🧱 Building Your Profile

1. Navigate to the **Profiles** tab.
2. Scroll through the list of NPCs and choose the **face appearance** you prefer for each one.

> 🧩 You are free to **mix and match** appearances from any NPC overhaul in your load order.

---

### 🧠 Understanding Sources

Each NPC has **two selectors**:

- 🔷 **Default Source (Blue Box)**  
  - Controls where the **AI/Dialogue, data assets, meshes/textures** come from.
- 👑 **Face Source (Green Crown)**  
  - Controls the actual **appearance** of the NPC (based on mugshots).

> ⚠️ **IMPORTANT:**  
> No NPC should ever have `AI Overhaul.esm` set as their **Default Source**.  
> This will cause blackface and other visual bugs.

#### 🔍 To quickly find and fix this:

1. Click the **funnel icon** under the Profile tab.
2. In the search bar, enter: `default plugin: AI Overhaul`
3. This will filter the list to show **only NPCs** using `AI Overhaul.esm` as their **Default Source**.
4. For **every single NPC**, you must change the Default Source (Blue Box) to one of the following:
   - ✅ `Unofficial Skyrim Special Edition Patch.esp` *(preferred — this should be used whenever possible)*
   - ✅ `Skyrim.esm` *(only use this if USSEP is not available for that NPC)*

> ⚠️ **Important:**  
> **Every NPC in your list must use either `USSEP` or `Skyrim.esm` as their Default Source.**

![image](https://github.com/user-attachments/assets/6f947a16-c088-4b0d-a077-8c637a1a50fe)

> 💬 **"Plugin not loaded"** warnings can be ignored unless you are actively editing that NPC.  
> These typically appear when mugshots don’t load, but they will not break your merge.

---

## 🛡️ Step 5: Build the Merge File

1. Go to the **Build** tab  
2. Review the **Alerts** tab:
   - Warnings about "suspicious masters" can typically be ignored unless you're encountering build errors
   - The Archive `Wintersun - Faiths of Skyrim - Textures.bsa`, alert can be safely disregarded.   
   - If any required NPC records are missing or unresolved, resolve those before continuing  

3. Under **Output Settings**:
   - **Mod Name**: `JOJ - NPC Merge`  
   - ✅ **Pack files into archives** (recommended)  
   - ✅ **Attempt conversion of wigs to head parts**  

4. When ready, click **Build** in the upper right corner  

![image](https://github.com/user-attachments/assets/503188d3-e1b5-47ae-9037-3125a9320b4c)

---

## ✅ Step 6: Finalize and Organize

After the build completes, you'll get a success message:

> “Your NPC Merge is ready at:  
> `YourDrive:\Journals of Jyggalag\mods\JOJ - NPC Merge (Lord's Vision)` or `YourDrive:\Journals of Jyggalag\mods\JOJ - NPC Merge (Reserved Vision)` depending on your profile.

![image](https://github.com/user-attachments/assets/b241093d-2649-4bcb-9b02-2a9dab64fcc0)

---

### 📦 Post-Build Steps in MO2

1. Close EasyNPC  
2. Enable **`JOJ - NPC Merge Profile (Lord's Vision)` or `JOJ - NPC Merge Profile (Reserved Vision)`** depedning on your profile in MO2  
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
