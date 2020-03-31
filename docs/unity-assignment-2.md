# Unity assignment 2: 360 image viewer

## Idea

1. View your 360 images in unity Equirectangular projection), 1 point
2. Add hotspots, 1 point
   - show info box etc.
   - change to other image/scene
3. Add your own twist to the viewer app (something extra, use your imagination), max 1 point
4. Return the project (check instructions below) to Oma and present your game to teacher before deadline to get the points

Grading 0-3 points.

## Instructions

1. Prepare 360 images: equirectangular projection, 2:1 ratio
   - using your own panoramas is preferred
   - there is couple of scrubby example images in Oma _documents/Unity_ folder, just in case
2. Import images to unity, 2 options:
   - Change image texture shape to _Cube_ in import settings, create material and set shader to: _Skybox/Cubemap_
   - Use default image import settings: create material and set shader to: _Skybox/Panoramic_
3. Add photo material to scene background (skybox): _Window -> rendering -> lighting settings -> environment, skybox material_
4. Set [SmoothMouseLook script](http://wiki.unity3d.com/index.php/SmoothMouseLook) for mouse based camera pan & tilt (this is used to simulate/replace head tracking available in "real" VR)
5. Add some 3D objects acting as hotspots
   - two types of hotspots: show/view some info (e.g. textbox) about something in the picture or move to another room/scene (other 360 image)
   - set the type of hotspots using e.g. tags
   - use Text gameobject on canvas to show info text (_GameObject -> UI -> Text_) when pointing/looking at the hotspot
6. Create a _CameraRayControl.cs_ script and attach it to _Main Camera_
   - add the functionality for interacting with hotspots
     - camera should [cast a ray](https://docs.unity3d.com/ScriptReference/Physics.Raycast.html) forward and react when the ray hits to other game object's collider
     - when pointig to info object/hotspot: show/hide the infobox
     - when pointing to change scene object/hotspot for couple of seconds: move to another room/scene
7. You should have at least two scenes and 360 images and user should be able to switch between the scenes using the hotspots
8. Develop further :)
   - design and add your own features

BONUS: Add [VR headset support](./unity-vr-instructions.md) and build for smartphone.

## Guidelines for Unity tasks

- 2-step returning:
  1. return your Unity project to oma: Create a zip-file of your project folder containing only _Assets_ and _ProjectSettings_ subfolders
  2. present project "live" to teacher latest at next day after the deadline to get the points
- always list used references & sources in code comments or in a separate readme file
- grading when returning late: less than a week: -50 %, more: -70-100 %
