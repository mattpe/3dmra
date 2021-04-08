# Unity Build for VR Goggles

## Adding Google VR Support (Cardboard) and building for Android devices (or iOS)

1. Follow the instructions by Google: [Quickstart for Google Cardboard for Unity](https://developers.google.com/cardboard/develop/unity/quickstart) and study especially the _Player/Main Camera_ GameObjects and attached components
1. Adapt settings and concepts from the quickstart to your own project/scene
1. Check also Unity docs: [Configuring your Unity Project for XR](https://docs.unity3d.com/Manual/configuring-project-for-xr.html)

### Some generic tips for VR builds (Android)

- Disable _SmoothMouseLook.cs_ and other keyboard/mouse controls if used for development only
  - Replace with _Tracked Pose Driver_ componet to use the device orientation for controlling the camera rotation
- Enable appropriate XR plugins  _Edit_ -> _Project Settings_ -> _XR Plugin Management_, click _Install XR Plugin Management system_
- Check/test/fix Canvas settings when using canvas based UI ([more info](https://unity3d.com/learn/tutorials/topics/virtual-reality/user-interfaces-vr), must be done for every scene)
  - Choose `Canvas` game object
  - Set Render mode to _Screen space - Camera_
  - Drag `Main Camera` game object to _Render Camera_
  - Fix _Plane Distance_ & _Scale Factor_ values (affects to how large UI elements appear on screen and how far the UI gets drawn compared to other game objects in the scene)
- Make sure you have [Android SDK Tools & JDK included in Unity modules installation](../assets/unity-android-sdk-install.png) or download, install & configure [Android SDK](https://developer.android.com/studio#downloads) manually
- Make your app identifier unique, choose _Player settings..._ and set: _Company Name_ and _Product Name_ to create a unique _Package Name_
- Set _minimum API level_ ([Android version](https://en.wikipedia.org/wiki/Android_version_history)) according to the specs of your test device (or how old Android versions you want to support)
- _Build & Run_ on a device connected with USB
  - [Enable developer mode](https://developer.android.com/studio/debug/dev-options) on your device
  - Allow USB debugging
- or _Build_ and install generated apk file manually to the device
  - Allow app installation from all sources on your device

## Unity VR docs & tutorials

- [Unity VR Documentation](https://docs.unity3d.com/Manual/VROverview.html)
- Read [VR best practice tutorial](https://learn.unity.com/tutorial/vr-best-practice)
- Check [Best UI Practices for VR tutorial](https://learn.unity.com/tutorial/unit-6-best-ui-practices-for-vr)

## Other VR devices

Follow the developer instructions provided by the device manufacturer and select correct XR plugin in Unity XR plugin management settings.

---

### Building for Samsung Gear VR goggles

- [Oculus Unity Developer Guide](https://developer.oculus.com/documentation/unity/latest/concepts/book-unity-dg/)

1. Check the Google VR on Android instructions above
    - fix canvas
    - disable desktop/laptop controls
    - switch to android platform
2. Choose _Player settings..._ and add Oculus to Virtual Realitys SDKs in Android's XR settings
3. Import `oculussig_[SOME_HASH]` file (download from Oma) into `Assets/Plugins/Android/Assets/` folder inside your project folder (signature file is device specific and needed to run Gear VR app in development mode)
4. _Build & run_
