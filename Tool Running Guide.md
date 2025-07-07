## 🛠️ Tool Running Guide – Journals of Jyggalag

---

This is the **complete guide** to running your tools on **Journals of Jyggalag**.

This guide walks you through **how to run all tools**, but not all of them need to be run **every time** you make changes. Below is a summary of when and why each tool should be run:

---

> ⚠️ **Disclaimer:**  
> This guide has been updated for **Journals of Jyggalag v3.3.0**, which is **not yet live** on the Wabbajack UI.  
> While all steps and plugin requirements still apply to **v3.2.2**, you may notice some differences in screenshots, plugin numbers, or mod names — as these have been updated significantly between versions.  
> This disclaimer will be removed once **v3.3.0** is officially released. We are still actively building and testing the new version.

---

### ⚠️ DISCLAIMER – READ THIS FIRST

Adding any mods to **Journals of Jyggalag** falls under **Rule 11**:  
You are modifying the list **at your own risk**.

While we’re happy to try and assist in the Discord, the team is **not obligated** to troubleshoot issues caused by your additions or changes.

Journals of Jyggalag is a **complete modlist**.  
By making alterations, you accept that:

- Everything this guide explains is **not recommended** unless you have prior modding experience or are willing to experiment and learn on your own.
- **You are solely responsible** for anything you break while making modifications.
- If you choose to alter the list, you accept that **you may break your install**, and it's up to **you** to fix it or re-install and start from scratch.

Proceed with caution. You have been warned.

---

### 🕺 Pandora
  - **When to run:** After **adding or removing any animation mod** — including locomotion, idle, combat, OAR animations, or MCO/DAR-based behavior changes.  
  - **What it does:** Compiles behavior data and animation bindings into a functioning output using OAR (Open Animation Replacer). Ensures animations play correctly in-game by linking conditions, behaviors, and transitions into a single cache.

### ⚙️ Synthesis
  - **When to run:** After adding gameplay mods, appearance overhauls, perk overhauls, combat mods, or other systems that use Synthesis patchers.  
  - **What it does:** Automatically generates compatibility patches for things like perks, spells, leveled lists, appearance, high-poly head, terrain, and more, depending on the patchers active for your profile.

### 🧱 ParallaxGen
  - **When to run:** After adding or removing **parallax-enabled textures** or **meshes** (terrain, architecture, armor, clutter, etc.).  
  - **What it does:** Generates height data files used by parallax shaders to create a 3D illusion of depth on **nearby surfaces** like stone walls, roads, cliffs, or ground textures.

### 🌄 xLODGen
  - **When to run:** After adding or removing worldspace-affecting mods (like new landmasses or city overhauls) or landscape textures.  
  - **What it does:** Generates the terrain LOD meshes and textures for worldspaces (LOD4, 8, 16, 32), allowing you to see distant terrain.


### 🧵 TexGen
  - **When to run:** After adding or removing any mod that affects landscape textures, tree models, lighting, weather, or object appearances **that you want represented in LODs**.  
  - **What it does:** Generates texture and normal map data used **exclusively by DynDOLOD**. TexGen must be run before DynDOLOD so distant objects have the correct lighting, shading, and texture data in the final LOD output.

### 🧠 DynDOLOD
  - **When to run:** After running TexGen, and after **any** change to worldspace (like buildings, trees, city overhauls, or anything that modifies what’s visible in the distance).  
  - **What it does:** Creates the dynamic LODs for all objects in the game world — trees, cities, distant clutter — and ties it all together for smooth performance and visuals.

---

You’ll find detailed, step-by-step instructions for each tool below — including how to set them up properly for each profile and how to avoid common errors.

These tools **build off one another in a specific sequence**, and must be run in the **order listed above** for everything to function correctly.
  
If you’re unsure, just follow the guide **step-by-step, top to bottom** — it’s written in the exact order you should run each tool.

---

## 🕺 Step 0: Run Pandora (Only if Using Animations)

This step is only required if you're **adding or removing animation mods** in JOJ — including OAR, MCO, DAR-based movement, combat, or idle animations.  
If you haven’t changed any animations, you can **skip this step** and proceed directly to **Step 1: Synthesis**.

---

### 🧹 1. Clear Old Pandora Output

- In **MO2**, scroll down to the `Outputs` separator.
- Locate the mod:  
  `JOJ - Pandora Output`
- Right-click > **Open in Explorer**
- **Delete everything** inside this folder.

---

### ⚙️ 2. Open Pandora Behavior Engine+

- Launch **Pandora Behavior Engine+** from the **MO2 executable dropdown**.

---

### ☑️ 3. Select All Patchers

- In the **top-left corner**, check the box labeled **Select All**.

![image](https://github.com/user-attachments/assets/ad25c912-3ced-4539-afa4-ea37efa79102)

---

### ▶️ 4. Click Run

- Click the **Run** button at the **bottom of the window**.

---

### 📁 Output Info

By default, Pandora is configured to output to:

```
JOJ - Pandora Output
```

![image](https://github.com/user-attachments/assets/4a57a161-0d81-4dd7-866b-f93aafd83a34)

This is already set correctly for JOJ and does **not** need to be changed.  
However, if you want to change the output location, you can do so by editing the executable settings in MO2 — though this is **not recommended** unless you know exactly what you're doing.

---

### ✅ Pandora Completion

Once Pandora finishes generating the behavior data, you'll see a message at the bottom of the window that says:

> **"Launch finished in (X) seconds"**

![image](https://github.com/user-attachments/assets/a4bf97e5-a311-46f1-8d76-3187f64ba989)

You're good to **close Pandora** at this point.

> 🔄 **Don't forget to refresh MO2** after closing Pandora so the output is recognized properly.

---

## ⚙️ Step 1: Run Synthesis

Each **Journals of Jyggalag** profile uses a prebuilt Synthesis configuration.

#### Supported Profiles:
- `Lord's Vision` – Full experience  
- `Performance` – Lower fidelity, same content  

---

### 🧭 Quick Setup Instructions

1. Open **Synthesis** from the MO2 dropdown.

2. In the **top-right corner**, click the **profile**.

![image](https://github.com/user-attachments/assets/00fbcd9f-d797-4df3-9701-381cb96c6047)

   From the list, select the profile that matches your current MO2 profile:
   - `Lord's Vision`
   - `Performance`

![image](https://github.com/user-attachments/assets/924a565a-6ee5-49c2-8c46-9c6a9a70d920)

3. Once selected, click the **Run** button in the **bottom-left corner**.  
   Synthesis will now execute all patchers relevant to your chosen profile.

4. When complete, you’ll see **“Complete”** in purple text at the top-left corner.

![image](https://github.com/user-attachments/assets/95153c12-8ecf-4ffc-bd30-377fad04ffbf)

5. You can now **close Synthesis**.

---

### ❗ Troubleshooting Blocking Errors

If you receive a **blocking error** when launching or running Synthesis:

1. Close Synthesis and try again.  
2. If the issue persists, it’s typically caused by **Windows permissions** and is **not** related to Synthesis or JOJ.

**Recommended Fixes:**
- Run **MO2 as Administrator** and try again.
- Reboot your PC to clear temp/cache files and try again.

---

### 🔁 Final Step: Re-enable Plugins

Return to **MO2** and re-enable the **three Synthesis plugins** under the `Outputs` separator.

![image](https://github.com/user-attachments/assets/92fbd63c-b733-47f6-b16f-2c2cecdb2251)

---

## 🔧 Step 1.5: Optional VRAMr Output (Recommended for Performance Users)

This step is **optional** and intended for users running the **Performance** profile who want to optimize texture memory usage.

If you choose to generate a **VRAMr Output**, refer to the official resources below:

- 📘 [VRAMr Nexus Page (Mod + Tutorials)](https://www.nexusmods.com/skyrimspecialedition/mods/90557)
- 📜 Guurzak's detailed **VRAMr guide for JOJ** on the **Scrolls of Schtevie Discord**  
  - 🧠 [Join Discord](https://discord.gg/scrollsofschtevie)  
  - 📎 [Direct Guide Link](https://discord.com/channels/1355637388281385071/1380587127854862578)

---

### ⚠️ Tool Order and Activation Notes

- **Run VRAMr** **before** running **ParallaxGen**
- The **VRAMr Output** mod must be **enabled** while running:
  - ✅ ParallaxGen
  - ✅ xLODGen

- The **VRAMr Output** mod must be **disabled** before running:
  - ❌ TexGen
  - ❌ DynDOLOD

- After all tools are finished, you may **re-enable the VRAMr Output** for normal gameplay.

---

✅ If you're not generating a custom VRAMr output, skip this step and move on to **ParallaxGen**.

---

## 🏔️ Step 2: Run ParallaxGen

> ⚠️ Before you run ParallaxGen, follow these steps carefully.

---

### 🔻 Disable Existing Outputs

In **Mod Organizer 2**, scroll to the bottom of the left panel and locate the `Outputs` separator.  
**Disable** the following mods:

- `JOJ - DynDOLOD Output (Your Profile)`
- `JOJ - TexGen Output (Your Profile`

![image](https://github.com/user-attachments/assets/c9bae4d0-46c7-4ea3-85c1-c99f85048356)


✅ Keep these disabled for now, even after the ParallaxGen step is complete.

---

### 🧹 Clear Old Output Files

1. **Delete the contents** of the existing output mod folder:
- In MO2, right-click on `JOJ - ParallaxGen Output (Your Profile` and choose **Open in Explorer**
- Delete **all files inside** this folder

---

### ▶️ Run ParallaxGen

1. Open **ParallaxGen**.
2. In the **Profile** dropdown, make sure the profile you're currently using is selected.
3. Depending on your profile:
   - For `Lord's Vision` (ENB-enabled):  
     ✅ **Check** the box **"Fix Mesh Lighting (ENB ONLY)"** in the top right.
   - For `Performance` (no ENB):  
     ❌ **Leave this box unchecked**.
4. In the **Output** field, choose a destination folder.  
   > 📁 It’s recommended to create a folder like `Journals of Jyggalag - Outputs\ParallaxGen Output` on the same drive as your installation to keep things organized.
5. ⚠️ **Do not check** the box for **"Zip Output"**.  
   While it won’t break anything, it will make it more difficult to manually copy the generated files later.
6. Click **Start Patching**.
7. Let the process run until **complete**.

![image](https://github.com/user-attachments/assets/4965611a-1279-45eb-b28d-2b7ff19295a2)


> 💬 **Note:** You may see warnings — that’s perfectly fine. As long as ParallaxGen finishes without a critical error, you're good to go.

---

### 📦 Move the Output to MO2

Once ParallaxGen finishes, you must manually move the generated files into the correct mod folder.

1. Navigate to wherever you told ParallaxGen to Output the data:

Your Drive:\Journals of Jyggalag - Outputs if you're following along exactly


2. Inside, you’ll these files

![image](https://github.com/user-attachments/assets/1d68a23d-766e-4bd4-b8af-9160fe550e98)
   
- Cut and paste the contents of the zip file into the folder below:
  ```
  Journals of Jyggalag\mods\JOJ - ParallaxGen Output (Your Profile)
  ```

3. Back in MO2, click the **Refresh** button so it detects the new files

4. **Enable** the `JOJ - ParallaxGen Output (Your Profile)` mod in the left panel

---

### 📜 Sort Plugins Correctly

In the **right-side Plugins tab** of MO2:

- Scroll to the bottom under the `Outputs` section
- Find and move these plugins **under** `Your Profile - Synthesis Patchers`:
- `ParallaxGen.esp`
- `PG_1.esp`

![image](https://github.com/user-attachments/assets/325d5f58-aec4-410c-8ec1-a4d5682a9a4e)

You're now ready to move on to the next tool!

---

## 🌄 Step 3: Run xLODGen

> ⚠️ This tool must be configured correctly for each LOD level (LOD4, LOD8, LOD16, LOD32).

> 📸 I’ve included two screenshots for **each** LOD level below — one for Lord’s Vision/Reserved Vision and one for Performance/Reserved Performance. Please double-check the title above each image to ensure you're using the correct settings for the profile you're configuring.

---

### 📁 Output Location

By default, xLODGen will save its output to:

```
YourDrive:\Journals of Jyggalag - Outputs
```

This is already pre-configured in **MO2 > Modify Executables**, but you can change it if needed.  

![image](https://github.com/user-attachments/assets/62575a96-91b2-4e74-9803-d61e5f5d8eb7)

---

### 🔛 Enable Required Resource

In **Mod Organizer 2**, scroll to the `Outputs` separator and **enable**:

- `xLODGen Resource - SSE Terrain Tamriel`

![image](https://github.com/user-attachments/assets/9a524bcc-1577-419a-9478-d5863ee4d9c5)

This is required for proper terrain LOD generation.

---

### 🧭 Configure Each LOD Level  
Check all worldspaces in the right panel (right-click > **Select All**)

---

### 🔹 LOD4 Settings
- **Lord's Vision**

![image](https://github.com/user-attachments/assets/f8342944-4aac-4e44-9070-a5de883a74f3)

- **Performance**  

![image](https://github.com/user-attachments/assets/e685caab-5760-4554-a173-2c631ccc13df)

---

### 🔹 LOD8 Settings
- **Lord's Vision**  

![image](https://github.com/user-attachments/assets/a96541f1-18bb-4d64-901f-3db691ae8fb7)

- **Performance**  

![image](https://github.com/user-attachments/assets/3eaf00e7-8400-4012-bc2e-22581909ea13)

---

### 🔹 LOD16 Settings
- **Lord's Vision**  

![image](https://github.com/user-attachments/assets/00738425-81a7-47b2-9e81-1f23054499a8)

- **Performance**  

![image](https://github.com/user-attachments/assets/2aa518a3-978d-459e-8ac4-13940d14410b)

---

### 🔹 LOD32 Settings
- **Lord's Vision**  

![image](https://github.com/user-attachments/assets/0b617d8f-053a-46f1-84fa-5bc6b2d9067f)

- **Performance**  

![image](https://github.com/user-attachments/assets/4b3e75b9-5e44-44a2-a611-3ecd8a82e082)


### 📁 Move the Output to MO2

After the LOD levels have been generated, your files will be located in:

`Journals of Jyggalag - Outputs\xLODGen Output\`


1. Navigate to the following folder:

    ```
    Journals of Jyggalag\mods\JOJ - xLODGen Output (Your Profile)
    ```

2. **Delete everything inside this folder** to ensure no remnant files remain  
3. Now open:

    ```
    Journals of Jyggalag - Outputs\XLODGen Output\
    ```

4. Locate the `meshes` and `textures` folders (these should be the only files present)  
5. Copy both folders into the `JOJ - xLODGen Output (Your Profile)` mod folder  
6. Back in MO2, click the **Refresh** button so the changes take effect  

### ⚠️ Step 7: Disable Resource Mod

> **You MUST disable** the `xLODGen Resource - SSE Terrain Tamriel` mod after generating your LODs.  
> Leaving it enabled will cause broken or ugly terrain in-game.

✅ That’s it! You’re now ready to move on to **TexGen**.

---

## 🌾 Step 3.5: Grass Cache (Optional / Advanced)

This step is **optional** — JOJ includes pre-generated grass caches for both supported profiles.  
You are free to use the existing `JOJ - Grass Cache (Your Profile)` mod **without doing anything further**.

However, you **should regenerate your own grass cache** if:

- You’ve added or removed large worldspace/landscape mods (e.g. major quest mods or new land mods)
- You’ve made significant terrain edits or changes to grass settings in INI files

---

### 🧠 How to Regenerate Grass Cache in JOJ

If you choose to regenerate grass cache, **you're on your own for this part**.  
But here’s what you need to know:

1. Inside MO2, locate the mod:

    ```
    JOJ - Grass Cache (Your Profile)
    ```
**Delete everything** inside this mod folder.  
This is required before beginning step 2.3.1 of the guide below.

2. **Read this guide** on Nexus by *infernalryan*:  
   📘 [Grass LOD + Cache Guide](https://www.nexusmods.com/skyrimspecialedition/articles/6919)

3. Skip directly to **Step 2.3.1** in the Nexus guide.  
All required plugins and mod files are already included in JOJ, so earlier steps can be ignored.

> 🔔 **Note:** Grass caching can be time-consuming and performance-intensive.  
> If you're unsure, it's perfectly fine to use the included cache.

---

🎖️ Special thanks to [infernalryan](https://next.nexusmods.com/profile/infernalryan?gameId=1704) for creating the comprehensive grass caching guide.

---

✅ Once finished (or skipped), you’re ready to move on to **TexGen**.

---

## 🎨 Step 4: Run TexGen

> ⚠️ **Important for Performance Users:**  
> If you are using the **Performance** profile and have generated your own VRAMr Output, you must **disable it** before running TexGen.  
> Keep it disabled until **after DynDOLOD** has finished running (the next step).

---

> 🧹 **Clean Slate Reminder:**  
> Just like with ParallaxGen, you must **delete your previous TexGen outputs** before generating new ones.

---

### 🧹 Clear Old TexGen Files

1. In **MO2**, scroll down to the `Outputs` separator
2. **Double-click** `JOJ - TexGen Output (Your Profile)` and choose **Open in Explorer**
3. Inside the folder, **delete the `textures` folder** completely

---

## 🚫 Disable Conflicting Plugins Before TexGen

Before running **TexGen**, you must temporarily **disable the following plugins** in MO2. These can interfere with LOD generation:

- `JOJ - Cell Patch - Lair of Succubi`  
  *(Found in the `JOJ Custom Patches` plugin group)*

- `JOJ - Journal of Followers`  
  *(Found in the `Alternate Perspective` plugin group)*

- `JOJ - Alternate Perspective`  
  *(Also in the `Alternate Perspective` plugin group)*

These plugins should remain **disabled** until after both **TexGen** and **DynDOLOD** are complete.  
Once all LOD tools are finished, you can safely re-enable them.

![image](https://github.com/user-attachments/assets/19b409f8-4e8a-4120-b5c6-ff401feb6e65)

---

### ▶️ Run TexGen

1. Launch **TexGen** from the MO2 dropdown menu
2. Allow it to load completely
3. Make sure your settings match the image below:

![image](https://github.com/user-attachments/assets/4928201a-f07c-4f1e-98f7-3f84f1ad1219)

4. Click **Start** to begin the process

---

### ✅ Finishing Up

Once TexGen completes, it will display a message and a **button to exit**:

![texgen done](https://github.com/user-attachments/assets/706d79ce-f63a-4d36-930e-95c4b1fec907)

- Click **"Exit TexGen"**  
- **DO NOT change the output path** — leave it set to the default

---

### 📁 Move the Output to MO2

1. At the top of the TexGen window, you’ll see the output path  
   *(`Journals of Jyggalag - Outputs\TexGen Output`)*

2. Open that folder, and **copy the `textures` folder** from it

3. Paste it into:

`Journals of Jyggalag\mods\JOJ - TexGen Output (Your Profile)`

4. Back in MO2, click **Refresh**

✅ TexGen is now complete! You're ready for the final step: DynDOLOD.

---

## 🏰 Step 5: Run DynDOLOD

> Just like with ParallaxGen and TexGen, you must delete the old output before running DynDOLOD.

---

### 🧹 Clear Old DynDOLOD Files

1. In **MO2**, scroll to the `Outputs` separator
2. **Double-click** `JOJ - DynDOLOD Output` and choose **Open in Explorer**
3. **Delete all files** inside the folder

---

### ▶️ Step 5: Run DynDOLOD

> ⚠️ **Before launching DynDOLOD, you must disable these specific plugins.**  
> These will cause generation failures if left enabled.

---

### 🔌 **Disable the following plugins in MO2:**

#### 📂 From the `Embers XD` plugin group:
- `JKs Castle Volkihar - Embers XD patch.esp`

![image](https://github.com/user-attachments/assets/ad838833-9696-408e-9d19-564d6b369002)

#### 🗺️ From the `World Map` plugin group:
- `OCW_AMM-SE_FEPatch.esp`

![image](https://github.com/user-attachments/assets/eb31b258-dd57-486d-89b4-37f7678f4805)

#### 🧩 From the `JOJ Custom Patches` plugin group:
- `JOJ - Cell Patch - Lair of Succubi.esp`
- `JOJ - City Patch - Markarth.esp`
- `JOJ - OCW Atlas Map Markers Fix.esp`

![image](https://github.com/user-attachments/assets/e41a85ec-aae8-4d4a-bead-e1920e1f30c1)

#### 🔄 From the `Alternate Perspective` plugin group:
- `JOJ - Alternate Perspective.esp`
- `JOJ - Journal of Followers.esp`

![image](https://github.com/user-attachments/assets/88dbf116-4262-4363-969f-b6a31e3f29ad)

---

✅ Once all these plugins are disabled, you're ready to launch **DynDOLOD**.

1. Launch **DynDOLOD** from the MO2 dropdown menu  
2. Allow it to fully load

> 📁 **Output Location Notice:**  
> The output path for DynDOLOD is set **inside the initial DynDOLOD window**, at the top of the interface.  
> By default, it should point to:  
> `Journals of Jyggalag\tools\DynDOLOD\DynDOLOD_Output\`  
> You may change this path if needed **before starting generation**.

> It is recommended to change your Output location to this so all of your Outputs go in the same place. This isn't required, but it helps keep all your output files organized in one place.:  
> `Journals of Jyggalag - Outputs\DynDOLOD Output\`

![image](https://github.com/user-attachments/assets/1d3a75e3-39e1-4494-9d61-9dd9c49590d0)

---

3. Click `Advanced >>>`
3. In the **top-left checkbox**, make sure **everything is checked**  
   (Right-click > **Select All**)  
4. Double check that your **Output Path** is set to the `Journals of Jyggalag - Outputs\DynDOLOD Output\`. 
5. In the **top-right corner**, select your quality preset based on your profile:

    - **Lord’s Vision** → Click **High**  
    - **Performance** → Click **Medium**

7. Match your other settings to the example provided below

![image](https://github.com/user-attachments/assets/065ce9b7-c817-4fe4-a669-c45ffa5fb046)

8. Allow DynDOLOD to run and complete. Be patient as this generally takes at least an hour, sometimes two depending on your PC specs.
9. Once it completes, just click `Exit DynDOLOD`
    
---

### 📁 Move the Output to MO2

Once DynDOLOD completes, the output files will be located at:

`Journals of Jyggalag - Outputs\DynDOLOD Output` if you followed the above recommended steps.

1. Open that folder and **copy everything inside**
2. Paste all files into:

`Journals of Jyggalag\mods\JOJ - DynDOLOD Output (Your Profile)`


5. Back in MO2, click **Refresh**

---

### 📜 Sort Plugins Correctly

Once you’ve copied the generated DynDOLOD files to the correct folder and enabled the `JOJ - DynDOLOD Output` mod in MO2, you’ll see **three new plugins** in the **right-side Plugins tab**:

- `DynDOLOD.esm` (near the top under Master Plugins)

![image](https://github.com/user-attachments/assets/c53e5bcb-231f-4ce5-a205-a3cc2109747c)

- `DynDOLOD.esp`
- `Occlusion.esp`

![image](https://github.com/user-attachments/assets/b15c29b9-1d58-42ff-b0e8-f6ee24a806e7)

---

### 🔧 Organize the Plugins

Make sure **all three are enabled**, then drag them into the correct plugin groups:

- Move `DynDOLOD.esm` into the `Master Plugins` plugin group
- Move `DynDOLOD.esp` and `Occlusion.esp` into the `Outputs` plugin group
- Ensure that **`DynDOLOD.esp` and `Occlusion.esp` are the final two entries** at the very bottom of your load order.
  
- Don't forget to **re-enable** the following plugins in MO2 from the steps above:**

#### 📂 From the `Embers XD` plugin group:
- `JKs Castle Volkihar - Embers XD patch.esp`

#### 🗺️ From the `World Map` plugin group:
- `OCW_AMM-SE_FEPatch.esp`

#### 🧩 From the `JOJ Custom Patches` plugin group:
- `JOJ - Cell Patch - Lair of Succubi.esp`
- `JOJ - City Patch - Markarth.esp`
- `JOJ - OCW Atlas Map Markers Fix.esp`

#### 🔄 From the `Alternate Perspective` plugin group:
- `JOJ - Alternate Perspective.esp`
- `JOJ - Journal of Followers.esp`

> ⚠️ **Important for Performance Users:**  
> If you are using the **Performance** profiles and have a VRAMr Output, you must **re-enable** it.

---

## ✅ Conclusion

You’ve now finished running all 5 major tools for **Journals of Jyggalag**:
- Synthesis
- ParallaxGen
- xLODGen
- TexGen
- DynDOLOD

If you’ve followed each step carefully, your modlist is now fully rebuilt with accurate terrain, texture, parallax, LOD, and worldspace data.

---

### ⚠️ Final Reminder

> **DISCLAIMER – RULE 11**

Adding any mods to Journals of Jyggalag falls under **Rule 11**:  
> You are modifying the list at your own risk.

While we’re happy to try and assist in the [Discord](https://discord.gg/8ZCa7w8BZQ), the team is **not obligated** to troubleshoot problems caused by your personal additions or changes.

You are responsible for **everything you add or modify** after the Wabbajack install is complete.

---

Thank you for using Journals of Jyggalag. May your LODs be crisp and your crashes few. 🧠✨
