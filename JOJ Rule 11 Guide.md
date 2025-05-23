
# Journals of Jyggalag
# A Prepper’s Guide to Rule-11

---

Written by Crusader of Order - **Aaronavich**

Edits and additions by fellow Crusaders and Arbiters - **Rauty79**, **Guurzak**, **Juntii**, and **BackBeatN**

---

### So, you want to introduce a little chaos to order?
### Read on…

---

# Preparing MO2

We all love a bit of chaos, but we can easily introduce a bit too much and end up with no way to go back to the safety of order.

Follow these steps to protect JOJ and make sure all is reversible!

## Create a custom JOJ Profile in Mod Organizer 2

1. Click the profile drop down menu at the top of the left pane and select ‘Manage’

![image](https://github.com/user-attachments/assets/0b537ce6-eb1a-4cdd-bd7e-9065d8103b7c)

2. In the pop-up window select Journals of Jyggalag (or whatever version of JOJ you are using)
3. Select copy
4. Name your new profile ‘JOJ Custom’ or something else
5. Click select, close the profiles window.

![image](https://github.com/user-attachments/assets/26d7699c-3fd1-471f-b835-bb273f4585d8)

#### *** Make sure your custom profile is now selected in MO2! ***

---

# Make your own Output folders

When we add or remove mods from JOJ, tools like synthesis, Pandora and BodySlide may need to be re-run. We don’t want to overwrite the original output or we won’t be able to restore order!

1. Scroll to the bottom of the left pane in MO2 and right click the ‘Not yet Installed separator
2. Hover over All Mods
3. Create Empty Mod Inside and name it ‘Custom BodySlide Output’

![image](https://github.com/user-attachments/assets/acea7ed5-3f1e-43dd-bffc-54d0f6af9596)

4. Create new mods for all the output folders shown below

![image](https://github.com/user-attachments/assets/4f27c5c2-2308-4ac1-b0bb-f2c771fc480e)

5. Expand the ‘Outputs’ separator and move each folder directly below the original of the same name and activate

![image](https://github.com/user-attachments/assets/62ef8cae-f048-4a5c-a511-1660bc33f1bf)

---

# Link the tools to your custom output Mods

By default, all the tools are set to output to the original output mods or to the overwrite section
We need to change the path to our new ones.

![image](https://github.com/user-attachments/assets/94b8903e-1d6e-4948-bb84-288daaa00c4e)

1. Click the gears icon at the top of MO2, this will open the executables window.

![image](https://github.com/user-attachments/assets/0819959c-a2e2-4e09-a6dd-9a2dcb0f3f99)

2. Select the BodySlide tool on the left pane
3. Tick the box next to ‘Create files in mod instead of overwrite
4. Select ‘Custom - BodySlide Output’
5. Click apply.

*** Some of the empty mod folders you have made do not have corresponding tools.
The main ones you need to set the path for are: BodySlide, Pandora, Synthesis & Easy NPC. ***

6. Close the executables window and run BodySlide.

![image](https://github.com/user-attachments/assets/52eb68bb-255c-4f59-bd47-0b44cd2075ca)

7. Open settings

![image](https://github.com/user-attachments/assets/8a440fae-ecd8-475b-8138-7ba9ad9efea4)

8. Expand ‘advanced’, locate ‘Output path’, click Browse and select ‘Custom – BodySlide Output’. Close Bodyslide.

![image](https://github.com/user-attachments/assets/f5db7576-580a-4fc8-aa6c-6a7a0b45d43f)

9. Lastly, reorder the columns in MO2’s left pane: Mod name > Priority > Conflicts.

This will help later on.

![image](https://github.com/user-attachments/assets/5073cfc2-8626-45d1-aa3e-cc982c2db04c)


### Congratulations! You have now completed the basic prep BUT we are not safe without following some rules when we introduce chaos.

---

# Re-installing / Editing Mods

You may want to re-install a mod to pick different FOMOD options. Creating a new profile does not protect the mods from being overwritten.

#### Follow the rules below

1. Right click the mod and choose reinstall mod.

2. If the mod does not have install options (FOMOD), you will be greeted with the ‘quick install’ pop-up.

![image](https://github.com/user-attachments/assets/b35c6456-84da-4716-9036-b6fa8685b675)

3. Rename the mod by adding the prefix ‘Custom’

4. If the mod you are reinstalling does have a FOMOD, before choosing new options, select the name field and rename the mod by adding the prefix ‘Custom’ so that it doesn’t overwrite the original.

![image](https://github.com/user-attachments/assets/d4559032-5fac-475e-bcfa-45acc64c5927)

Go ahead and change your options.

#### Never merge or overwrite the original! There are exactly 0 good reasons to do this!

5. Once renamed and installed, locate the original version of the mod and make a note of the priority number in the second column of the left pane.

![image](https://github.com/user-attachments/assets/5abaa118-3444-4f00-b2ac-f478e025dad7)

6. Now locate your renamed version at the bottom of MO2 and set it’s priority so that it will sit directly below the original.

![image](https://github.com/user-attachments/assets/1d7246b5-1d61-45c7-bbd4-980f0e786fd4)

**Warning** - Do not use the filter box in the left pane and/or drag mods up through your mod list, you are highly likely to make a mistake this way!

7. Once in place, activate your new mod BEFORE deactivating the original, this will ensure that the plugin load order is preserved!

![image](https://github.com/user-attachments/assets/517f2c15-8c0c-46f0-b30c-6751ac5aa6f5)

8. De-activate the original and leave it in place.

#### Note: Always check the bottom of the right pane (Plugins tab) in MO2 and check if any new plugins got added by your re-install options, if there are and you weren’t expecting this then I strongly recommend you consider the changes you’ve made carefully.

---

# Adding New mods

This section is a bit more involved but will only cover generically applicable rules for all additions you might want to make.

A 10-page guide could be written for this section alone, so this is not exhaustive and won’t go into what types of mods are safe to add and what aren’t.

You can ask in Rule 11 chat and maybe a kind Crusader or Arbiter will give you a steer.

### Some Simple Rules to help keep you right

1. Use the search function in discord! Someone may have already added the mod you want and there may be useful info to digest before proceeding!

![image](https://github.com/user-attachments/assets/71200222-ad44-4417-a906-346b86a339e6)

2. Create a new separator at the bottom the left pane of MO2 and name it ‘Newly added’. You can do this by clicking the (small) wrench and screwdriver icon where we went to refresh MO2 earlier in this guide.

![image](https://github.com/user-attachments/assets/e6a75942-284a-4158-bd8d-c5ef74e6455d)
![image](https://github.com/user-attachments/assets/2e3c582c-a71a-4ab5-a144-cfa8d5ee1f4a)

3. Read the Mod Page! Check requirements, find compatibility sections and read them carefully! Check for pins in the comments section. Make sure as best you can, that the mod you want to add is compatible with  JOJ.

![image](https://github.com/user-attachments/assets/a8f9a677-ee3b-4e74-93e4-0aae0568bc26)

4. Check the ‘bugs’ section! If a mod has hundreds of bug reports, it is a good bet that it has problems. However, many excellent mods have no bugs and yet still get reports because… ‘humans with computers’. Exercise your grey matter!

5. Once you’ve downloaded and installed your mod, activate it but don’t move it yet!

![image](https://github.com/user-attachments/assets/e2d4d2a3-547b-438c-9812-2e59720ea03b)

6. Double click the mod and look at the file tree. Make note of what you see.. Does it have a plugin? Is it structured correctly??

![image](https://github.com/user-attachments/assets/f721505f-a4f3-45b3-8bb3-f158974e38b7)

7. Navigate to the conflicts tab in the same pop-up window. There are three sections here, familiarise yourself with them and make a note of what files your new mod is overwriting (if any). It may also be getting overwritten if your new mod contains BSA files (loose files always overwrite BSA’s)

![image](https://github.com/user-attachments/assets/16299e4c-789f-473c-b316-b8b69bd7ebac)

8. Now you need to engage your grey matter a bit more, are the files your mod is overwriting what you were expecting it to? We need to figure out where to place your new mod and if it is even compatible!

9. If you’ve decided to keep the mod, then in general, I strongly recommend creating your own separators for all your additions even if they would logically belong in one of the original separators.

10. You’ll have to use discernment here to decide where to place it or ask in rule 11 chat if you’re unsure!

11. Select a standout colour for your separators by rick clicking it > select colour. This will make it easier to find any mods you’ve added in the future.

![image](https://github.com/user-attachments/assets/fe6cefa7-d44a-400c-973e-46d484fadc2a)

12. If your new mod contains a plugin/s then you must always run synthesis again unless you really know what you’re doing (but then you wouldn’t be reading this guide!) so just do it.

---

# Plugin Placement

Some may disagree with this, but I strongly recommend that you Do Not Run Loot to sort your added plugins! Hand place your mod additions yourself instead!

There are really no shortcuts here, if you want to be sure where your added plugins should go then you’ll need to learn to view conflicts in xEdit, but if you aren’t inclined to put the time in then use common sense and position the plugin similarly to where you’ve positioned the mod folder in the left pane.

#### There is so much more to cover here but the scope of this guide is limited so I’ll leave it there. To learn more, consult your friend- the interwebs.




# What tools should I re-run when installing new mods?

*** Non-exhaustive! Use common sense! ***

#### Official JOJ GitHub Guide on re-running Tools:


#### Bodyslide
Armour / Clothing / equipment / hair / ‘attachment’ mods

#### Pandora
Anything that adds or changes animations. (OAR / DAR animations usually don’t require it but it only takes a couple of minutes so just do it anyway and save yourself an occasional reboot!

#### Synthesis
Anytime you add/remove/replace a mod that contains a plugin

#### EasyNPC

Anytime you add/remove/replace or make changes to NPC replacer mods


#### XLODGen / TexGen / DynDOLOD
Mods that add or remove stuff to the exterior world space (Check in Xedit)
Town or city overhauls
New player homes or buildings in general
Added world spaces from DLC sized mods

#### ParallaxGen
Armour / Clothing / Equipment
Environmental textures- town overalls etc
If you are re-running DynDOLOD, probably re-run this


### Note:
Before re-running a tool it is best practice to deactivate the output mod folders of tools that are run afterwards (reference the mod load order in the outputs section of the left pane). Usually it is sensible to delete the contents of the output folder for the tool you are about to re-run beforehand.

#### ***Ensure that the tool is set to output to YOUR output folder and not the original JOJ Output***

#### Caution:
When you reactivate DynDOLOD output, the plugins will be in reverse order. Ensure Occlusion.esp is below DynDOLOD.esp at the bottom of your load order.





# A Warning about disabling Mods

In general, just don’t disable mods, if there is something you want to remove from your game then ask for help from a Crusader or Arbiter


Where possible, always use MCM settings to disable mods instead of removing /disabling in MO2!



#### That concludes this guide, much of the above falls under ‘best practice’ not all of it is strictly necessary but it takes experience to know when it is safe to ignore something so do yourself a favour while you gain experience and follow the rules!





# Appendix

### The Following are links to useful tutorials and guides to advance your modding prowess

Reading Crash Logs


#### xEdit - How to check for conflicts between mods


xEdit - Simple Conflict Resolution


Walkthrough of Conflict Resolution and 3D Space Patching


Bodyslide Quick Start Guide


Outfit Studio Tutorial Series


Creation Kit Basics


A TLDR on Immersive Equipment Displays










Happy Rule 11 Modding,

Aaronavich & the JOJ Support Team








