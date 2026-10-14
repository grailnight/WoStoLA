Los Santos for Spider-Man: Web of Shadows 1.0.0
================================================

Los Santos from GTA San Andreas, in place of New York: downtown, Grove Street,
Idlewood, Ganton, Verona Beach, Santa Maria Beach, Market, Vinewood Boulevard,
Glen Park, East Los Santos. You can walk, run, climb and swing on it, and the
city's pedestrians and traffic use Los Santos streets.

This package contains NO files from GTA San Andreas or Web of Shadows. The
installer builds the map on your PC from your own copies of both games.
This build has no symbiote goo webs strung across the city.


REQUIREMENTS
------------
- Spider-Man: Web of Shadows for PC, version 1.1 (1.1.77076). The installer
  checks the EXE. A "4 GB patch" (Large Address Aware) is needed; the
  installer offers to set it and keeps a backup of the EXE.
- exWoS (the Web of Shadows mod loader by kirbystealer), installed.
- GTA San Andreas for PC, the classic version (1.0 retail or Steam). The
  Definitive Edition does not work. A gta3.img with modded MAP COLLISION
  fails the build (see TROUBLESHOOTING); texture mods only change the look.
- Python 3.10 or newer, 64-bit (python.org, "Windows installer (64-bit)").
  The installer can add the packages pillow, numpy and shapely with pip.
- About 4 GB free disk space during the build, about 250 MB afterwards.
- Recommended: WOSTweaks, to teleport to Los Santos (preset "Los Santos").
- Optional: WoS Graphics (deferred renderer): then Los Santos buildings cast
  sun shadows.


INSTALL
-------
1. Extract the archive INTO the Web of Shadows folder (next to
   "Spider-Man Web of Shadows.exe").
2. Close the game. Double-click "Los Santos - Install.cmd".
3. Pick your GTA San Andreas folder when asked. The build takes about
   5-10 minutes and needs a few GB of memory.
4. At the end you get "Done." The map is in exWoS\SA_ls_full.


PLAY
----
1. Start the game with "Los Santos - Play.cmd". A normal launch stays New York.
2. Load a save.
3. Teleport with WOSTweaks to the preset "Los Santos" (the installer adds it
   when WOSTweaks is present). New York is hidden, so a save that starts far
   from Los Santos stands over empty water.
"Los Santos - Play.cmd" turns SA_ls_full on in exWoS.config.ini for that
session only and turns it back off when the game closes. Other exWoS mods that
replace the same files are switched off for that session too (they are listed
in WoS_LosSantos\bin\play.log). If the PC crashes or loses power during the
session, the next start of any "Los Santos - *.cmd" puts the settings back.


WHAT TO EXPECT
--------------
- New York's buildings, streets and trees are hidden and have no collision;
  its cars and people stay.
- The map covers the area listed above. The hills north of Vinewood are cut off.
- No traffic lights. Some San Andreas objects (trees, a few props) have no
  collision, as in San Andreas' own data.
- Story missions and New York landmarks are not adapted.


REMOVE
------
"Los Santos - Uninstall.cmd" deletes exWoS\SA_ls_full and its config line.
Then delete WoS_LosSantos and the three "Los Santos - *.cmd" files.
Backups (the EXE before the LAA flag, exWoS.config.ini) are kept in
WoS_LosSantos\backup.


TROUBLESHOOTING
---------------
- "collision ... does not match": your gta3.img has modded collision files.
  Build from an unmodded San Andreas (a second clean copy works too).
- "Cannot write to ...": the game is under Program Files. Run
  "Los Santos - Install.cmd" as administrator, or move the game.
- "The map loader did not start": the game is closed again at once, so it
  never runs with half of the map. See WoS_LosSantos\bin\collision_loader.log
  and play.log.
- The map is invisible: in collision_loader.log, look for WORLD_LOADED and
  WORLD_PULSE lines.
- Crashes after a while: the EXE must be Large Address Aware. The installer
  sets it; if you replaced the EXE later, set it again (or run the installer).


Author: grailnight. GTA San Andreas (c) Rockstar Games; Spider-Man: Web of
Shadows (c) Activision / Marvel. This mod includes none of their files.
