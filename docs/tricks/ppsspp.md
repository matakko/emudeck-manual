# <img src="/assets/emulators/ppsspp.png" alt="EmuDeck guide" width="80" style="vertical-align: middle"> PPSSPP Tips and Tricks

[TOC]

---

### How to Install Custom Textures



**Preface**

The PPSSPP Flatpak (installed by EmuDeck) does not use a named Memstick folder to manage its contents. Instead, the Memstick folder is located here: `/home/deck/.var/app/org.ppsspp.PPSSPP/config/ppsspp/PSP`.

---

**Texture Pack Sources**

_This list is not exhaustive_

- [https://forums.ppsspp.org/forumdisplay.php?fid=36](https://forums.ppsspp.org/forumdisplay.php?fid=36)

---

**How to Install Custom Textures**

1. In Desktop Mode, open PPSSPP, click the `Games` tab, click the `Gear` icon, Toggle `Show ID`.
   - ![How to Install Custom Textures: PPSSPP-1](../../assets/ppsspp-how-to-install-custom-textures-1.png)
2. Click the "three lines" icon to the left of the `Gear` icon. Note down the Game ID to the right of your game
   - ![How to Install Custom Textures: PPSSPP-2](../../assets/ppsspp-how-to-install-custom-textures-2.png)
3. In PPSSPP, click the `Settings` button, click the `Tools` tab,, click `Developer tools`, check `Replace textures`
   - This option is enabled by default but if texture packs are not loading properly, you may want to double check that this setting is enabled
4. In Desktop Mode, open the `/home/deck/.var/app/org.ppsspp.PPSSPP/config/ppsspp/PSP/` folder
   - `~/.var` is a hidden folder by default, click the `Hamburger` menu in the top right of the file explorer, click `Show Hidden Files`
5. If one does not exist already, create a `TEXTURES` folder here, casing matters
6. In the `TEXTURES` folder, create a folder matching your Game ID
   - Using Grand Theft Auto: Chinatown Wars as an example:
     - ![How to Install Custom Textures: PPSSPP-2](../../assets/ppsspp-how-to-install-custom-textures-3.png)
7. Place your texture folders and files directly in the newly created GAME ID folder
   - Using Grand Theft Auto: Chinatown Wars as an example:
     - ![How to Install Custom Textures: PPSSPP-4](../../assets/ppsspp-how-to-install-custom-textures-4.png)
8. Your texture pack will now be installed

---

### How to Install Custom Shaders

**Preface**

The PPSSPP Flatpak (installed by EmuDeck) does not use a named Memstick folder to manage its contents. Instead, the Memstick folder is located here: `/home/deck/.var/app/org.ppsspp.PPSSPP/config/ppsspp/PSP`.

---

**Shader Sources**

_This list is not exhaustive_

- [https://forums.ppsspp.org/showthread.php?tid=6594](https://forums.ppsspp.org/showthread.php?tid=6594)
- [https://forums.ppsspp.org/showthread.php?tid=6594&pid=55390#pid55390](https://forums.ppsspp.org/showthread.php?tid=6594&pid=55390#pid55390)
- [https://forums.ppsspp.org/showthread.php?tid=6594&pid=124441#pid124441](https://forums.ppsspp.org/showthread.php?tid=6594&pid=124441#pid124441)
- [https://forums.ppsspp.org/showthread.php?tid=6594&pid=54841#pid54841](https://forums.ppsspp.org/showthread.php?tid=6594&pid=54841#pid54841)
- [https://forums.ppsspp.org/showthread.php?tid=6594&pid=112250#pid112250](https://forums.ppsspp.org/showthread.php?tid=6594&pid=112250#pid112250)
- [https://buildbot.libretro.com/assets/system/](https://buildbot.libretro.com/assets/system/)
  - Download `PPSSPP.zip` and use the contents of the `shaders` folder in the extracted `PPSSPP.zip` folder

---

#### How to Install Custom Shaders

1. In Desktop Mode, open the `/home/deck/.var/app/org.ppsspp.PPSSPP/config/ppsspp/PSP/` folder
   - {{ hiddenfolders }}
2. If one does not exist already, create a `shaders` folder here, casing matters
   - `Shaders` or `SHADERS` **will not** work, it must be named `shaders`
3. In the `shaders` folder, place your custom shader files
4. To enable the new custom shaders, open PPSSPP, click `Settings`, click the `Graphics` tab on the left, click `Display layout & effects`, click the `+` button under `Postprocessing shaders` and select your preferred custom shader

#### How to Create Custom Shader INI Files

Typically, the shader packs linked above will include a master INI file which will contain a set of good defaults that expand the repository of shaders you can use in PPSSPP. However, you can create custom INI files to mix and match shaders. This section will cover how to do that.

1.  Right click anywhere in the `shaders` folder, click `Create New > Text File`
2.  Name the newly created text file matching your shader file or something descriptive (For example `CRT-Bloom.ini`)
3.  Right click the newly created text file, click `Open with Kate` or a text editor of your choice
4.  Use the following format:

        [SHADERNAME]
        Name=SHADERNAME
        Fragment=SHADER.FSH
        Vertex=VERTEX.FSH

5.  For example:

        [CRT-Bloom]
        Name=CRT-Bloom
        Fragment=crt.fsh
        Vertex=aa2obl.vsh

6.  Your custom shader will now be created. To enable it, open PPSSPP, click `Settings`, click the `Graphics` tab on the left, click `Display layout & effects`, click the `+` button under `Postprocessing shaders` and select your newly created custom shader

---

### How to Use Cheats



**Preface**

The PPSSPP Flatpak (installed by EmuDeck) does not use a named Memstick folder to manage its contents. Instead, the Memstick folder is located here: `/home/deck/.var/app/org.ppsspp.PPSSPP/config/ppsspp/PSP`.

---

**Cheat Sources**

_This list is not exhaustive_

- [https://forums.ppsspp.org/showthread.php?tid=11961](https://forums.ppsspp.org/showthread.php?tid=11961)
- [https://forums.ppsspp.org/showthread.php?tid=22800](https://forums.ppsspp.org/showthread.php?tid=22800)

---

#### How to Use a cheats.db File

1. In Desktop Mode, open `/home/deck/.var/app/org.ppsspp.PPSSPP/config/ppsspp/PSP/`
   1. `~/.var` is an invisible folder by default, click the `Hamburger` menu in the top right of the file explorer, click `Show Hidden Files`
2. Create a `Cheats` folder here, casing matters
   1. If one exists, skip this step
3. Place a `cheat.db` file in this folder
   1. <img src="https://user-images.githubusercontent.com/108900299/214385915-9016e2ca-02fd-4e20-9331-5ff9d4e632da.png" height="300">
4. Open PPSSPP, click `Settings`, select `System`, scroll down and check `Enable cheats`
   1. <img src="https://user-images.githubusercontent.com/108900299/214386240-5cc0309c-dd93-43a3-a14e-a38e1ff210f6.png" height="300">
5. In Game Mode, open a game and either press the `Escape Key` hotkey: `Steam` + `DPad Left` or use the `PPSSPP Steam Input Profile` to open the Quick Menu
   1. [Global Hotkeys](../../controls-and-hotkeys/steamos/hotkeys.md#global)
   2. [PPSSPP Hotkeys](#ppsspp-hotkeys)
   3. <img src="https://user-images.githubusercontent.com/108900299/214387780-baab0bf4-2ed8-4632-9a46-091faccb5900.png" height="300">
6. Select `Import from cheat.db`, and check the cheat(s) you would like to enable
   1. <img src="https://user-images.githubusercontent.com/108900299/214387170-31a93120-5b6f-47e0-ade8-b5078676530f.png" height="300">
7. Return to game and your cheat(s) should now be enabled

---

#### How to use Cheat Codes

1. In Desktop Mode, open `/home/deck/.var/app/org.ppsspp.PPSSPP/config/ppsspp/PSP/`
   1. `~/.var` is an invisible folder by default, click the `Hamburger` menu in the top right of the file explorer, click `Show Hidden Files`
2. Create a `Cheats` folder here, casing matters
   1. If one exists, skip this step
3. Locate your Game ID
   1. To find your Game ID, open PPSSPP, click the `Games` tab, click the `Gear` icon, Toggle `Show ID`
   2. <img src="https://user-images.githubusercontent.com/108900299/210125694-441118ba-2f32-4843-bc7f-48def75e9b09.png" height="300">
   3. Note down the Game ID to the right of your game
4. In the `Cheats` folder, create a file matching your Game ID with an `.ini` file extension
   1. Skip this step if an `.ini` file already exists matching your Game ID
   2. Example (Using Grand Theft Auto: Liberty City Stories - `ULUS10160.ini`): <img src="https://user-images.githubusercontent.com/108900299/214389912-556cf061-e426-4384-8a7a-6d048e603a49.png" height="300">
5. Open the `.ini` file and add your cheat to the bottom of the file
   1. Example (Using a 60 FPS cheat for Grand Theft Auto: Liberty City Stories): <img src="https://user-images.githubusercontent.com/108900299/214389761-989b1891-25c9-408f-9ccd-e8b6f4df4ab3.png" height="300">
6. Save and close out of the `.ini` file
7. In Game Mode, open a game and either press the `Escape Key` hotkey: `Steam` + `DPad Left` or use the `PPSSPP Steam Input Profile` to open the Quick Menu
   1. [Global Hotkeys](../../controls-and-hotkeys/steamos/hotkeys.md#global)
   2. [PPSSPP Hotkeys](#ppsspp-hotkeys)
   3. <img src="https://user-images.githubusercontent.com/108900299/214387780-baab0bf4-2ed8-4632-9a46-091faccb5900.png" height="300">
8. Select `Cheats` on the right
9. scroll down the list of cheats and enable the cheat(s) you added to the `.ini` file
   1. <img src="https://user-images.githubusercontent.com/108900299/214390274-8832ce4e-50d9-4844-8d39-35f1d233a4c6.png" height="300">
10. Return to game and your cheat(s) should now be enabled

---

### How to Roll Back PPSSPP to an Older Version



If you do not have access to a mouse and keyboard for the below section, use `L2` to right click and `R2` to left click. Alternatively, remote into your Steam Deck using one of the methods found in the FAQ, [How do I remotely control my Steam Deck?](../../frequently-asked-questions/steamos/index.md#how-do-i-remotely-control-my-steam-deck).

1. In Desktop Mode, open `Konsole`
2. To see a list of prior versions of the emulator, type:
   - `flatpak remote-info --log flathub org.ppsspp.PPSSPP`
3. If Konsole prompts you to select `system` or `user`, enter `2` to select `user`
4. Konsole will list a list of previous versions for the flatpak. The important line for each version is the `Commit: ` line. The `Commit: ` line will have a long accompanying alphanumeric string (the “commit” code). Copy the string for the version you want to downgrade to.
   - Using Citra as an example:
     - ![How to Roll Back Flatpaks: 1](../../assets/how-to-roll-back-flatpaks-1.png)
5. To downgrade to the version you want:
   - `flatpak update --commit=put_commit_code_here org.ppsspp.PPSSPP`
   - Replace `put_commit_code_here` with the actual code you located in Step 2.
     - Using Citra as an example:
       - ![How to Roll Back Flatpaks: 2](../../assets/how-to-roll-back-flatpaks-2.png)

If the above steps did not work and you are getting an error message along the lines of `Flatpak not installed`, your Flatpak is likely installed at the system level instead. Select one of the below solutions:

Solution 1: Open the EmuDeck application, click the `Manage Emulators` page, select the emulator in question, and click `Reinstall / Update`.

Solution 2: Add `sudo` in front of the commands written in Step 2 and Step 5. In Step 2, write `sudo flatpak remote-info --log flathub org.ppsspp.PPSSPP` and in Step 5, write `sudo flatpak update --commit=put_commit_code_here org.ppsspp.PPSSPP`.

---

### How to Use the Original PSP Font



Legally, PPSSPP cannot use the original PPSSPP font and instead uses an open source font, "Roboto-Condensed". However, switching to the original PPSSPP font is easy.

Before proceeding with the below steps, dump the original font from a PSP. You can find the font in the `flash0/font` folder.

1. Open the `/home/deck/.var/app/org.ppsspp.PPSSPP/config/ppsspp/PSP` folder
   - `~/.var` is a hidden folder by default, click the `Hamburger` menu in the top right of the file explorer, click `Show Hidden Files`
2. Create a `flash0` folder in `/home/deck/.var/app/org.ppsspp.PPSSPP/config/ppsspp/PSP`
3. Create a `font` folder in `/home/deck/.var/app/org.ppsspp.PPSSPP/config/ppsspp/PSP/flash0`
4. Place your fonts in `/home/deck/.var/app/org.ppsspp.PPSSPP/config/ppsspp/PSP/flash0/font`
5. Your fonts are now installed

---

### How to Configure Language Settings



#### UI

1. In Desktop Mode, open PPSSPP
2. On the right, click `Settings`
3. Click the `System` tab
4. To the right of `Language`, select your preferred language in the drop-down menu

#### In-Game

1. In Desktop Mode, open the `/home/deck/.var/app/org.ppsspp.PPSSPP/config/ppsspp/PSP/SYSTEM` folder
2. Right click `ppsspp.ini` and click `Open with Kate` or a text editor of your choice
3. Under the `[SystemParam]` section, locate `Language = 1`
4. Replace `1` with your preferred language:
   - JAPANESE 0
   - ENGLISH 1
   - FRENCH 2
   - SPANISH 3
   - GERMAN 4
   - ITALIAN 5
   - DUTCH 6
   - PORTUGUESE 7
   - RUSSIAN 8
   - KOREAN 9
   - CHINESE_TRADITIONAL 10
   - CHINESE_SIMPLIFIED 11
5. Save and exit out of the text file

---
