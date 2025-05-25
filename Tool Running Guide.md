## 🛠️ Tool Running Guide – Journals of Jyggalag

---

## 📚 Table of Contents

1. [🧰 Introduction](#-introduction)
2. [⚠️ Disclaimer](#️-disclaimer)
3. [🛠️ Tool Overview](#-tool-overview)
4. [🧬 Step 1: Run Synthesis](#-step-1-run-synthesis)
5. [🧼 Step 2: Run ParallaxGen](#-step-2-run-parallaxgen)
6. [🌄 Step 3: Run xLODGen](#-step-3-run-xlodgen)
7. [🎨 Step 4: Run TexGen](#-step-4-run-texgen)
8. [▶️ Step 5: Run DynDOLOD](#-step-5-run-dyndolod)
9. [📦 Conclusion](#-conclusion)
10. [📌 Final Disclaimer](#-final-disclaimer)

---

##Introduction 

This is the **complete guide** to running your tools on **Journals of Jyggalag**.

This guide walks you through **how to run all tools**, but not all of them need to be run **every time** you make changes. Below is a summary of when and why each tool should be run:

---

##⚠️ DISCLAIMER – READ THIS FIRST

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

##Tool Overview

---

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

### ⚙️ Step 1: Run Synthesis

Each **Journals of Jyggalag** profile uses a unique Synthesis patcher setup. You must configure Synthesis properly for your chosen profile **before running it**, or the patchers may generate incorrect data.

#### Supported Profiles:
- `Lord's Vision` – Full experience  
- `Performance` – Lower fidelity, same content  
- `Reserved Vision` – Immersion-focused visuals  
- `Reserved Performance` – Immersion + performance

---

### 🔧 Setting Up Synthesis for Your Profile

1. In **Mod Organizer 2 (MO2)**, go to the **Plugins tab**.  
   In the **`Outputs`** plugin group, **disable all plugins** before running Synthesis.  
   ⚠️ This prevents circular patching, load order issues, and unwanted data duplication.
   
   ![image](https://github.com/user-attachments/assets/ccd5d094-58eb-45e9-8c80-ffd88a0f3934)

2. In the top-right MO2 dropdown menu, click **Edit...**
   
   ![image](https://github.com/user-attachments/assets/30e34f8f-21e9-47db-a350-55ef82d0da3e)

3. In the left-hand list, select **Synthesis**.
   
   ![image](https://github.com/user-attachments/assets/13202921-5c58-456f-8e45-461c99e2f396)
 
4. In the field labeled `Create files in mod instead of overwrite (*)`, select the correct output folder for your active profile:

```
JOJ - Synthesis Output (Lord's Vision)  
JOJ - Synthesis Output (Performance)  
JOJ - Synthesis Output (Reserved Vision)  
JOJ - Synthesis Output (Reserved Performance)  
```

5. Click **OK** to close the Modify Executables window.

---

### 🧠 Configuring Patchers in Synthesis

1. Launch **Synthesis** from the MO2 dropdown.  
2. Once loaded, verify that the patchers are named correctly for your active profile.  
   - By default, the patchers are labeled for **Lord’s Vision**.  
   - If you're using a different profile, you **must rename** the patchers.

#### 🔁 How to Rename Patchers:
- Click on the patcher’s title (e.g. `Lord's Vision - Synthesis Terrain`)
- Rename it to match your current profile.  
  Example for Reserved Vision:

```
Reserved Vision - Synthesis Terrain  
Reserved Vision - Synthesis Character  
Reserved Vision - Synthesis Gameplay  
```

![image](https://github.com/user-attachments/assets/c9ad1871-a00c-4ec5-8fcc-44148acf50d1)

---

### ▶️ Run the Patchers

Once your patchers are correctly named and the output path is set, click the **Run** button at the bottom of the Synthesis window. Let the process complete — this may take several minutes depending on your system and load order.

✅ You will know the process is complete when you see "Complete" in purple text in the top-left corner.

You can now safely close Synthesis.

Return to MO2 and re-enable the plugins in the Outputs plugin group that you disabled in Step 1.

![image](https://github.com/user-attachments/assets/d2688dc9-31c2-4beb-a654-c84e9fb5ea0e)

---

### ❗ Troubleshooting Blocking Errors

If you receive a **blocking error** when launching or running Synthesis:

1. Close Synthesis and try again.  
2. If the issue persists, it’s typically caused by **Windows permissions** and is **not** related to Synthesis or JOJ.

**Recommended Fixes:**
- Run **MO2 as Administrator** and try again.
- Reboot your PC to clear temp/cache files and try again.

---

## 🏔️ Step 2: Run ParallaxGen

> ⚠️ Before you run ParallaxGen, follow these steps carefully.

---

### 🔻 Disable Existing Outputs

In **Mod Organizer 2**, scroll to the bottom of the left panel and locate the `Outputs` separator.  
**Disable** the following mods:

- `JOJ - DynDOLOD Output`
- `JOJ - TexGen Output`

(![image](https://github.com/user-attachments/assets/44a9d589-48a2-4d14-9cca-f628f986f52d)


✅ Keep these disabled for noe, even after the ParallaxGen step is complete.

---

### 🧹 Clear Old Output Files

1. **Delete the contents** of the existing output mod folder:
- In MO2, right-click on `JOJ - ParallaxGen Output` and choose **Open in Explorer**
- Delete **all files inside** this folder

---

### ▶️ Run ParallaxGen

1. Open **ParallaxGen**.
2. In the **Profile** dropdown, make sure the profile you're currently using is selected.
3. Depending on your profile:
   - For `Lord's Vision` and `Reserved Vision` (ENB-enabled):  
     ✅ **Check** the box **"Fix Mesh Lighting (ENB ONLY)"** in the top right.
   - For `Performance` and `Reserved Performance` (no ENB):  
     ❌ **Leave this box unchecked**.
4. In the **Output** field, choose a destination folder.  
   > 📁 It’s recommended to create a folder like `Journals of Jyggalag - Outputs` on the same drive as your installation to keep things organized.
5. ⚠️ **Do not check** the box for **"Zip Output"**.  
   While it won’t break anything, it will make it more difficult to manually copy the generated files later.
6. Click **Start Patching**.
7. Let the process run until **complete**.

![image](https://github.com/user-attachments/assets/803686b7-3c67-484e-a905-aefd99a37285)


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

![image](https://github.com/user-attachments/assets/5faac650-ccbe-443d-97e4-974aedf2e12f)

---

### 🔛 Enable Required Resource

In **Mod Organizer 2**, scroll to the `Outputs` separator and **enable**:

- `xLODGen Resource - SSE Terrain Tamriel`

This is required for proper terrain LOD generation.

---

### 🧭 Configure Each LOD Level  
Check all worldspaces in the right panel (right-click > **Select All**)

---

### 🔹 LOD4 Settings
- **Lord's Vision / Reserved Vision**

![image](https://github.com/user-attachments/assets/f8342944-4aac-4e44-9070-a5de883a74f3)

- **Performance / Reserved Performance**  

![image](https://github.com/user-attachments/assets/e685caab-5760-4554-a173-2c631ccc13df)

---

### 🔹 LOD8 Settings
- **Lord's Vision / Reserved Vision**  

![image](https://github.com/user-attachments/assets/a96541f1-18bb-4d64-901f-3db691ae8fb7)

- **Performance / Reserved Performance**  

![image](https://github.com/user-attachments/assets/3eaf00e7-8400-4012-bc2e-22581909ea13)

---

### 🔹 LOD16 Settings
- **Lord's Vision / Reserved Vision**  

![image](https://github.com/user-attachments/assets/00738425-81a7-47b2-9e81-1f23054499a8)

- **Performance / Reserved Performance**  

![image](https://github.com/user-attachments/assets/2aa518a3-978d-459e-8ac4-13940d14410b)

---

### 🔹 LOD32 Settings
- **Lord's Vision / Reserved Vision**  

![image](https://github.com/user-attachments/assets/0b617d8f-053a-46f1-84fa-5bc6b2d9067f)

- **Performance / Reserved Performance**  

![image](https://github.com/user-attachments/assets/4b3e75b9-5e44-44a2-a611-3ecd8a82e082)


### 📁 Move the Output to MO2

After the LOD levels have been generated, your files will be located in:

`Journals of Jyggalag - Outputs\lodgen outputs\`


1. Navigate to the following folder:

    ```
    Journals of Jyggalag\mods\JOJ - xLODGen Output (Your Profile)
    ```

2. **Delete everything inside this folder** to ensure no remnant files remain  
3. Now open:

    ```
    Journals of Jyggalag - Outputs\lodgen outputs\
    ```

4. Locate the `meshes` and `textures` folders (these should be the only files present)  
5. Copy both folders into the `JOJ - xLODGen Output (Your Profile)` mod folder  
6. Back in MO2, click the **Refresh** button so the changes take effect  

### ⚠️ Step 7: Disable Resource Mod

> **You MUST disable** the `xLODGen Resource - SSE Terrain Tamriel` mod after generating your LODs.  
> Leaving it enabled will cause broken or ugly terrain in-game.

✅ That’s it! You’re now ready to move on to **TexGen**.

---

## 🎨 Step 4: Run TexGen

> ⚠️ **Important for Performance Users:**  
> If you are using the **Performance** or **Reserved Performance** profiles, you must **disable the `JOJ - VRAMr (Your Profile)` mod** before running TexGen.  
> Keep it disabled until **after DynDOLOD** has finished running (the next step).

![image](https://github.com/user-attachments/assets/f7809c0c-5746-4b54-81ec-45899dcf4d16)

> 🧹 **Clean Slate Reminder:**  
> Just like with ParallaxGen, you must **delete your previous TexGen outputs** before generating new ones.

---

### 🧹 Clear Old TexGen Files

1. In **MO2**, scroll down to the `Outputs` separator
2. **Double-click** `JOJ - TexGen Output (Your Profile)` and choose **Open in Explorer**
3. Inside the folder, **delete the `textures` folder** completely

---

### ▶️ Run TexGen

1. Launch **TexGen** from the MO2 dropdown menu
2. Allow it to load completely
3. Make sure your settings match the image below:

![texgen](https://github.com/user-attachments/assets/58646424-6da3-4242-9a7a-d1d71e41fc93)

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
   *(`Journals of Jyggalag - Outputs\TexGen_Output`)*

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

> 📁 **Output Location Notice:**  
> The output path for DynDOLOD is set **inside the DynDOLOD window**, near the bottom of the interface.  
> By default, it should point to:  
> `Journals of Jyggalag - Outputs\dyndolod outputs\`  
> You may change this path if needed **before starting generation**.

---

> ⚠️ **Before launching DynDOLOD, you must disable two specific plugins.**  
> These will cause generation failures if left enabled.

**Disable the following plugins in MO2:**
- From the **Embers XD** plugin group:  
  `JKs Castle Volkihar - Embers XD patch.esp`

![image](https://github.com/user-attachments/assets/8d7262b8-50ae-47ae-abe9-2d1bce8cb626)

- From the **World Map** plugin group:  
  `OCW_AMM-SE_FEPatch.esp`

![image](https://github.com/user-attachments/assets/4c7d7344-6266-469a-8691-3e28a334d39f)

---

Once the plugins are disabled:

1. Launch **DynDOLOD** from the MO2 dropdown menu  
2. Allow it to fully load
    > 🛑 **Pop-Up Warnings Notice:**  
    > You’ll likely receive **two warning popups** like the one below. These are safe to ignore.  
    >  
    > ![image](https://github.com/user-attachments/assets/32aafa5a-68f2-489d-88b4-0e4db0e4a584)
    >  
    > These errors are caused by conflicting record types (e.g., a `BOOK` being overwritten by a `CELL`), which are irrelevant to LOD generation.  
    > Just click **Ignore** and allow DynDOLOD to continue loading normally.  
3. In the **top-left checkbox**, make sure **everything is checked**  
   (Right-click > **Select All**)  
4. Set your **Output Path** to the `dyndolod outputs` folder if it isn’t already  
5. In the **top-right corner**, select your quality preset based on your profile:

    - **Lord’s Vision / Reserved Vision** → Click **High**  
    - **Performance / Reserved Performance** → Click **Medium**

7. Match your other settings to the example provided below

![image](https://github.com/user-attachments/assets/5171072b-1a41-4f51-8387-92b3dc492f09)

---

### 📁 Move the Output to MO2

Once DynDOLOD completes, the output files will be located at:

`Journals of Jyggalag - Outputs\dyndolod output`


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
