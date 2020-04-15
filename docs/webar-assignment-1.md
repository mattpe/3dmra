# WebAR Getting Started

Getting started WebAR development with [A-Frame](https://aframe.io/) and [AR.js](https://github.com/AR-js-org/AR.js). A-Frame is [based on three.js](https://aframe.io/docs/1.0.0/introduction/developing-with-threejs.html) and has a [built-in support for AR.js](https://aframe.io/blog/arjs/).

## Prerequisites

(Optional. For the basic stuff any text editor will do.)

Install [JavaScript & web development tools](./01-software-setup.md).

- Node Package Manager, NPM, comes with [Node.js](https://nodejs.org/en/)
- [Git](https://git-scm.com/downloads)
- Code Editor/IDE like [Visual Studio Code](https://code.visualstudio.com/) or [Webstorm](https://www.jetbrains.com/webstorm/)
  - Preferred VS Code extensions: Auto Import, ESLint, EditorConfig for VS Code

## Assignment

1. Create a project (empty folder and _index.html_ file) or use the teacher's [Webpack based web development boilerplate project](https://github.com/mattpe/wtmp-starter) with local dev server.
    - to use the Webpack project you'll need Git, npm and basic knowledge of how to use them, short instructions:
    1. Get the boilerplate project: `git clone https://github.com/mattpe/wtmp-starter.git <NAME-OF-TARGET-DIR>`
    1. Install all dependencies (packages listed in _package.json_ and needed for running and developing the app, like three.js library, webpack, etc..): run `npm install` inside the project folder and packages are installed into _node\_modules_ folder
    1. Open the project folder in your editor. Source code files are located in _src/_ subfolder.
    1. Start the development server (at <http://localhost:8080/> by default) and run the app: `npm start`
        - browser window based on your default browser setting should open automatically, just open the developer tools and start developing your app
        - browser window should be refreshed automatically when you save any changes in source files. If not or something else goes wrong, try to restart the dev server: hit _ctrl-c_ to stop and run `npm start` to run it again
2. Follow the instructions of [Getting Started with Image Tracking](https://aframe.io/blog/arjs3/) tutorial (and check [AR.js Docs](https://ar-js-org.github.io/AR.js-Docs/) too!)
    - Study [Creating good markers](https://github.com/Carnaux/NFT-Marker-Creator/wiki/Creating-good-markers) and genereate your own image marker with [NFT Marker Creator](https://carnaux.github.io/NFT-Marker-Creator/) tool.
3. Include your own 3D model
    - e.g. Photogrammetry model from Mika's assignment, some of the objects in your house model or anything else
    - [Supported model formats](https://aframe.io/docs/1.0.0/introduction/models.html)
    - Try using/converting to [glTF format](https://aframe.io/docs/1.0.0/components/gltf-model.html)

[Teacher's example files](../assets/webar/) for the 1st proof-of-concept tests (3D model source: <https://www.cgtrader.com/items/977015/download-page>).

### Notes & tips for development workflow

- External webcam is the easiest option to test with markers displayed on your screen.
- If you don't have an external webcam, integrated webcam works with markers displayed on your mobile device's screen (or printed markers can be used).
- Test with your mobile device: use a local webserver in you home network or upload app to a web server and open with a mobile browser
- When testing on internet, SSL secured https protocol must be used (http won't work).
- When using a mobile as a test device log messages can be accessed by using [Chrome dev tool and remote debugging](https://developers.google.com/web/tools/chrome-devtools/remote-debugging). On android device developer settings and usb debugging must be activated.
- Uploading your files to <https://users.metropolia.fi/~MYUSERNAME/MY-FOLDER-NAME/> using command line: `scp -r dist/* MYUSERNAME@shell.metropolia.fi:public_html/MY-FOLDER-NAME/`

### Grading (0-3 points)

- Working WebAR demo published on a web server, 1 point
- Teacher's example done (with car marker & model), 1 p.
- Something extra done, own image marker and 3d models in use, clean implementation & code, 1 p.

### Returning

- Publish the application (contents of _dist/_ folder  after production build _if_ using the Webpack project) on a web server (e.g: upload to your `public_html/`) and provide a link to the image/marker used.
- Return the whole project folder as a **zip** file and a **clickable links** to your published app and the marker to Oma
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
