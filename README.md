# SVG Coasters

This project includes FreeCAD macros that can be used to import an SVG into FreeCAD as a sketch and then use that sketch to create a 3D-printable inlay. A coaster template is included but it will work for anything.

## Usage:
1. Open SVG_Coasters.FCStd
  1. This project has a VarSet defining several parameters
2. Select the top face of the coaster, then run the Import_SVG_To_Face.FCMacro macro.
3. Then double-click the SVG_Sketch object in the Model window to modify the sketch
4. Use the Move, Rotate, and Scale to adjust the sketch location and size (probably in the center of the coaster). Save the sketch
5. Select the SVG_Sketch object again, then run the Make_Inlay.FCMacro macro.
6. A window will ask for the inlay depth and tolerance.
7. 3D print and place a beverage on top.