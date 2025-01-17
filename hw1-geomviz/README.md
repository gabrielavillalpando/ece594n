# Geomviz: Visualizing Differential Geometry

Goal: Get intuition on Differential Geometry by visualizing manifolds.

- Deadline: Thursday 04/21/2022: Presentation in class (5 min per team).
- Team of 2-4 students.

## Register your team

First come, first serve. Send a message on slack to register your team.

- [X] Stiefel manifold: Xinling Yu, Zheng Xu and Zhiyuan Ren.
- [X] Grassmanian manifold: Gabriella Torres, Breanna Takacs, Becky Martin and Sam Rosen.
- [X] Manifold of symmetric positive definite (SPD) matrices: Christos Zangos and Vincent Benenati.
- [ ] Hyberbolic spaces: Alireza Parsay.
- [X] Special Euclidean group: Swetha Pillai and Ryan Guajardo.
- [ ] Heisenberg group: TBD.
- [X] Discrete curves: Jax Burd and Abhijith Atreya.
- [X] Manifold of beta distributions: Yiliang chen and Sunpeng Duan.
- [X] Manifold of categorical distributions: Ian Wu, Steven Lin, Haoming Chen 

## Guidelines

- [Git clone](https://github.com/git-guides/git-clone) this GitHub repository.
- Create a new folder in this folder with the name of your manifold.
- In this new folder:
  - Add a python file named `[your-manifold].py`, e.g. `grassmanian.py`
    - This file will have the core functions for your project (details below).
  - Add a Jupyter notebook named `[your-manifold].ipynb` that represents the bulk of your project.
- Make sure to indicate which teammate did which part of the work.
- Submit your work as a [Pull Request (PR)](https://opensource.com/article/19/7/create-pull-request-github) to this GitHub repository.
- You can submit code to this repository anytime until the deadline.

## Important Remarks

- The elementary operations (exp, log, geodesics, etc) are already implemented in [geomstats/geometry](https://github.com/geomstats/geomstats/tree/master/geomstats/geometry):
  - Search for the file that represents your manifold in this folder.
  - Your goal is not to re-implement them, but to use them and visualize them.
- Some visualizations are already implemented in [geomstats/visualization.py](https://github.com/geomstats/geomstats/blob/master/geomstats/visualization.py) for some manifolds.
  - Search if your manifold has some visualization implemented and think about how to improve it.
  - You can use what is already implemented.
- The folders of [examples](https://github.com/geomstats/geomstats/tree/master/examples) and [notebooks](https://github.com/geomstats/geomstats/tree/master/notebooks) show you examples on how to use the operations on your manifold.
  - Search for your manifold in these files to get ideas.
- Higher-dimensional manifolds: (i) do not plot them or (ii) find a "trick" to plot them
- Note that some visualizations are already available in Geomstats for some manifolds listed above.

## Code Structure 

Design from Elodie Maignant, PhD student at INRIA (France) and contributor to Geomstats.

− In your file `[your-manifold].py`:
  - Create a python class named after your manifold `class YourManifold`.
  - Add visualization utils as methods from this class, such as:
    - `plot`: draws the manifold (e.g. cone for SPD matrices)
    - `plot_grid`: draws the manifold with a geodesic grid.
    - `plot_rendering`: draws the manifold with regularly sampled data.
    - `plot_tangent_space`: draws the tangent space to the manifold at a point.
    - `scatter`: plot a point cloud. Inherits matplotlib.scatter parameters.
    
    - `plot_geodesic` allows to visualise a (discretised) geodesic. Takes either point and tangent vec as parameters, or initial point and end point as parameters.
    
    − `plot_vector_field` allows to visualise vectors fields. Takes points and tangent vecs as parameters.
    
− In your notebook `[your-manifold].ipynb`, respect the following outline:
  - 1. Introduction.
  - 2. Mathematical definition of [your manifold].
  - 3. Uses of [your manifold] in real-world applications.
  - 4. Visualization of elementary operations on [your manifold]
    - Showcase your visualization can be used by plotting the inputs and outputs of operations such as exp, log, geodesics.
  - 5. Conclusion and references


## Additional remarks

- Your code should be documented with docstrings, see [here for docstring guidelines](https://github.com/geomstats/geomstats/blob/master/docs/contributing.rst#writing-docstrings).
- You do not have to implement all of the methods listed above. You can implement methods not listed.
- Your visualization functions should work with only matplotlib.
- You can add options for your functions to be interactive, using plotly or bokeh in addition to matplotlib.
- Here is an [example of a visualization project by Elodie Maignant](https://github.com/geomstats/geomstats/blob/master/notebooks/16_real_world_applications__visualizations_in_kendall_shape_spaces.ipynb).


## Grading Criteria

- The notebook respects the guidelines in this Readme, and in particular: the code is clean and documented. 10%
- The notebook gives the correct mathematical definition of the manifold. 10%
- The notebook gives 5+ interesting real-world uses of the manifold, with references. 10%
- The notebook uses existing `geomstats` operations (log, exp, geodesics, parallel transport) on the manifold. 20%
- The notebook uses existing `geomstats` [visualization tools](https://github.com/geomstats/geomstats/blob/master/geomstats/visualization.py) to show the results of the elementary operations. 20% 
  - If there are no tools in [visualization tools](https://github.com/geomstats/geomstats/blob/master/geomstats/visualization.py) for your manifold, mention it and this criterion is not taken into account.
- The notebook implements custom visualization tools to show the results of the elementary operations. 20%
- The presentation in class is clear and helps give intuition about the manifold. 10%

