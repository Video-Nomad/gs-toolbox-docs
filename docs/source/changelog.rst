.. currentmodule:: <index>

#########
Changelog
#########

Version 1.1 - Major Update:
^^^^^^^^^^^^^^^^^^^^^^^^^^^

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

Version 1.0.3:
^^^^^^^^^^^^^^

**Fixed Bugs:**

- Switching scenes and workspaces will no longer cause the menu to be closed
- Switching scenes will now update material swatches correctly

**Other:**

- Changed version number format for consistency with my other plug-in(s)


Version 1.02/1.021:
^^^^^^^^^^^^^^^^^^^

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