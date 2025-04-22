.. currentmodule:: <index>

#########
Changelog
#########


Version 1.2.1
=============

**New Features:**

- Maya 2026 support. Please report bugs.
- Material swatches can now select polys or entire objects (Ctrl+Click or Shift+Ctrl+Click).

**Improvements:**

- Updated tooltips for material swatches with click functions.
- Automatic initialization in case of Maya version upgrade.
- Updated the pop-out input dialogs for new maya versions.

Version 1.2
=============

**New Features:**

- Added a new "spacing" field for Live Plane function. Spacing allows for more precise control of the Live Plane grid resolution.
- Live Plane Align can now align to X,Y,Z,-X,-Y,-Z axes via the new marking menu (hold RMB on Align). This will align the selected axis of the mesh to the live plane grid. Hotkeys are also available.
- No more default material for the Quick Materials. Default swatch will be either lambert1 or standardSurface1 material depending on the Maya version. gsBlankMaterial will no longer be used as a placeholder.
- Added new Array Control Window. This window holds all the array controls that were previously only available from the Channel Box.
- Linear Arrays now support multiple target curves. It will create an array on each of the target curves.
- Added additional Array controls such as Twist, Twist Deform, axis Offsets, Scale and more.
- All the windows within the plug-in are now updated to the new consistent style.
- All the controls and buttons now have a tooltip attached. Hover over any control to get a quick tooltip with hotkeys, tips and advanced functions. Tooltips can be disabled in the Options menu.
- Boolean function now has an optional "reverse selection" order toggle in the Options. Reversing the selection order will allow change which object is considered a "base" object and which objects are "cutter" objects. Either last or the first object in the selection can now be "base" object, with the rest being the "cutter" objects.

**Improvements:**

- Delete Node button label and function name was changed to Undo Edit to better describe its functionality.
- Boolean functions are now compatible with instances and multi-boolean function was optimized.
- Boolean delete function general improvements.
- Array attributes can now be controlled while selecting either mesh or the control curve (via the new Array Control Window).
- If matcap material is applied and the viewport does not have "Textured" enabled, it will be enabled automatically.
- Improvements to Snap to Poly function.
- Removed unnecessary nodes from MatCap material.
- Improved swatch rendering for Quick Materials.


**Bug Fixes:**

- Separate objects will now properly work on multiple selected meshes.
- Deleting matcap materials will no longer show an error in the script editor.
- Material swatches will now have the correct background color.
- Some python v2 compatibility improvements (for older Maya versions).
- Global Material toggle will no longer cause "Green Material" to appear on meshes that used the global material as their current material.
- Set Hidden in Outliner option fixed.
- Array hotkey was fixed.


Version 1.1.9
=============

**Bug Fixes:**

- Fixed multiple hotkeys:

  - UnCrease Plus
  - Selection: By Angle
  - Selection: Border
  - Selection: NGons
  - Selection: Hard Edges
- Other small fixes.

**Technical:**

- Decoupled the plug-in from the “version/scripts” folder for easier use of modules in studio environment. The only “hardcoded” path now is the “log.log” file path. It will be created in the same folder as before “version/scripts/gs_toolbox/log.log” for each user.

Version 1.1.8
=============

**New Features:**

- Maya 2025 Support (please report bugs).

**Improvements:**

- Old versions are now available as a download (v1.1+).
- Snap to Poly algorithm was improved.

  - Snapping multiple selected objects to multiple faces will now work as expected.
  - If the number of selected faces is bigger than the number of selected objects it will now snap everything in a repeating pattern, so all the faces are populated.

- General code improvement for maintainability.
- Hotkeys system was changed internally for better maintainability. You might need to check your hotkeys for GS Toolbox.

**Bug Fixes:**

- Fixed a rare bug with custom materials that prevented them from being created.
- Fixed a Snap to Poly bug that prevented it to be functional if only one poly is selected.
- Extract Snapshot bug was fixed.
- Several small bug fixes with regex and other boring stuff.

Version 1.1.7
=============

**New Features:**

- Maya 2024 Support

**Improvements**:

- Added new StandardSurface material in Maya 2024 as default

**Bug Fixes:**

- Fixed Array having the wrong arrangement on some Maya versions
- Fixed hotkeys for Selection Constraint and Transform Constraint
- Fixed "Save Preset" swatch generation bug in Quick Materials

Version 1.1.6
=============

**New Features:**

- Maya 2023 Support
- Selection Sets Boolean Logic. Middle Mouse Drag or Click with Modifiers:

  - **Shift + Ctrl** to add selection to the layer or (combine layers if dragged)
  - **Shift + Alt** to get a difference between the layer and the selection (or the difference between dragged and target layer)
  - **Ctrl + Alt** to get an intersection between the selection and the layer (or the intersection between the dragged and target layer)
  
**Improvements:**

- Major improvement for Duplicate and Extract functions. They will now separate only selected faces and other detached shells will stay combined with the original object.
- Added Hotkeys:

  - Create Crease Sets
  - Creases to Bevels
  - Bake Crease Sets

**Bug Fixes:**

- Fixed a bug with "Repeat Last" hotkey not working for some functions.

**Deprecation:**

- Maya 2017 Support is Dropped. It might still work just fine but there will be no bug fixes for this version.

Version 1.1.5
=============


**Improvements:**


- Duplicate Faces and Extract functions will now respect Isolate Select when used.
- Added a warning to the Array functions when it detects that the scene units are different from "cm". This is due to limitation of MASH system. MASH does not support anything other than centimeters and (since Array functionality heavily relies on MASH) neither Array function in Toolbox.

**Bug Fixes:**

- Fixed a critical bug with Fill function that caused incorrect positioning of the vertices when scene units were different from "cm". Every scene unit is now supported by the Fill function.

Version 1.1.4
=============

**New Features:**

- Added a Shift modifier for "Apply Boolean" button to keep the boolean group hidden after "Apply" button is pressed
  
  - Holding Shift will now result in an old behavior - deletion of the boolean group
  - Normal click will now result in a boolean group hidden, but not deleted

- Added an option in the options menu to store applied boolean groups in a separate group called "GS_AppliedBooleans"

**Improvements:**

- Added additional hotkeys for some Shift modified commands
- Modifier and Marking menu icons visuals were improved

**Bug Fixes:**

- Fixed position resetting of the main window after Maya is reloaded
- Bevel Plus will now work correctly on instanced objects
- Shift can now be used when setting custom hotkeys
- Some minor typos and code fixes

Version 1.1.3
=============

**Bug Fixes:**

- For Maya 2020.4 Only: Deformed arrays will now be created properly
- Fixed font issue for all versions
- Fixed some of the hotkeys

Version 1.1.2
=============

**New Features:**

- **Full Maya 2022 and Python 3 Support**! New supported versions are 2017-2022. Maya 2022 is supported in both Python 2 compatibility mode and the default Python 3 mode.
- Added **Select Hard Edges** command in **Select Edges** button marking menu (Hold RMB)

**Improvements:**

-  Added new hotkeys:

    -  Flip X,Y,Z
    -  Instance X,Y,Z 
    -  Flatten Local X,Y,Z
    -  Flatten World X,Y,Z

**Bug Fixes:**

- Arrays will no longer throw an error if the default MASH settings were changed by the user.


Version 1.1.1
=============

**Fixed Bugs:**

- Fixed an issue with "presets" folder not being created automatically when deleted
- Fixed an issue where not initialized Maya plug-ins caused errors
- (Maya 2017) Initialization issue was fixed
- (Maya 2017) Some Array bugs fixed

**Known Issues:**

- (Maya 2017) Fill function will fail if vert selection is near another open border. Fix is to add edge loops to separate this vert from secondary open borders.

Version 1.1
===========

**New Features:**

- Reworked User Interface. It will now stretch with the window, expand text to fill the buttons and more.
- Arraying System with two types of arrays, each one of them with two different modes. Select axis, add or remove objects to/from the array. Change parameters. Control with a curve. All procedural. All editable:

    - Select initial Axis.
    - Multiple objects in one array. Create procedural pipes, jewelry, laces and other repeating patterns.
    - Add or Remove objects to/from the array. Create Patterns.
    - Deformable and Non-Deformable Linear arrays.
    - Deform with a curve. Linear arrays will follow the controller curve.
    - Deformable and Non-Deformable (Uniform) Radial arrays.
    - Radial Mirroring (Radial Arrays)
    - Procedural Parameters. Change them on the fly.
    - Array randomization.
    - Quickly apply arrays to continue modeling.
    
- New Smooth Edge function. Smooth Edges and Edge Groups. Change multiplier to increase or decrease the effect.
- New Fill Hole with Quads function. Select one vert to fill the hole. Select two verts for custom patterns of quads. Works on curved and complex surfaces.
- New and Reworked Instance+ function. Now it allows to switch between two modes (Mesh and Inst) and apply modifiers to the mesh itself or to the Instance+ if needed. New button highlights.
- New Align functions for Live Plane. Align any object to live plane in one click.
- New Online Documentation is now available. It will be expanded an updated as the development continues.
- Mac OS is now supported (Beta). It should work just fine but may have some bugs. Please Report.

**Improvements:**

- Every function is fully rewritten and reworked.
- New UI will now stretch with the window and the text will expand based on the with of the buttons.
- Interactive Sliders are now much faster.
- PDF documentation is now replaced with online documentation (can still download as PDF).
- Delete Node function modifier is now inverted. Normal Click will now delete last node and Shift + Click with the node selected will delete the selected node.
- Straighten and Interpolate functions are now much faster when selecting multiple edge groups.
- Snap to Poly now has Pre-Duplication option. When enabled it will always leave behind instanced version of the snapped object(s) to allow for additional editing.
- Create Maya Material window will now open a custom window with available materials and clicking on any material will create it and automatically add it to the appropriate material slot.
- Save Preset material preview creation is now more reliable.
- Numerous small improvements of the code for reliability and stability.

**Fixed Bugs:**

- Fixed boolean transforms issue when using in conjunction with Instance+.
- Matching names should no longer cause an error on some functions.
- Numerous small bugs were fixed during a full rewrite from MEL to Python.

Version 1.0.3
=============

**Fixed Bugs:**

- Switching scenes and workspaces will no longer cause the menu to be closed
- Switching scenes will now update material swatches correctly

**Other:**

- Changed version number format for consistency with my other plug-in(s)


Version 1.02 + 1.021
====================

**Improvements:**

- Back to one folder for all versions of Maya

- Minor optimizations

**Fixed Bugs:**

- No more random "Stack Trace" errors on Maya startup
- Angle Highlight will now respect custom polygon display options

Version 1.015
=============

**Improvements:**

- Added full Maya 2020 Support

**Fixed Bugs:**

- Fixed some minor bugs for all Maya versions

Version 1.005
=============

**Improvements:**

- Supported Maya versions now have separate plugins for better compatibility. Report bugs with Maya version attached.

**Fixed Bugs:**

- Fixed huge Shelf icons some users of Maya 2018 and 2017 have experienced
- Fixed a few minor bugs in Maya 2017 version

Version 1.004
=============

**Fixed Bugs:**

- GS Toolbox was unable to initialize  ("invalid flag -t" error)

Version 1.0
===========

- Initial Release
