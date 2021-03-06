## Gridfields

Scientists' ability to generate and store simulation results is outpacing their ability to analyze them via ad hoc programs. We observe that these programs exhibit an algebraic structure that can be used to facilitate reasoning and improve performance.

In our work on GridFields, we present a formal data model that exposes this algebraic structure, then implement the model, evaluate it, and use it to express, optimize, and reason about data transformations in a variety of scientific domains.

Simulation results are defined over a logical grid structure that allows a continuous domain to be represented discretely in the computer. Existing approaches for manipulating these gridded datasets are incomplete. The performance of SQL queries that manipulate large numeric datasets is not competitive with that of specialized tools, and the up-front effort required to deploy a relational database makes them unpopular for dynamic scientific applications. Tools for processing multidimensional arrays can only capture regular, rectilinear grids. Visualization libraries accommodate some forms of unstructured grid, but no algebra has been developed to organize the library of raw algorithms and afford optimization. Further, these libraries are data dependent---physical changes to data characteristics break user programs.

The GridFields library exposes 1) topological equivalences among gridded datasets and 2) logical equivalences among grid-oriented programs. These equivalences offer optimization opportunities and simplify programming.

We adopt the grid as a first-class citizen, separating topology from geometry and separating structure from data. Our model is agnostic with respect to dimension, uniformly capturing, for example, particle trajectories (1-D), sea-surface temperatures (2-D), and blood flow in the heart (3-D). Equipped with data, a grid becomes a gridfield. We provide operators for constructing, transforming, and aggregating gridfields that admit algebraic laws useful for optimization. We implement the model by analyzing several candidate data structures and incorporating their best features. We then show how to deploy gridfields in practice by injecting the model as middleware between heterogeneous, ad hoc file formats and a popular visualization library.

In this project, we define, develop, implement, evaluate and deploy a model of gridded datasets that accommodates a variety of complex grid structures and a variety of complex data products. We evaluate the applicability and performance of the model using datasets from oceanography, seismology, and medicine and conclude that our model-driven approach offers significant advantages over the status quo.

Here at CMOP, we use GridFields to implement query services over ocean circulation model results, and we have added a GridFields plugin module for the VisTrails provenance and visualization system.

## Installation
There are two packages: a C library (clib) and SWIG python bindings (pygridfields)
See README files in these directories for more information

## References
 * GridFields: Model-Driven Data Transformation in the Physical Sciences, Bill Howe, Phd Dissertation, Portland State University, 2007.
 * Algebraic Manipulation of Scientific Datasets Bill Howe, David Maier VLDB Journal, 14(4), November 2005

