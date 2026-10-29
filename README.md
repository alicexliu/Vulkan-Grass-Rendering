Vulkan Grass Rendering
==================================

**University of Pennsylvania, CIS 565: GPU Programming and Architecture, Project 5**

* Alice Liu
  * [LinkedIn](https://www.linkedin.com/in/aliceliuu/), [personal website](https://aliceliu.xyz/)
* Tested on: Windows 11, AMD Ryzen 5 7640HS @ 4.30GHz 16GB, RTX 4060 Laptop GPU 8GB (Personal Laptop)

## Overview
<p align="center">
  <img src="img/thumbnail.gif" width="650"><br>
  8192 blades of grass
</p>

In this project, I used Vulkan to implement a grass simulator and renderer. The project was split into three main parts that are explained more in depth below:
- Rendering the blades of grass
- Applying forces (gravity, recovery, and wind)
- Culling

### Rendering
<p align="center">
  <img src="img/still_grass.gif" width="500"><br>
  Still grass before forces are applied
</p>

### Forces
| Gravity | Gravity + Recovery | Gravity + Recovery + Wind |
|---|---|---|
| ![](img/gravity_grass.png) | ![](img/gravity_recovery_grass.gif) | ![](img/wind_grass.gif) | 

### Culling
| Distance Culling | View-Frustum Culling |
|---|---|
| ![](img/distance_culling.gif) | ![](img/view_frustum_culling.gif) | 

A brief description of the project and the specific features you implemented
GIFs of your project in its different stages with the different features being added incrementally

## Performance Analysis
### Number of Grass Blades


<p align="center">
  <img src="img/num_blades_graph.png" width="600"><br>
</p>

Below is the raw data:

| Number of Grass Blades | Avg Frame Time (ms) |
| :---: | :---: |
| 50 | 0.201 ms |
| 500 | 0.318 ms +
| 5,000 | 0.719 ms |
| 50,000 | 3.578 ms |
| 500,000 | 26.270 ms |


### Culling Tests


Your renderer handles varying numbers of grass blades
The improvement you get by culling using each of the three culling tests