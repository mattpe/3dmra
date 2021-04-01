# Unity assignment 3: 3D models (in VR)

Import your own 3D models to Unity and explore them and interact with them by moving around in the virtual world.

## Reading

- [Supported model file formats](https://docs.unity3d.com/Manual/3D-formats.html)
- [Importing model files](https://docs.unity3d.com/Manual/ImportingModelFiles.html)
- [Using FBX files in other applications](https://docs.unity3d.com/Manual/HOWTO-exportFBX.html)
- [Meshes & materials](https://docs.unity3d.com/Manual/class-Mesh.html)

## Instructions

1. 1st Unity assignment can be used as a starting point
1. Import your 3D models and place them into scene (results of Antti's assignments)
   - use of `.fbx` format is preferred
   - some notes for house/room models:
     - if having performance issues when importing/using models in Unity check that your model is not too complex
     - if your model includes a camera, disable it to use the Unity's Main Camera game object
   - add your photogrammetry model if available (result/product of another assignment)
   - add your 3D scanned model if available (result/product of another assignment)
   - Some tips _for Sketchup users_:
     - [Sketchup model import settings](https://docs.unity3d.com/Manual/class-SketchUpImporter.html)
     - try with `.skp`, `.fbx`, or `.dae` format
     - when using the free web version of Sketchup, save your model in **2017** format (`skp`)
     - [Sketchup Make 2017](https://help.sketchup.com/en/downloading-older-versions) is a free standalone software that can be used to export models in Collada format (`dae`) too
1. Fix imported materials (only when needed)
   - choose your model in _Project_ window and click _Materials_ tab in _Inspector_
   - if using `skp` format try to change _Location_ property value to _Use external Materials (Legacy)_
1. Add a "player" object with capability to explore your model(s) by moving and looking around (check assignment 1)
   - add [SmoothMouseLook script](http://wiki.unity3d.com/index.php/SmoothMouseLook) for mouse based camera pan & tilt (simulating head tracking available in "real" VR)
   - prevent walking through walls etc. -> add colliders to your models (generate in import settings or create by yourself)
   - how to move the player or interact with objects without keyboard, joystick, etc. controllers? (one solution: see raycast example in assignment 2)
1. Add your extras, use your imagination, some ideas:
    - use of hotspots and other user interactions
    - innovative use of models
    - set the atmosphere by playing with ligths & scene background skybox (see Antti's _TexturingAndStuff.zip_ example project in Oma)
    - _anything_ to make your scene more interesting for user to explore
    - [VR headset support](./unity-vr-instructions.md)

## Grading (max. 3 points)

- Self-made 3D models and movable player in Unity scene: 1 p.
- Extras: 2 p.

## Guidelines for all Unity tasks

- 2-step returning:
  1. return your Unity project to oma: Create a zip-file of your project folder containing **only** the _Assets_ and _ProjectSettings_ subfolders
  2. present your project "live" to teacher latest at next day after the deadline to get the points
- always list used references & sources in code comments or in a separate readme file
- grading when returning late: a week or less: -50 %, more: -70-100 %
