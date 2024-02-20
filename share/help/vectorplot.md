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
* `sparsity` - A number between 0 and 1 to indicate the fraction of vectors to plot. Default is `1`.
* `showmesh` - A Boolean to indicate whether or not to plot the mesh with the vectors. Default is `true`.
* `colormap` - A `ColorMap` object to use for coloring the arrows. If not provided, `ViridisMap` is used as the default. Note that a constant `Color` object can also be used as a colormap, as it just matches all values to the same color.
* `scale` - A Boolean to indicate whether or not to scale the colors by the bounds of the colormap. Default is `true`.
* `scalebar` - A `Scalebar` object to use. 
* `colorby` - Argument to control the color of the arrows. See below
* `filter` and `transmit` - Used by the `povray` module to indicate transparency.

Supported `colorby` arguments: 

* `default` - Color all vectors by the same color.
* `norm` - Color by the magnitude of the vector fields
*  `x` - Color by the x-coordinate of the vector fields
* `y` or `z` - Color by the y or z components, similar to `x`.
