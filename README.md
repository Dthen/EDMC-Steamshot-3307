# EDMC-Steamshot-3307
This plugin's config doesn't work.
A plugin for EDMC which detects an uncompressed screenshot from Steam, renames it with relevant information, and retains EDFX / Reshade effects.
My attempt to learn how EDMC plugins work by reviving something which didn't work when I tried to use it.

The plugin takes a screenshot file created by Steam and generates a new name based on current star system and stellar body while retaining EDFX / Reshade information. 
The converted file can be saved to a different directory from the original file. The original file can optionally be deleted. 

# Prerequisites
1. Steam-Overlay must be enabled for screenshots to be taken.
2. If having trouble with Steam-Overlay not working with EDFX / Reshade activated. Follow the steps below:
	* In EDFX, head to the FX Compatibility mode tab
	* Under Compatibility mode select `Mode 2 (dxgi.dll)`. Steam-Overlay should now be enabled with EDFX / Reshade effects intact. 
3. In Steam, go to `Settings -> In-Game`
	* Ensure `Save an uncompressed copy` is enabled 
	* Choose the desired folder in which you would like the original screenshot to be saved by pressing the `Screenshot folder` button below. This folders path will be the `Screenshot Directory` in EDMC.

# Installation

Download the [latest release](https://github.com/dylanfrankcom/EDMC-Steamshot/releases/latest), open the archive (zip) and extract the folder to your EDMC plugin folder.

* Windows: `%LOCALAPPDATA%\EDMarketConnector\plugins` (usually `C:\Users\username\AppData\Local\EDMarketConnector\plugins`).
* Mac: `~/Library/Application Support/EDMarketConnector/plugins` (in Finder hold ⌥ and choose Go &rarr; Library to open your `~/Library` folder).
* Linux: `$XDG_DATA_HOME/EDMarketConnector/plugins`, or `~/.local/share/EDMarketConnector/plugins` if `$XDG_DATA_HOME` is unset.

Relaunch EDMC to initiate the plugin.

## Configuration
**THIS IS CURRENTLY BROKEN**

**On my PC the plugin will create a copy of the screenshot in the foilder I have set Steam to save screenshots to, and rename it correctly, but I have no idea how it knows, as the configuration to tell it is broken and I don't use the default steam location.**

Go to `File/Settings -> Steamshot` and put in: 
* the directory where Steam saves uncompressed screenshots
* the directory where you want the converted screenshots to go
* Choose whether to delete the original file


### Credit
EDMC-Steamshot-3307 is a fork of [dylanfrankcom]'s EDMC-Steamshot which is a fork of [NoFoolLikeOne's](https://github.com/NoFoolLikeOne) [EDMC-Screenshot](https://github.com/NoFoolLikeOne/EDMC-Screenshot) plugin, without which this plugin would not be possible. This plugin differs from its parent as it renames and relocates an uncompressed png file created by Steam while retaining EDFX / Reshade effects. 

This fork is an attmept to make the plugin work properly again in the year 3307 (2021) with my amateurish understanding of code.
