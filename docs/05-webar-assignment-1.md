# WebAR Getting Started

Getting started WebAR development with [A-Frame](https://aframe.io/) and [AR.js](https://github.com/AR-js-org/AR.js). A-Frame is [based on three.js](https://aframe.io/docs/1.2.0/introduction/developing-with-threejs.html) and has a built-in support for AR.js, read: [article in A-Frame blog](https://aframe.io/blog/arjs/) and [AR.js Docs](https://ar-js-org.github.io/AR.js-Docs/marker-based/).

## Prerequisites

This is optional. For the basic development (and for this assignment) any code editor with _html/css/js_ support will do.

Install [JavaScript & web development tools](./00-software-setup.md).

- Node Package Manager, NPM, comes with [Node.js](https://nodejs.org/en/)
- [Git](https://git-scm.com/downloads)
- Code Editor/IDE like [Visual Studio Code](https://code.visualstudio.com/) or [Webstorm](https://www.jetbrains.com/webstorm/)
  - Preferred VS Code extensions: Auto Import, ESLint, EditorConfig for VS Code

## Assignment

1. Create a project (empty folder and _index.html_ file) **or** use the teacher's [Webpack based web development boilerplate project](https://github.com/mattpe/wtmp-starter) with local dev server.
    - to use the Webpack project you'll need Git, npm and basic knowledge of how to use them, short instructions:
        1. Get the boilerplate project: `git clone https://github.com/mattpe/wtmp-starter.git <NAME-OF-TARGET-DIR>`
        1. Install all dependencies (packages listed in _package.json_ and needed for running and developing the app, like three.js library, webpack, etc..): run `npm install` inside the project folder and packages are installed into _node\_modules_ folder
        1. Open the project folder in your editor. Source code files are located in _src/_ subfolder.
        1. Start the development server (at <http://localhost:8080/> by default) and run the app: `npm start`
            - browser window based on your default browser setting should open automatically, just open the developer tools and start developing your app
            - browser window should be refreshed automatically when you save any changes in source files. If not or something else goes wrong, try to restart the dev server: hit _ctrl-c_ to stop and run `npm start` to run it again
2. Follow the instructions of [Getting Started with Image Tracking](https://aframe.io/blog/arjs3/) tutorial (and check the [AR.js Docs](https://ar-js-org.github.io/AR.js-Docs/) too!)
    - Study [Creating good markers](https://github.com/Carnaux/NFT-Marker-Creator/wiki/Creating-good-markers) and genereate your own image marker with [NFT Marker Creator](https://carnaux.github.io/NFT-Marker-Creator/) tool.
3. Try with your own 3D model(s)
    - e.g. photogrammetry model from Toni's assignment or some of the objects created for Antti's assignments
    - [Supported model formats](https://aframe.io/docs/1.2.0/introduction/models.html)
    - Try using/converting to [glTF format](https://aframe.io/docs/1.2.0/components/gltf-model.html)

[Teacher's example files](../assets/webar/) for the 1st proof-of-concept tests (3D model source: <https://www.cgtrader.com/items/977015/download-page>).

### Notes & tips for development workflow

- External webcam is the easiest option to test with image markers displayed on your screen.
- If you don't have an external webcam, integrated webcam works with markers displayed on your mobile device's screen (or printed markers can be used).
- Test with your mobile device: use a local webserver in your home network or upload the web app to a web server and open with a mobile browser
- When testing on internet, SSL secured _https_ protocol must be used (http won't work).
- When using a mobile as a test device log messages can be accessed by using [Chrome dev tool and remote debugging](https://developers.google.com/web/tools/chrome-devtools/remote-debugging). On android device developer settings and usb debugging must be activated.
- Tip: uploading your files to <https://users.metropolia.fi/~MYUSERNAME/MY-FOLDER-NAME/> using command line: `scp -r dist/* MYUSERNAME@shell.metropolia.fi:public_html/MY-FOLDER-NAME/` (works with Git Bash)

### Grading (0-3 points)

- Working WebAR demo published on a web server, 1 point
- Teacher's example done (something similar to car marker & model), 1 p.
- Something extra done, own image marker and 3d models in use, clean implementation & code, 1 p.

### Returning

- Publish the application (contents of _dist/_ folder after production build _if_ using the Webpack project) on a web server (e.g: upload to your `public_html/`) and provide a link to the image marker used.
- Return the whole project folder as a **zip** file and a **clickable links** to your published app and the image marker to Oma
- Present your app to teacher to get the points.

**Using/bundling your own model files, textures and other assets with Webpack:**

All files in _src/assets_ folder are copied recursively to _dist/assets/_ folder when building the app or running the dev server.

To make a production build, a "release" of your app, stop the development server (_ctrl-c_) if running and run: `npm run build`. It generates _dist/_ folder inside your project folder. You can then publish your app by copying the content of that folder to any public web server.

## Some reading & links

- [WebAR: All you need to know about the next big thing](https://www.creativebloq.com/features/webar) By Ben Graves
- [Three.js and AR.js Examples](https://stemkoski.github.io/AR-Examples/)
- [AR.js Marker generator](https://ar-js-org.github.io/AR.js/three.js/examples/marker-training/examples/generator.html)
- [Using 3D models with AR.js and A-Frame](https://medium.com/@akashkuttappa/using-3d-models-with-ar-js-and-a-frame-84d462efe498)
- [glTF format for 3D](https://en.wikipedia.org/wiki/GlTF)
- [Online glTF converter](https://anyconv.com/gltf-converter/)
- WebAR with WebXR API by Wood Neck: [part 1](https://medium.com/naver-fe-platform/webar-with-webxr-api-part-1-e191a2dc7177), [part 2](https://medium.com/naver-fe-platform/webar-with-webxr-api-part-2-dc76b20767fb)
