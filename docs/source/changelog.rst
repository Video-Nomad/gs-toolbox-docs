.. currentmodule:: <index>

#########
Changelog
#########

Version 1.1.6
^^^^^^^^^^^^^

**New Features:**

- Maya 2023 Support
- Selection Sets Boolean Logic. Middle Mouse Drag or Click with Modifiers:

  - **Shift + Ctrl** to add selection to the layer or (combine layers if dragged)
  - **Shift + Alt** to get a difference between the layer and the selection (or the difference between dragged and target layer)
  - **Ctrl + Alt** to get an intersection between the selection and the layer (or the intersection between the dragged and target layer)
  
**Improvements**

- Major improvement for Duplicate and Extract functions. They will now separate only selected faces and other detached shells will stay combined with the original object.

Version 1.1.5
^^^^^^^^^^^^^


**Improvements:**


- Duplicate Faces and Extract functions will now respect Isolate Select when used.
- Added a warning to the Array functions when it detects that the scene units are different from "cm". This is due to limitation of MASH system. MASH does not support anything other than centimeters and (since Array functionality heavily relies on MASH) neither Array function in Toolbox.

**Bug Fixes:**

- Fixed a critical bug with Fill function that caused incorrect positioning of the vertecies when scene units were different from "cm". Every scene unit is now supported by the Fill function.

Version 1.1.4
^^^^^^^^^^^^^

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
^^^^^^^^^^^^^

**Bug Fixes:**

- For Maya 2020.4 Only: Deformed arrays will now be created properly
- Fixed font issue for all versions
- Fixed some of the hotkeys

Version 1.1.2
^^^^^^^^^^^^^

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
^^^^^^^^^^^^^

**Fixed Bugs:**

- Fixed an issue with "presets" folder not being created automatically when deleted
- Fixed an issue where not initialized Maya plug-ins caused errors
- (Maya 2017) Initialization issue was fixed
- (Maya 2017) Some Array bugs fixed

**Known Issues:**

- (Maya 2017) Fill function will fail if vert selection is near another open border. Fix is to add edge loops to separate this vert from secondary open borders.

Version 1.1
^^^^^^^^^^^

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
^^^^^^^^^^^^^

**Fixed Bugs:**

- Switching scenes and workspaces will no longer cause the menu to be closed
- Switching scenes will now update material swatches correctly

**Other:**

- Changed version number format for consistency with my other plug-in(s)


Version 1.02 + 1.021
^^^^^^^^^^^^^^^^^^^^

**Improvements:**

- Back to one folder for all versions of Maya

- Minor optimizations

**Fixed Bugs:**

- No more random "Stack Trace" errors on Maya startup
- Angle Highlight will now respect custom polygon display options

Version 1.015
^^^^^^^^^^^^^

**Improvements:**

- Added full Maya 2020 Support

**Fixed Bugs:**

- Fixed some minor bugs for all Maya versions

Version 1.005
^^^^^^^^^^^^^
**Improvements:**

- Supported Maya versions now have separate plugins for better compatibility. Report bugs with Maya version attached.

**Fixed Bugs:**

- Fixed huge Shelf icons some users of Maya 2018 and 2017 have experienced
- Fixed a few minor bugs in Maya 2017 version

Version 1.004
^^^^^^^^^^^^^

**Fixed Bugs:**

- GS Toolbox was unable to initialize  ("invalid flag -t" error)

Version 1.0
^^^^^^^^^^^

- Initial Release