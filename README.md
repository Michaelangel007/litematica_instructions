Litematica Instructions
by Michaelangel007


# === Terminology ===

* Area -- the 3d volume that contains your build
* Schematic -- The blueprint of the 3d volume saved as a `.litematica` file.
* Placement -- A loaded blueprint that shows in-game where to place/remove blocks
   * Red    - block needs to be removed
   * Orange - Origin
   * Blue   - block needs to be placed


# === Hotkeys ===

/!\ If you have _Xaeo's World Map_ installed you will need to change the default _Open World Map_ key bind from `M` to something else such as `Caps Lock` via:

`Esc` > `[Options]` > `[Controls]` > `[Key Binds...]` > Xaeoro's World Map: _Open World Map_

0. I'm using these custom Litematica Hotkeys:

  * `m` (Default) to bring up Litematica menu
  * `[Configuration menu]`
  * `[Hotkeys]`
    * **Note:** You can click on the magnifying glass on the left to filter and only show a subset of commands.
  * Click on a button, press the new keybind, then press `Esc`

```
    easyPlaceToggle                    KP_8      (Default: none)
    executeOperation                   KP_9      (Default: none)
    setAreaOrigin                      END       (Default: None)
    toggleAllRendering                 KP_ENTER  (Default: M+R or BACKSLASH)
    toggleAreaSelectionBoxesRendering  DELETE    (Default: None)
    togglePlacementBoxesRendering      KP_5      (Default: LEFT)
    toggleSchematicBlockRendering      KP_1
    toggleSchematicRendering           HOME
    toggleTranslucentRendering         KP_3
```

# === New Schematic ===

1. Build your creation in Survival or Creative.

2. Make sure you have a `Stick` (yes, a wooden stick) in your inventory hotbar and selected.

3. Create new bounding box area
  * `m` to bring up Litematica menu
  * `Area Selection browser`
  * `New Selection`
  * Name it. i.e. Blaze Farm
  * Press OK
  * `Configure`
    * Change `Selection Mode: Normal` to `Simple`
    * Change `Manual Origin` to `On`
    * Name the selection again. i.e. Blaze_Farm
    * Name the Sub-region. (You can leave this blank)
    * `ESC` to return to Area Selection
  * `ESC` to return to Litematica main menu
  * `ESC` to return to Minecraft

4. Select the bounding box area
  * Mode should be `[1/9]: Area selection`.  Use `Ctrl+MouseWheel` to switch Litematica modes.
  * Move to and press `Left click` on corner1 (i.e. bottom left)
  * Move to and press `Right click` on corner2 (i.e. top right)
  * Move to and press `END` on the origin
  * You can hold `Alt`-`Mousewheel` to adjust the corners in _Corners Mods: Expand_
  * To change the active corner, _Area Editor_ > `[x] Corner 2`

Don't worry if the corners / origin aren't exact. You can fine-tune the corners/origin via the Area Editor.
  * Press `Numeric Keypad *` to bring up the _Area Editor_
  * Click on the `+/-` buttons to fine tune
       * `Left click` to add +1
       * `Right click` on subtract +1

Legend:


  | Click | Axis | Direction |
  |:------|:----:|:----------|
  | Left  |  +X  | East      |
  | Right |  -X  | West      |
  | Left  |  +Y  | Raise     |
  | Right |  -Y  | Lower     |
  | Left  |  +Z  | South     |
  | Right |  -Z  | North     |


* TIP: use `/gamemode spectator` and `/gamemode creative` to inspect the corners / origin.
* TIP: Press `DELETE` to toggle rendering of the area selection.

5. Verify blocks and bounding box is correct
  * Press `Numeric Keypad *` to bring up the _Area Editor_
  * `Analyze Area` will display a manifest of all blocks
  * Press `ESC` to return to Minecraft

6. Save the area as a schematic
  * Press `Numeric Keypad *` to bring up the _Area Editor_
  * `Save Schematic`
  * OPTIONAL: `[x] Ignore entities`
  * Name it
  * `Save Schematic`
  * `ESC` to return to Area Editor
  * `ESC` to return to Litematica main menu
  * `ESC` to return to Minecraft

NOTE: Litematica will save your `<name>.litematica` to this default location:

 * Windows: `%APPDATA%\.minecraft\schematics\`
 * macOS: `~\Library\Application Support\Minecraft\schematics\`

To goto a a folder direclty in your OS:

* On Windows press `Windows+E` to bring up Explorer, and then `Ctrl-L`
* On macOs press: `Command-shift-G`

# Place Schematic

7. Load the Schematic as a Placement
  * `m` to bring up Litematica menu
  * `Load Schematics`
  * `[x] Create a placement`
  * Click on the previously saved schematic
    * You will see stats in the right panel
  * `Load Schematic`
  * You will see a dialog box if was loaded correctly

8. Troubleshooting Placement not displaying correctly

  * If you only see a bounding box, make sure Layer Mode is All
    * Hold down `m` and press `Pageup` until you see `Layer Mode: All`
  * If you don't see the placement, or see an bounding box
    * Press `HOME` to toggle Schematic Rendering
  * To switch between translucent blue boxes and textured boxes
    * Press `Numeric Keypad 1` to toggle Schematic Block Rendering

9. Move and Rotate the Placement
  * **NOTE** `Ctrl`-`MouseWheel` to be in `Mode [2/9]: Schematic Placement`
  * Hold down `ALT` and use the scroll wheel to move the placement along the direction you are looking.
  * i.e. To move the placement down, look down, hold `ALT` and scroll the mouse wheel up.
  * To rotate the placement
    * Press `Numeric Keypad -` to bring up `_Configure Schematic Placement_
    * Click on `Rotation` to rotate
  * If `Alt+MouseWheel` changes the dimesions you are in the wrong mode.
    You need to be in `Mode [2/9]: Schematic Placement`

10. Move a Placement Fast
  * Press the `KP -` key to bring up the placement GUI.
  * Set the new origin

# Build or Print Schematic

## Printer Mode - Block by Block

11. With the placement aligned, use `Ctrl-MouseWheel` and switch to mode `[3/9]: Fill`
12. Make sure `easyPlaceMode` and `easyPlaceHoldEnabled` are on.
   To turn this on press `m` to bring up Litematica menu, `Configuration menu` > `Generic`
13. Switch OFF of the _Stick_ block.
14. Destroy blocks (left-click) and Place blocks (right-click)

## Printer Mode - Entire Structure

**NOTE:** On many servers this will PROBABLY NOT BE ALLOWED. Always check the server rules!

15. Change mode to _Paste Schematic in world_ via `Ctrl`-`MouseWheel` until you see `Mode [5/9]: Paste Schematic in world`
16. Press `Ctrl`-`m` to cycle to **Replace blocks: all** (Alternatively, you can try **non-air**)
17. To paste the ENTIRE structure you need to use the `ExecuteOperation` key  (Custom hotkey `KP_9`.)  **Note:** There is NO default key, you need to set one.

# FAQ

Q. **Verify missing blocks?**

To get a summary of missing/wrong blocks:

1. `m` to bring up Litematica menu
2. `[Schematic Placements]`
3. Click on the placement you are currently building
4. Click on the `Configure`
5. In the bottom left click on `Material List`

To see a detailed block-by-block missing/wrong blocks:

1. `m` to bring up Litematica menu
2. `[Schematic Placements]`
3. On the placement you are currently building select `[Configure]`
4. `[Schematic Verifier]`
5. `[Start verification]`
6. Click on `[Wrong Blocks]` or `[Wrong States]`
7. Press `Esc` multiple times to return to the 3D view
8. Wrong blocks will have an orange wire-frame box around them
 * To customize Configuration > Colors (AARRGGBB format)
   * schematicOverlayColorWrongBlock #4CFF3333
   * schematicOverlayColorWrongState #4CFF9010
9. When done repeat stepas 1-4 and then press `[Reset data]`

Q. **See the Manifest before you build?**

1. Load Schematics
2. Click on the schematic
3. Material List

Q. Help, **I can't place any blocks inside my placement/loaded schematic!**

A. Press `KP_8` (easyPlaceToggle)

Q. **I can't place any blocks outside my placement!**

A. Turn off:

 * **easyPlaceToggle: OFF** (`KP_8`) and
 * **togglePlacementRestriction: OFF** (`KP_5`)

Q. **I keep getting a _Action prevented by Placement Restriction Mode_ message!**

A. To turn placement restriction mode off:
   * `m` for Litematica Menu
   * `Schematic Placements`
   * `Configure`
   * `Placement:`, and turn this `OFF`

Q. The above didn't help. **I keep getting an _Action prevented by Placement Restriction Mode_**

A. You are trying to place a block that isn't in the schematic blueprint.

You need to `Left-Click` to break the existingg block, then `Right-Click` to place the planned schematic block.
Alternatively you can Unload the Placement.
