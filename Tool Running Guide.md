## 🛠️ Tool Running Guide – Journals of Jyggalag

---

This is the **complete guide** to running your tools on **Journals of Jyggalag**.

This guide walks you through **how to run all tools**, but not all of them need to be run **every time** you make changes. Below is a summary of when and why each tool should be run:

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

![step one outputs](https://github.com/user-attachments/assets/5017ebfa-5dc1-4a39-b5cb-f6825d533f9f)


✅ Keep these disabled until you've finished running **all the tools** in this guide.

---

### 🧹 Clear Old Output Files

You must fully clear out any existing ParallaxGen data before generating new output.

1. **Delete the existing output `.zip` file**:

Journals of Jyggalag\tools\ParallaxGen\ParallaxGen_Output


2. **Delete the contents** of the existing output mod folder:
- In MO2, right-click on `JOJ - ParallaxGen Output` and choose **Open in Explorer**
- Delete **all files inside** this folder

---

### ▶️ Run ParallaxGen

- Open ParallaxGen
- Click **Start Patching**
- Let it run until complete

![unnamed](https://github.com/user-attachments/assets/23f91ee8-8fc6-4b10-af63-f642b44e25d1)


> 💬 **Note:** You may see warnings — that’s perfectly fine. As long as ParallaxGen finishes without a critical error, you're good to go.

---

### 📦 Move the Output to MO2

Once ParallaxGen finishes, you must manually move the generated files into the correct mod folder.

1. Navigate to:

Journals of Jyggalag\tools\ParallaxGen\ParallaxGen_Output


2. Inside, you’ll see a `.zip` file:
- Either **unzip it directly** into:
  ```
  Journals of Jyggalag\mods\JOJ - ParallaxGen Output
  ```
- **OR** cut and paste the contents of the zip file into the folder above

3. Back in MO2, click the **Refresh** button so it detects the new files

4. **Enable** the `JOJ - ParallaxGen Output` mod in the left panel

---

### 📜 Sort Plugins Correctly

In the **right-side Plugins tab** of MO2:

- Scroll to the bottom under the `Outputs` section
- Find and move these plugins **under** `JOJ - Synthesis Patch`:
- `ParallaxGen.esp`
- `PG_1.esp`

![unnamed (1)](https://github.com/user-attachments/assets/d04f3775-571a-46c9-8c19-9dcc9ebabe87)


You're now ready to move on to the next tool!

## 🌄 Step 3: Run xLODGen

> ⚠️ This tool must be run **four times**, once for each LOD level (LOD4, LOD8, LOD16, LOD32).

---

### 🔛 Enable Required Resource

In **Mod Organizer 2**, scroll to the `Outputs` separator and **enable**:

- `xLODGen Resource - SSE Terrain Tamriel`

This resource is required for proper terrain LOD generation.

---

### 🧭 Run xLODGen for Each LOD Level

Each time you open xLODGen, you'll be generating a specific LOD level. After each run:

- You’ll see a message at the bottom that says:  
  `"LOD generation complete"`
- **Close and reopen xLODGen** before starting the next level

Make sure to:
- **Check all worldspaces** in the **right panel** (right-click > **Select All**)

---

### 🔹 LOD4 Settings

![lod4](https://github.com/user-attachments/assets/0de0bf79-e05f-4459-ab8e-220be43d658b)

- Run xLODGen with the **LOD4** settings shown above
- Once complete, close xLODGen

---

### 🔹 LOD8 Settings

![lod8](https://github.com/user-attachments/assets/f2c752c9-d1cc-4071-8675-0df1677b80de)

- Reopen xLODGen
- Run with the **LOD8** settings
- Once complete, close xLODGen

---

### 🔹 LOD16 Settings

![lod16](https://github.com/user-attachments/assets/3a86e744-342a-4b35-a61b-fc6e5bb8df6e)

- Reopen xLODGen
- Run with the **LOD16** settings
- Once complete, close xLODGen

---

### 🔹 LOD32 Settings

![lod32](https://github.com/user-attachments/assets/3bed4c6c-df81-43f2-aa66-10128cab4cdf)

- Reopen xLODGen
- Run with the **LOD32** settings
- Once complete, close xLODGen

---

### 📁 Move the Output to MO2

After all four LOD levels have been generated, your files will be located in a new folder:

Journals of Jyggalag - Outputs\lodgen outputs\


1. Open this folder and locate the `meshes` and `textures` folders
2. Copy both folders into:

Journals of Jyggalag\mods\JOJ - xLodGen Output


3. If prompted, **replace all existing files**
4. Back in MO2, click the **Refresh** button so the changes take effect
5. Disable the "xLODGen Resource - SSE Terrain Tamriel" mod when finished with xLODGen

✅ That’s it! You’re now ready to move on to TexGen.

## 🎨 Step 4: Run TexGen

> Just like with ParallaxGen, you must **delete previous TexGen outputs** before generating new ones.

---

### 🧹 Clear Old TexGen Files

1. In **MO2**, scroll down to the `Outputs` separator
2. **Double-click** `JOJ - TexGen Output` and choose **Open in Explorer**
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
   *(usually something like `Journals of Jyggalag - Outputs\TexGen_Output`)*

2. Open that folder, and **copy the `textures` folder** from it

3. Paste it into:

Journals of Jyggalag\mods\JOJ - TexGen Output

4. Overwrite any files if prompted

5. Back in MO2, click **Refresh**

✅ TexGen is now complete! You're ready for the final step: DynDOLOD.


## 🏰 Step 5: Run DynDOLOD

> Just like with ParallaxGen and TexGen, you must delete the old output before running DynDOLOD.

---

### 🧹 Clear Old DynDOLOD Files

1. In **MO2**, scroll to the `Outputs` separator
2. **Double-click** `JOJ - DynDOLOD Output` and choose **Open in Explorer**
3. **Delete all files** inside the folder

Even though it’s empty now, you must still:
- **Re-enable** the `JOJ - DynDOLOD Output` mod in MO2

---

### ▶️ Run DynDOLOD

1. Launch **DynDOLOD** from the MO2 dropdown menu
2. Allow it to fully load
3. In the **top-left checkbox**, make sure **everything is checked** (right-click > **Select All**)
4. Match your settings to the example below:

![dyndolod](https://github.com/user-attachments/assets/3846a86f-d896-494b-a192-5f2e5b6980aa)

5. Click **OK** to begin generation

> ⏳ Note: This process can take **an hour or more** depending on your PC — be patient!

6. Once DynDOLOD has finished, click **"Save and Exit"**

![dyndolod done](https://github.com/user-attachments/assets/6ff1dbea-d779-403f-b84f-1b64164c2d72)

---

### 📁 Move the Output to MO2

Once DynDOLOD completes, the output files will be located at:

Journals of Jyggalag - Outputs\dyndolod output


1. Open that folder and **copy everything inside**
2. Paste all files into:

Journals of Jyggalag\mods\JOJ - DynDOLOD Output


3. Overwrite any files if prompted
4. Back in MO2, click **Refresh**

---

### 📜 Sort Plugins Correctly

Once you’ve copied the generated DynDOLOD files to the correct folder and enabled the `JOJ - DynDOLOD Output` mod in MO2, you’ll see **three new plugins** in the **right-side Plugins tab**:

- `DynDOLOD.esm`
- `DynDOLOD.esp`
- `Occlusion.esp`

![dyndolod done](https://github.com/user-attachments/assets/f296dee5-0b74-40ae-b3f4-4b0184f924f9)

---

### 🔧 Organize the Plugins

Make sure **all three are enabled**, then drag them into the correct plugin groups:

- Move `DynDOLOD.esm` into the `Mod Resources` plugin group
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
