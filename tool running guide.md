# 🛠️ Tool Running Guide – Journals of Jyggalag

This is the complete guide to running your tools on **Journals of Jyggalag**.  
Please note: you **only need to run these tools** if you add mods that make **major changes to the worldspace** — such as quest mods, city overhauls, or new landmasses.

---

### ⚠️ DISCLAIMER – READ THIS FIRST

Adding any mods to Journals of Jyggalag falls under **Rule 11**:  
> You are modifying the list at your own risk.

While we’re happy to try and assist in the [Discord](https://discord.gg/8ZCa7w8BZQ), the team is **not obligated** to help troubleshoot issues caused by your additions or changes.

You are responsible for **everything you add or change** after the Wabbajack installation is complete.

---

## ⚙️ Step 1: Run Synthesis

1. Open **Synthesis** from the dropdown menu in **Mod Organizer 2 (MO2)**.
2. Allow it to load completely — once it finishes, you'll see the **Run** button at the bottom.
3. Click **Run** and let the patching process complete.

---

### ❗Troubleshooting Blocking Errors

If you receive a blocking error when launching or running Synthesis:

- **First**, close Synthesis and try launching it again.
- If the issue persists, it's likely caused by **Windows permissions** — this is **not** a Wabbajack or Journals of Jyggalag issue.

#### ✅ Fixes:
- Run **MO2 as Administrator**
- Reboot your PC to clear temp/cache files and try again

If you're still stuck, feel free to ask in the Discord server for help!


## 🏔️ Step 2: Run ParallaxGen

> ⚠️ Before you run ParallaxGen, follow these steps carefully.

---

### 🔻 Disable Existing Outputs

In **Mod Organizer 2**, scroll to the bottom of the left panel and locate the `Outputs` separator.  
**Disable** the following mods:

- `JOJ - DynDOLOD Output`
- `JOJ - TexGen Output`

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

You're now ready to move on to the next tool!


