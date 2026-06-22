# SVG Coasters

This project includes FreeCAD macros that can be used to import an SVG into FreeCAD as a sketch and then use that sketch to create a 3D-printable inlay. A coaster template is included but it will work for anything.

Note: The MakeInlay script will NOT work with SVGs that have B-Splines. See below for conversion to straight lines.

## Usage:
1. Open SVG_Coasters.FCStd
  1. This project has a VarSet defining several parameters
2. Select the top face of the coaster, then run the Import_SVG_To_Face.FCMacro macro.
3. Then double-click the SVG_Sketch object in the Model window to modify the sketch
4. Use the Move, Rotate, and Scale to adjust the sketch location and size (probably in the center of the coaster). Save the sketch
5. Select the SVG_Sketch object again, then run the Make_Inlay.FCMacro macro.
6. A window will ask for the inlay depth and tolerance.
7. 3D print and place a beverage on top.

To import an SVG manually (without the macro)
1. Drag and drop the SVG into the design and select _Import as Geometry_
2. Select all objects that are created and go to the Draft workbench. Choose Make Sketch to create the sketch. Delete the original objects.
3. If multiple sketches are created, select all the sketches and in the Sketcher workbench use the Sketch->Merge Sketches tool. Delete original sketches
4. Drag and drop the new sketch into the Coaster body part in the tree view.
5. Select the top face of the coaster body and do Sketch->Attach Sketch. Select the sketch, and choose to attach it to the face.

## Inkscape SVG Creation from B/W Image
1. New document
2. Import B/W PNG
3. Path->Trace Bitmap
4. Set detection mode to Brightness Cutoff and set value to something high, around 0.995.
5. Click Apply
6. Delete original imported PNG
7. Select new object. Do Extensions->Modify Path->Approximate Curves by Straight Lines. (This part removes B-Splines)
8. Set value to 0.5. Apply and Close
9. File->Export as an Inkscape SVG.

## After Printing
Simple pieces may pop into place without any glue. Some pieces may come out loose and will need a drop of super glue.
Some complex pieces may require light tapping with a mallet to push into place.

## Examples
Examples are based on the images in [this repo](https://github.com/RiosDeterioratingMentalHealth/OuterWildsPlanetIcons)
