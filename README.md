# WireFilter
With this FreeCAD macro you can filter a sketch (or any object with wires, including solids) to use only the wires you desire to use.  The sketch itself is unchanged.  The filter acts as an intermediary.  You can also 2D offset the wires, reorder the wires, scale the wires (independently in x, y, z directions), choose among 4 different face makers, and form a new wire from selected edges.  When used in Part Design it automatically inserts itself into the parent body of the selected sketch.  With WireFilter you can use Pad on sketches it would otherwise not be able to use (if it has nested wires within nested wires, for example if you make a face using the FaceMakerBullseye option).
## Toolbar Icon
<a href="wirefilter.svg">Download</a> the toolbar icon: <img src="wirefilter.svg" alt="toolbar icon">

## Usage
Select an object to filter.  If the entire object is selected in the tree, then all the wires are used.  If one or more faces are selected, then the wires that make up those faces are used.  If one or more edges are selected, then the wires that contain those edges will be filtered for use.  After making the desired selection run the macro, and a new document object called WireFilter will be created.  Modify the WireFilter by editing its properties.  If desired, you can select edges of the WireFilter object in the 3D view and toggle the SelectEdges boolean trigger to put the selected edges into the Selected Edges property (a string list).  Then if you set UseSelectedEdges to True you will futher filter out all other edges and form a new wire from the selected edges.  This new wire can be offset, scaled, and made into a face.

By default it locates itself coincident with the filtered object, but if you wish to do so you can toggle the Follow Source property to False, and then attach the WireFilter or adjust its placement as desired.  In this manner you can have multiple WireFilters of the same sketch and place them in different positions, for example, to loft between them.


## Changelog

##### 0.2021.10.19.rev2
Add option to fix normals on Pads and Extrudes that cannot find the normal properly
##### 0.2021.10.19
Initial upload
