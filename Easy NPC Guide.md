# 🧑‍🎨 EasyNPC Customization Guide – Journals of Jyggalag

Welcome, Champion of Order.

This guide walks you through how to **rebuild or customize your NPC appearance merge** using [EasyNPC](https://www.nexusmods.com/skyrimspecialedition/mods/56095). This tool allows you to visually select which NPC overhauls you prefer — giving you full control over how characters look in your game.

---

## 🧠 What is EasyNPC?

EasyNPC is a GUI-based tool that lets you:
- Compare different NPC overhauls side-by-side
- Resolve conflicts between overhaul mods
- Generate your own merged plugin and FaceGen data
- Eliminate blackface bugs and reduce plugin count

---

## ✨ Why It’s Included

After repeated requests from v1.0.0 users, the latest version of **Journals of Jyggalag** includes **all of the NPC overhaul mods** used in my original merge. This gives you the freedom to:
- Use the default setup
- Make your own aesthetic choices
- Rebuild the entire merge with your preferred overhauls

---

### ⚠️ DISCLAIMER – Rule 11

> **You are modifying the modlist at your own risk.**

While we’ll try to help in the [Discord](https://discord.gg/8ZCa7w8BZQ), the team is not obligated to troubleshoot issues caused by your personal edits or merges.

---

> ## 📸 Important: Add Mugshots Before Starting EasyNPC
>
> To ensure all NPC mugshots load correctly and are properly assigned in EasyNPC:
>
> 1. Download the **[JOJ - NPC Mugshots](https://www.nexusmods.com/skyrimspecialedition/mods/146771?tab=files)** file from Nexus Mods (manual download).
> 2. Unzip the file.
> 3. Copy the entire `Mugshots` folder into the following location:
>
>    ```
>    Journals of Jyggalag\tools\EasyNPC
>    ```
>
> Once this is done, EasyNPC will automatically load the mugshots when you launch the tool, making NPC face selection significantly easier.

---

## 🛠️ Step 1: Enable NPC Overhaul Mods

1. In **MO2**, scroll to the `EasyNPC` separator in the left panel  
2. **Enable every mod** listed under this separator

![easynpc1](https://github.com/user-attachments/assets/2a5d6e3d-6d47-4c49-a0ae-0c617262c2b1)
![easynpc2](https://github.com/user-attachments/assets/bdbe5966-9da6-42aa-b5b2-2c63102d5094)

> 💡 These mods are the source data for your merge.

3. This will enable all of the plugins as well, to ensure there are no issues with this:

**Recommended:**
- Click the first mod in the plugins panel at the bottom
- Hold **Shift**, click the last mod to select all
- Right-click > **Create Group** > I always name it Easy NPC for organiztional purposes
- Move this group just above the “Outputs” plugin group

![easynpc3](https://github.com/user-attachments/assets/a7277e3d-09bf-4dd1-936f-a63a7b97b820)

![easynpc4](https://github.com/user-attachments/assets/a1458d88-b78e-49a6-975c-c55beac12bd3)

---

### 🔄 Step 1.5 (Optional): Remove or Change NPC Replacers

If you want to remove or swap out any NPC mods under `NPC Replacers and Add-Ons`:

1. Disable all mods in that section
2. Rerun Synthesis after all the steps below are completed.

This will unmerge those NPCs and remove dependencies cleanly.

---

## 🧹 Step 2: Disable Synthesis & Clear Previous Merge

1. In the **right panel**, disable:
   - `JOJ - Synthesis Patch.esp`

2. In the **left panel**, find `JOJ - NPC Merge` under the `Outputs` separator  
   - Right-click > **Open in Explorer**
   - Delete **everything inside the folder**

3. Click the **Refresh** button in MO2

---

## ▶️ Step 3: Run EasyNPC

1. Launch **EasyNPC** from the MO2 executables dropdown
2. Let it load fully
3. Ensure **all plugins are checked**, then click **OK**

![easynpc5](https://github.com/user-attachments/assets/a38ae50c-710c-4dad-8451-fbf3606087f6)

---

## 🎨 Step 4: Build Your Profile

1. Go to the **Profiles** tab  
2. This is where you select the faces you want to appear in-game

You can preload my default profile:

- Click the **folder icon** in the top-right
- Navigate to:  
  `Journals of Jyggalag\mods\JOJ - NPC Mugshots`
- Select:  
  `JOJ - NPC Merge profile.txt`

---

### 🧠 How This Works

- **Blue Box** = Default Source (loads textures)  
- **Green Crown** = Face Source (selects face appearance)

> Do **not** change the Default Source — only the Face Source.

> Ignore plugins marked **“Plugin not loaded”** in yellow. Only assign NPCs that have mugshots loaded.

![easynpc6](https://github.com/user-attachments/assets/05f12def-d0f8-4f8e-bb75-33bf0058b726)

---

## 🧱 Step 5: Build the Merge File

1. Click the **Build** tab next to the Profile tab
2. Review the **Alerts** tab — “suspicious masters” can be safely ignored

Under **Output Settings**:
- Rename the Mod Name to:

JOJ - NPC Merge

- Check both:
- ✅ Pack files into archives (recommended)
- ✅ Attempt conversion of wigs to head parts

Click **Build Anyway** in the top right.

![easynpc8](https://github.com/user-attachments/assets/1c217a88-f191-4fde-99db-6ba39e6db040)

---

## ✅ Step 6: Finalize and Organize

Once the build completes successfully, you’ll see a confirmation screen:

> “Your NPC Merge is ready at:  
> `YourDrive:\Journals of Jyggalag\mods\JOJ - NPC Merge`”

> ⚠️ The example path in the screenshot may look different — yours should show the correct location above.

![easynpc9](https://github.com/user-attachments/assets/39b34b29-7fa3-4f46-a821-8d7dfd2a805e)

---

### 📦 Post-Build Steps

1. Close EasyNPC
2. Enable the `JOJ - NPC Merge` mod in MO2
3. Refresh MO2

You will now see **5 new plugins** at the bottom of your plugin panel.

- Move them **above `JOJ - Synthesis Patch.esp`**, but keep them within the `Outputs` group
- Enable all of them

![easynpc10](https://github.com/user-attachments/assets/6e9878f9-68e0-4b08-a0e3-0bfa32aa4e7d)

---

### 🚫 Final Cleanup (IMPORTANT)

Now that your new merge is live:

- **Disable ALL mods** under the `EasyNPC` separator in MO2  
These were only needed to generate the merge — leaving them active will cause plugin conflicts, FaceGen issues, and NPC bugs.

---

## 🧾 Conclusion

You're done!

Your NPCs are now fully customized and merged into a clean, blackface-free plugin set. If you experience any NPC bugs in game, rerun all steps in this guide.

### 🔥 REMINDER – RULE 11

You chose to modify the modlist. That means:

- You are responsible for any issues this causes
- If something is broken, **re-read this guide carefully**
- I am not responsible for fixing problems introduced by your changes

---

Thanks for taking the time to customize your experience — that’s the spirit of modding. Enjoy your tailored adventure in the Journals of Jyggalag. 👑
