# here are three basic types of lighting:

- Ambient light is the light that permeates the scene; it's non-directional and affects every face in the scene equally, regardless of which direction it's facing.

- Directional light is light that is emitted from a specific direction. This is light that's coming from so far away that every photon is moving parallel to every other photon. Sunlight, for example, is considered directional light.

- Point light is light that is being emitted from a point, radiating in all directions. This is how many real-world light sources usually work. A light bulb emits light in all directions, for example.

For our purposes, we're going to simplify the lighting model by only considering simple directional and ambient lighting; we won't have any specular highlights or point light sources in this scene. Instead, we'll have our ambient lighting plus a single directional light source, aimed at the rotating cube from the previous demo.


<hr>

<br>

1. The world matrix translates the coordinates of your vertices from model space to world space. This transformation includes the position of the object in the world as well as its orientation and potentially scale.

2. The view matrix translates those vertices from world space to camera/view space. This means the transformed coordinates are in relation to the camera/point of view.

3. The projection matrix finally translates those coordinates from camera/view space to projection space. Projection space coordinates specify where the vertex is located on your display/monitor as well as containing depth information (i.e. How far away from the camera the point is). This coordinate space is the "homogeneous clip space", because all the x/y components of all visible points are in the range [-1,1]. Depth (z component) lies in [0, 1].

