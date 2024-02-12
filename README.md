## What is this?

These are all my personal settings for [Counter-Strike 2](https://store.steampowered.com/app/730/CounterStrike_2/).
It includes all my configurations such as keyboard/mouse bindings, practice shortcuts, and more!

## How to use

1. On GitHub, on the top right click on Code → Download ZIP
2. Navigate to the `cfg` folder inside the main installation folder of CS2:
`C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg`
3. Extract the ZIP file.
4. Rename the folder from `and1.cfg-main` to `frank`.

> ⛔ **STOP:** The next step will REPLACE all your settings and keybindings with mine. If you don't have your own .cfg file you won't be able to easily revert back to your configuration.
> 
> ⚠PROCEED AT YOUR OWN RISK⚠

5. Load up CS2, open the console, and run `exec frank\and1.cfg`
6. To see a quick help press F1 while in-game (doesn't work in the main menu), or open the console and execute `ahelp`.

### File Structure

```
📁...\cfg\frank\
| and1.cfg....................| 📄 Main configuration file.
| and1.help.cfg...............| ❔ Quick help with most common binds.
| practice.cfg................| 🛠 Sandbox environment for offline practice.
| practice.help.cfg...........| ❔ Quick help for the practice config.
| csgo backup\................| 🗄 My old CS:GO config. UNTESTED IN CS2.
_________________________________________________________________________________
```

### Automatic Execution

How to automatically execute this config when the game starts.

1. Navigate to the `cfg` folder inside the main installation folder:
`C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg`

2. Create a file called `autoexec.cfg`

3. Paste the following in it and save
```
exec frank/and1.cfg
```

## Resources

### Useful Links
- [Valve's official list of CS2 console commands and variables](https://developer.valvesoftware.com/wiki/List_of_Counter-Strike_2_console_commands_and_variables)
- [Starting guide to learn the basics of CS configs](https://steamcommunity.com/sharedfiles/filedetails/?id=314801693)
- [Tool for tracking your match statistics](https://csstats.gg/)
- [Skins & Market info](https://csgostash.com/)

### PLAY Command

The `play` command allows you to play pretty much all available sounds in game, for example: `play ambient/animal/bird1`. Needless to say, only you will hear them.
This is useful for adding auditory feedback to your commands, for example: `toggle sv_showimpacts; play ui/beepclear`

**How to find the sound files**

1. Download this tool: [Source 2 Viewer](https://valveresourceformat.github.io/)
2. Open this file: `C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\pak01_dir.vpk`
3. See the `sounds` folder.

**Full list of CS2 Sounds**

As of 2024-02-12, there are 18.880 files and 244 folders, weighing 4.17GB.
I've listed the entire file structure (names only) here: [./cs2_sounds.txt](./cs2_sounds.txt)

If you want the actual audio files, you could try to use the same tool to extract and decompile the `.vsnd_c` files into `.mp3` or other format.
