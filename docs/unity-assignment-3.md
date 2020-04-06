# Unity assignment 3: 3D models (in VR)

Import your own 3D models to Unity and explore them and interact with them by moving around in the virtual world.

## Reading

- [Supported model file formats](https://docs.unity3d.com/Manual/3D-formats.html)
- [Importing model files](https://docs.unity3d.com/Manual/ImportingModelFiles.html)
- [Sketchup model import settings](https://docs.unity3d.com/Manual/class-SketchUpImporter.html)
- [Meshes & materials](https://docs.unity3d.com/Manual/class-Mesh.html)

## Instructions

1. Import your model(s) and place it into scene (Try with `.skp`, `.fbx`, or `.dae` format from Sketchup (or other modelling software))
   - house model (result from Ulla's Sketchup task), some notes:
     - When using the free web version of Sketchup, save your model in **2017** format (`skp`)
     - [Sketchup Make 2017](https://help.sketchup.com/en/downloading-older-versions) is a free standalone software that can be used to export models in Collada format (`dae`) too
     - if having performance issues when importing/using models in Unity check that your model is not too complex
   - photogrammetry model if available (result from Mika's task)
   - 3D scanned model if available (result from Mika's task)
2. Fix materials (if needed)
   - Choose your model in _Project_ window and click _Materials_ tab in _Inspector_
   - When using `skp` format try to change _Location_ property value to _Use external Materials (Legacy)_
3. Add "player" object with capability to explore your model(s) by moving and looking around
   - prevent walking through walls etc. -> add colliders to your models (generate or create by yourself)
   - check `03-VRTravel.zip` example project in Oma _Documents/Unity_
4. Add your extras, some ideas:
    - Add [VR headset support](./unity-vr-instructions.md)
    - Add hotspots and other user interactions
    - Add anything to make your scene more interesting to explore

## Grading (max. 3 points)

- Self-made 3D model(s) and movable player in Unity scene: 1 p.
- Extras: 2 p.

## Guidelines for Unity tasks

- 2-step returning:
  1. return your Unity project to oma: Create a zip-file of your project folder containing only _Assets_ and _ProjectSettings_ subfolders
  2. present project "live" to teacher latest at next day after the deadline to get the points
- always list used references & sources in code comments or in a separate readme file
- grading when returning late: less than a week: -50 %, more: -70-100 %
