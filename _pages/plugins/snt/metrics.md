---
title: SNT › Metrics
nav-links: true
nav-title: Metrics
artifact: org.morphonets:SNT
icon: /media/icons/snt.png
forum-tag: snt
update-site: Neuroanatomy
extensions: ["mathjax"]
tags: snt,reconstruction,tracing,arbor,neuron,morphometry,dendrite,axon,neuroanatomy
---

## Metrics
{% capture text%}
**This list reflects only default measurements and is [not exhaustive](#notes). For each metric SNT retrieves the descriptive statistics _Mix_, _Max_, _Mean_, _Standard Deviation_ (SD), _Sum_ and _N_**, which may lead to inevitable [redundancy](#notes) between measurements.<br>
E.g., when measuring  [Branch length](#branch-length) for a particular cell, it is possible to retrieve the length of the smallest branch (_Min_), the longest (_Max_), the average and standard deviation of all branch lengths (_Mean_ and _SD_), their total length (_Sum_), and number (_N_).
<br>
<br>
 Also, please note that some of the metrics described here have been ported from [L-measure](http://cng.gmu.edu:8080/Lm/help/index.htm): {% include citation doi='10.1038/nprot.2008.51' %}
{% endcapture %}
{% include notice icon="info" content=text %}



<span id="b"></span>
###### Branch contraction
A measure of _straightness_. The ratio between the Euclidean distance of a branch (i.e., Euclidean distance between the first and last node of the branch) and its path length. Range of values: ]0--1] (unitless)

###### Branch fractal dimension
Also known has [Hausdorff dimension](https://en.wikipedia.org/wiki/Hausdorff_dimension). Defined as the slope obtained from the log-log plot of _Path distance vs Euclidean distance_, as [implemented by L-measure](http://cng.gmu.edu:8080/Lm/help/index.htm) following the definition of [Marks & Burke (2007)](https://doi.org/10.1002/cne.21418). It is only computed for branches defined by at least five nodes. Described in: {% include citation doi='10.1002/cne.21418' %} 

###### Branch length
The path length of a branch (i.e., the sum of all its internode distances)

###### Branch mean radius
The average of the radii of the nodes defining a branch

###### Branch surface area
_Estimated_ surface area[^1] of a branch computed from treating each internode segment as a conical frustum and summing the surface area of all frusta

###### Branch volume
_Estimated_ volume[^1] of a branch computed from treating each internode segment as a conical frustum and summing the volume of all frusta

<span id="c"></span>
###### Cable length
The total path length of a structure, i.e., the sum of all internode distances of its paths

###### Complexity index
Also known as "Dendritic Complexity Index". An index based on the number of primary neurites, total arbor length, and the number and Strahler-order of terminal branches. Described in: {% include citation doi='10.1523/JNEUROSCI.19-22-09928.1999' %}

###### Convex hull: Boundary size
The perimeter of the 2D polygon or the surface area of the 3D polyhedron of the convex hull

###### Convex hull: Boxivity
The extent to which the convex hull approaches a rectangle (2D) or a cuboid (3D). Range of values: 0--1 (unitless)

###### Convex hull: Centroid-root distance
The distance between the root of a neuronal arbor and the centroid of its convex hull

###### Convex hull: Elongation
The [caliper (also known as Feret) diameter](https://en.wikipedia.org/wiki/Feret_diameter) of the convex hull

###### Convex hull: Roundness
The extent to which the convex hull approaches a circle (2D) or a sphere (3D). Range of values: 0--1 (unitless)

###### Convex hull: Size
Either the area of the 2D polygon, or the volume of the 3D polyhedron defining the convex hull

<span id="d"></span>
###### Depth
The depth of the bounding box embedding the structure being measured

<span id="h"></span>
###### Height
The height of the bounding box embedding the structure being measured

###### Horton-Strahler bifurcation ratio
The average bifurcation ratio of [Strahler bifurcation ratios](https://en.wikipedia.org/wiki/Strahler_number#Bifurcation_ratio)

###### Horton-Strahler number
The highest Horton-Strahler number of a tree, i.e., the Horton-Strahler number of its root node 

<span id="i"></span>
###### Internode distance
The distance between nodes defining a branch or a Path

###### Internode distance (squared)
The squared distance between nodes defining a branch or a Path. Alternative to _Internode distance_ when faster computations are required.

<span id="l"></span>
###### Length of inner branches
The sum of branch lengths of branches of highest Strahler order. Typically, these correspond to the most 'internal' branches of an arbor, in direct sequence from the root. Note that_Primary branches_ are _inner branches_ starting at the tree's root.

###### Length of longest shortest path
Considering a [graph-theory tree](https://en.wikipedia.org/wiki/Tree_(graph_theory)), the _Length of longest shortest path_ corresponds to the [graph diameter](https://mathworld.wolfram.com/GraphDiameter.html). Note that this metric can only be computed for structures that are valid mathematical trees.

###### Length of primary branches
The sum of branch lengths of primary (or root-associated) branches. Primary branches have origin in a tree's root, extending to the closest branch point or end-point, i.e., they are _inner branches_ starting at the root. Note that a primary branch can also be terminal.

###### Length of terminal branches
The sum of branch lengths of branches ending at terminal endpoints (tips)

<span id="n"></span>
###### No. of branch nodes (branch fragmentation)
 The total number of nodes (and thus _compartments_) in a branch

###### No. of branch points
The total number (count) of branch points (also known as fork points)

###### No. of branches
The total number (count) of branches

###### No. of fitted paths
The total number (count) of [fitted](/plugins/snt/manual#refinefit) paths

###### No. of inner branches
The number of branches of highest Strahler order. Typically, these correspond to the most 'internal' branches of an arbor, in direct sequence from the root

###### No. of path nodes (path fragmentation)
 The total number of nodes (and thus _compartments_) in a path

###### No. of paths
The total number (count) of paths defining a structure

###### No. of primary branches
The total number (count) of primary (or root-associated) branches. Primary branches have origin in a tree's root, extending to the closest branch point or end-point, i.e., they are _inner branches_ starting at the root. Note that a primary branch can also be terminal.

###### No. of spines/varicosities
Sum of all spine/varicosity markers in a structure

###### No. of spines/varicosities per path
Number of spines/varicosities associated with a path

###### No. of terminal branches
The total number (count) of branches ending at terminal endpoints (tips)

###### No. of tips
The total number (count) of terminal endpoints in a structure

###### No. of total nodes
The total number (count) of nodes in a structure

###### Node intensity values
The pixel intensity at each node location

###### Node radius
The radius at each node, typically obtained from [fitting procedures](/plugins/snt/manual#refinefit)

<span id="p"></span>
###### Partition asymmetry
[L-measure metric](http://cng.gmu.edu:8080/Lm/help/index.htm). Computed at each bifurcation point of the structure being measured. Note that branch points with more than 2 children are ignored. Given $$n1, n2$$ the number of tips on each side of a bifurcation point, Partition asymmetry is defined as: $$\frac{abs(n1-n2)}{(n1+n2-2)}$$. 

###### Path channel
The color channel associated with a path (multidimensional image)

###### Path contraction
The ratio between the Euclidean distance of a path (i.e., Euclidean distance between the first and last node of the path) and its path length. Range of values: ]0--1[ (unitless)

###### Path frame
The time-lapse frane associated with a path (multidimensional image)

###### Path length
The sum of all internode distances in a path

###### Path mean radius
The average of the radii of the nodes defining a path

###### Path order
See [Path Order Analysis](/plugins/snt/analysis#path-order-analysis)

###### Path spine/varicosity density
The number (count) of spine/varicosity markers associated with a path, divided by its path length

###### Path surface area
_Estimated_ surface area[^1] of a path computed from treating each internode segment as a conical frustum and summing the surface area of all frusta

###### Path volume
_Estimated_ volume[^1] of a path computed from treating each internode segment as a conical frustum and summing the volume of all frusta

<span id="r"></span>
###### Remote bif. angles
The angle between each bifurcation point and its children in the simplified graph, which comprise either branch points or terminal nodes. Note that branch points with more than 2 children are ignored.

<span id="s"></span>
###### Sholl: Decay
The [Sholl regression coefficient](/plugins/sholl-analysis#sholl-decay)

###### Sholl: Degree of Polynomial fit
The polynomial degree used to fit the Sholl profile. See [Sholl › Fitting functions](/plugins/sholl-analysis#eq1)

###### Sholl: Kurtosis
See [Kurtosis](/plugins/sholl-analysis#kurtosis) in [Sholl › Metrics based on sampled data](/plugins/sholl-analysis#metrics-based-on-sampled-data)

###### Sholl: Max
See [Max inters.](/plugins/sholl-analysis#max-inters) in [Sholl › Metrics based on sampled data](/plugins/sholl-analysis#metrics-based-on-sampled-data)

###### Sholl: Max (fitted)
See [Critical value](/plugins/sholl-analysis#critical-value) in [Sholl › Metrics based on fitted data](/plugins/sholl-analysis#metrics-based-on-fitted-data)

###### Sholl: Max (fitted) radius
See [Critical radius](/plugins/sholl-analysis#critical-radius) in [Sholl › Metrics based on fitted data](/plugins/sholl-analysis#metrics-based-on-fitted-data)

###### Sholl: Mean
See [Mean inters.](/plugins/sholl-analysis#mean-inters) in [Sholl › Metrics based on sampled data](/plugins/sholl-analysis#metrics-based-on-sampled-data)

###### Sholl: No. maxima
The number of times _Max inters._ occurs in a Sholl profile. See [Max inters.](/plugins/sholl-analysis#max-inters) in [Sholl › Metrics based on sampled data](/plugins/sholl-analysis#metrics-based-on-sampled-data)

###### Sholl: No. secondary maxima
The number of times a secondary peak occurs in a Sholl profile. See [Max inters.](/plugins/sholl-analysis#max-inters) in [Sholl › Metrics based on sampled data](/plugins/sholl-analysis#metrics-based-on-sampled-data)

###### Sholl: Ramification index
See [Schoenen Ramification index](/plugins/sholl-analysis#schoenen-sampled) in [Sholl › Metrics based on sampled data](/plugins/sholl-analysis#metrics-based-on-sampled-data)

###### Sholl: Skeweness
See [Skeweness](/plugins/sholl-analysis#skeweness) in [Sholl › Metrics based on sampled data](/plugins/sholl-analysis#metrics-based-on-sampled-data)

###### Sholl: Sum
See [Sum inters.](/plugins/sholl-analysis#sum) in [Sholl › Metrics based on sampled data](/plugins/sholl-analysis#metrics-based-on-sampled-data)

###### Surface area
Treating each internode segment as a conical frustum, the sum of the surface areas[^1] of all frusta

<span id="v"></span>
###### Volume
Treating each internode segment as a conical frustum, the sum of the volume[^1] of all frusta

###### Width
The width of the bounding box embedding the structure being measured

###### X,Y,Z coordinates
Cartesian coordinates in the three-dimensional space

##### Notes
- This list does not include specialized metrics provided by dedicated SNT plugins, such as [Strahler](/plugins/snt/analysis#strahler-analysis) or [Sholl](/plugins/snt/analysis#sholl-analysis)
- Some combinations of metrics/statistics may not be meaningful: e.g., if you are only measuring a single cell, pairing [cable length](#cable-length) to _SD_ will not be useful, since only one value has been computed. In this case, the Measurements table will append '[Single metric]' to such data
- Each of the 60+ metrics is represented by five statistical properties: minimum, maximum, mean, standard deviation and sum, resulting in a total of at least $$60\times 5$$ features. Note that there is an intrinsic redundancy between these features: E.g., for a given cell, retrieving [Branch length](#branch-length)'s _N_ is effectively the same as retrieving [No. of branches](#no-of-branches)
-  *NaN* values for a reported metric typically reflect undefined operations (e.g., division by zero), or the fact that the reconstruction being parsed is not a valid mathematical tree
- Currently, volume-related metrics do not take into account [path fillings](/plugins/snt/step-by-step-instructions#filling)

[^1]: Volume and surface area calculations assume radii have been assigned to  path nodes, typically through [fitting routines](/plugins/snt/manual#refinefit).<br>

<span id="statistics"></span>
## Group Statistics
SNT assembles comparison reports and simple statistical reports (two-sample t-test/one-way ANOVA) for up to six groups of cells. This is described in [Comparing Reconstructions](/plugins/snt/analysis#comparing-reconstructions). Descriptive statistics of measurements can be obtained by running _Summarize Existing Results_ in the [Measurements dialog](/plugins/snt/analysis#measurements) or by running [ Frequency/Distribution Analysis](https://imagej.net/plugins/snt/analysis#statistics) commands.


## Glossary

###### Mesh
A polygon mesh defines the shape of a three-dimensional polyhedral object. In neuronal anatomy, meshes define neuropil annotations, typically compartments of a reference brain atlas (e.g., the hippocampal formation in mammals, or mushroom bodies in insects)

###### Multi-dimensional image
An image with more than 3 dimensions (3D). Examples include fluorescent images associated with multiple fluorophores (multi-channel) and images with a time-dimension (time-lapse videos). A 3D multi-channel timelapse has 5 dimensions

###### Neurite
Same as neuronal process. Either an axon or a dendrite

###### Path
Can be defined as a sequence of branches, starting from soma or a branch point until a termination. In manual and assisted (semi-automated) tracing, neuronal arbors are traced using paths, not branches. [Fitting algorithms](/plugins/snt/manual#refinefit) that take into account voxel intensities can be used to refine the center-line coordinates of a path, typically to obtain more accurate curvatures. Fitting procedures can also be used to estimate the volume of the neurite(s) associated with a path

###### (Neuronal) morphometry
Quantification of neuronal morphology

###### Neuropil
Any area in the nervous system. The cellular tissue around neuronal processes

###### Out-of-core
Software with out-of-core capabilities is able to process data that is too large to fit into a computer’s main memory. SNT supports out-of-core tracing via scripting.

###### Reconstruction
See [Tracing](#tracing)

###### ROI
Region of Interest. Define specific parts of an image to be processed in image processing routines

###### Skeleton
A thinned version of a digitize shape (such as a neuronal reconstruction) or of a binary image

###### Tracing
A digital reconstruction of a neuron or neurite. The term predates computational neuroscience and reflects the manual ‘tracing’ on paper performed with [camera lucida](https://en.wikipedia.org/wiki/Camera_lucida) devices by early neuroanatomists

###### Volume rendering
A visualization technique for displaying image volumes (3D images) directly as 3D objects


{% capture text%}
This glossary was assembled from the supplementary note of SNT's publication: {% include citation id='plugins/snt' %}
{% endcapture %}
{% include notice icon="info" content=text %}
