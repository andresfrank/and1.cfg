## ⛔ THIS IS NOT TESTED IN CS2 AND MAY BREAK YOUR GAME IF EXECUTED ⛔

> These configurations are provided "as is" for reference purposes onl; their behavior in CS2 is unknown.
> Feel free to look around and test commands and ideas individually, but I strongly advise against blindly executing these files.

----

## What is this?

These are all my personal settings for [Counter-Strike: Global Offensive](https://store.steampowered.com/app/730/CounterStrike_Global_Offensive/).
It includes all my configurations such as keyboard/mouse bindings, practice sandbox shortcuts, custom radiopanels, and much more!

### File Structure
Default Location: `C:\Program Files (x86)\Steam\SteamApps\common\Counter-Strike Global Offensive\csgo\cfg`

```
📁..\cfg\frank\
| frank.cfg................| 📄 Main configuration file.
| frank_help.cfg...........| ❔ Quick help.

	📁 offline\
	| demo.cfg....................| ⌨ Binds and settings for demo viewing.
	| practice.cfg................| 🛠 Full sandbox environment for offline practice.
	| practice_help.cfg...........| ❔ Quick help for the practice config.
	| surf.cfg....................| 🏄‍♀️ Quick script to enable surfing.

	📁 misc\
	| blast.cfg...................| 💥 Settings for the "BLAST Stand-Off" map.
	| graph.cfg...................| 📊 Quick script to switch to a bigger and persistent graph.
	| trollch.cfg.................| 🎯 Quick script to mess with people who can see other's crosshairs.

	📁 radiopanel\
	| radiopanel_frank.txt........| 🗣 Custom Radiopanel.
	| radiopanel_original.txt.....| 🔙 Default Radiopanel.
_____________________________________________________________________________________________________
```

## How to use

1. On GitHub, on the top right click on Code → Download ZIP
2. Navigate to the `cfg` folder inside the main installation folder of CS:GO:
`C:\Program Files (x86)\Steam\SteamApps\common\Counter-Strike Global Offensive\csgo\cfg`
3. Create a folder called `frank`
4. Extract all files there.
5. Load up CS:GO, open the console, and run `exec frank\frank.cfg`

> ⛔ **WARNING:** This will REPLACE all your settings and keybindings with mine. If you don't have your own .cfg file you won't be able to revert back to your configuration. 
> ⚠PROCEED AT YOUR OWN RISK⚠

6. To see a quick help press F1 while in-game, or open the console and execute `fhelp`.

### How to install the Custom Radiopanels

1. Navigate to `C:\Program Files (x86)\Steam\SteamApps\common\Counter-Strike Global Offensive\csgo\resource\ui`
2. Backup `radiopanel.txt`
3. Replace `radiopanel.txt` with `frank\radiopanel\radiopanel_frank.txt`


## Other Optional Changes

### Automatic Execution

How to automatically execute this config when the game starts

1. Navigate to the `cfg` folder inside the main installation folder:
`C:\Program Files (x86)\Steam\SteamApps\common\Counter-Strike Global Offensive\csgo\cfg`

2. Create a file called `autoexec.cfg`

3. Paste the following in it and save
```
exec frank/frank.cfg
```

### Game Launch Options

Set this by navigating to Steam library → Right Click CS:GO → Properties → Set Launch Options
```
-novid -language english
```

**Other options:**

* `-console`			: Starts the game with the console already opened.
* `-novid`				: The Valve intro video will not play.
* `-nojoy`				: Fully suppress Steam Input performance overhead.
* `-high`				: Start the game in high-priority mode.
* `-tickrate 128`		: Dedicated servers will be created with 128 tick, instead of the default 64.
* `-windowed`			: Forces the game to run in windowed mode.
* `-w 1920 -h 1080`		: Forces the game to run in specified resolution.
* `-noborder`			: Removes the Windows' window border.
* `-no-browser`			: Alternative to cl_disablehtmlmotd 0 as some servers block that command.
* `-language english`	: Pick the language (english, spanish, french, etc.)
* `+exec autoexec`		: Force execution of the 'autoexec' config file.

## Resources

### Useful Links
- [Valve's official documentation](https://developer.valvesoftware.com/wiki/List_of_CS:GO_Cvars)
- [Basic CFG knowledge](https://steamcommunity.com/sharedfiles/filedetails/?id=314801693)
- [Fairly comprehensive list of commands](https://steamcommunity.com/sharedfiles/filedetails/?id=1995743598&preview=true)
- [csgo-cvar-unhide](https://github.com/saul/csgo-cvar-unhide)

### Steam Cloud User Data Folder
`C:\Program Files (x86)\Steam\userdata\<YOUR_ID>\730\local\cfg`

How to find the userdata ID for your account:
1. Log in to Steam and navigate to your Inventory.
2. At the top-right click on the "Trade Offers" blue button.
5. On the right side menu click on "Who can send me Trade Offers?".
6. You will now see a trade URL that looks like this: https://steamcommunity.com/tradeoffer/new/?partner=123456&token=abcdfg
7. The number after `?partner=" is your userdata ID.


## Changelog

#### 2020-12-06
**New Operation: Broken Fang**
https://blog.counter-strike.net/index.php/2020/12/31908/

- New command: Disable voice chat until the end of the round: `bind X clutch_mode_toggle`
- New Player ping: `bind MOUSE3 player_ping`
- New Chat Wheel:
	+ `+radialradio`
	+ `+radialradio2`
	+ `+radialradio3`

#### 2020-04-19
- Formatting and Capitalization
- Removed the following alias, as it was not printing correctly, and replaced it with something more basic but more functional
```
// Activates/Deactivates voice chat and shows a message on top left corner
	alias "voice_chat" "chat_0"
	alias "chat_1" "voice_scale 0.3; echo "Damage Given VOICE_ON"; alias voice_chat chat_0"
	alias "chat_0" "voice_scale 0; echo "Damage Given" VOICE_OFF; alias voice_chat chat_1"
	bind F4 voice_chat
```

#### 2020-04-17
New Update: https://blog.counter-strike.net/index.php/2020/04/29707/

- `cl_show_observer_crosshair`: Show the crosshair of the player being observed. [0=off; 1=friends and party; 2=all]
- Added trollch.cfg to mess with people who have enabled the new command.
https://steamcommunity.com/sharedfiles/filedetails/?id=1589955838

#### 2020-03-09
- Full redesign on help menus and console logs.
- radiopanel.txt completely redone; Adjusted keybinds for compatibility

#### 2020-02-25
New Update: https://blog.counter-strike.net/index.php/2020/02/28792/

- New Commands:
	+ `cl_buywheel_nomousecentering 0/1`
	+ `cl_buywheel_nonumberpurchasing 0/1`

#### 2019-11-13
- Replaced deprecated command `cl_teamid_overhead_always "1"` with `cl_teamid_overhead_mode "2"`
- Moved `cl_teamid_overhead_maxdist` and `cl_teamid_overhead_maxdist_spec` to practice.cfg as they are sv_cheats restricted
- Removed the RALT alias for overheadid as now it can be toggled via `cl_teamid_overhead_mode`

#### 2019-10-07
New Update: https://blog.counter-strike.net/index.php/2019/10/25710/

- New command: `cl_crosshair_friendly_warning` = 0: always off, 1: only on default crosshair styles, 2: always on