# Unity Build for VR Goggles

## Adding Google VR Support (Cardboard) and Building for Android

- [Google VR](https://vr.google.com/)
- [Unity Documetation](https://docs.unity3d.com/Manual/googlevr_quick_start.html)

1. [Download the SDK](https://developers.google.com/vr/develop/unity/download) Choose latest _.unitypackage_ file
2. Import GoogleVR package to your project: _Assets -> Import package -> Custom package..._
3. Download and install [Android SDK](https://developer.android.com/studio#downloads)
4. Fix Canvas settings ([more info](https://unity3d.com/learn/tutorials/topics/virtual-reality/user-interfaces-vr), must be done for every scene)
    - Choose `Canvas` game object
    - Set Render mode to _Screen space - Camera_
    - Drag `Main Camera` game object to _Render Camera_
    - Set Plane distance value to something smaller (affects to how large UI elements appear on screen and how far the UI gets drawn compared to other game objects in the scene)
5. Disable _SmoothMouseLook.cs_ and other keyboard/mouse controls if used
6. Open _File -> Build settings_ and switch platform to Android
7. Choose _Player settings..._ and set them in inspector:
    - Product & Company name
    - Android settings: Package Name
    - XR settings: Add cardboard
8. _Build & Run_ (device connected with USB)
    - [Enable developer mode](https://developer.android.com/studio/debug/dev-options) on your device
    - Allow USB debugging
9. or _Build_ and install generated apk file manually to the device
    - Allow app installation from all sources on your device

## Google VR for IOS

- [Google's quickstart doc](https://developers.google.com/vr/develop/unity/get-started-ios)

## Building for Samsung Gear VR

- [Oculus Unity Developer Guide](https://developer.oculus.com/documentation/unity/latest/concepts/book-unity-dg/)

1. Check the Google VR on Android instructions above
    - fix canvas
    - disable desktop/laptop controls
    - switch to android platform
2. Choose _Player settings..._ and add Oculus to Virtual Realitys SDKs in Android's XR settings
3. Import `oculussig_[SOME_HASH]` file (download from Oma) into `Assets/Plugins/Android/Assets/` folder inside your project folder (signature file is device specific and needed to run Gear VR app in development mode)
4. _Build & run_
