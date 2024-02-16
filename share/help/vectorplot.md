[comment]: # (Vectorplot module help)
[version]: # (0.0.1)

# Vectorplot
[tagvectorplot]: # (vectorplot)

The `vectorplot` module provides a method for visualizing vector / dyadic fields on meshes. These functions produce Graphics objects that can be displayed with `Show`.

To use the module, first import it:

    import vectorplot

[showsubtopics]: # (subtopics)

## Plotvectorfield
[tagplotvectorfield]: # (plotvectorfield)

Visualizes a vector `Field` object:

    var g = plotvectorfield(field)

Plotfield accepts a number of optional arguments to control what is displayed:

* `dl` - Sets the size of the vectors. Default is `1`.
* `aspectratio` - Sets the aspect ratio of the arrows / cylinders representing the field. Default is `0.3`.
* `noarrows` - A Boolean variable to indicate whether you want the arrowheads to be drawn. Default is `false`. This can be set to `true` to visualize dyadic / nematic fields that have a head/tail symmetry.
* `colorby` - Argument to control the color of the arrows. See below
* `scalebar` - A `Scalebar` object to use. 
* `showmesh` - A Boolean to indicate whether or not to plot the mesh with the vectors. Default is `true`.
* `filter` and `transmit` - Used by the `povray` module to indicate transparency.

Supported `colorby` arguments: 

* `default` - Color all vectors by the same color.
*  `x` - Color by the x-coordinate of the vector fields
* `y` or `z` - Color by the y or z components, similar to `x`.
