# Software installation & setup

## Unity 3D

- Download and install Unity Hub from <https://unity3d.com/get-unity/download>
  - Install latest Unity Editor version & Visual Studio IDE
- Register for Individual license: choose personal or student

Getting started:

- [Create Your First Unity Project](https://learn.unity.com/tutorial/create-your-first-unity-project)
- [Roll-a-ball tutorial](https://learn.unity.com/project/roll-a-ball-tutorial)

---

## Tools for JavaScript & WebGL developlment

Ultimately, code editor is your choice. VSCode is recommended.

### Code editor: Visual Studio Code

- free & open source light code editor by Microsoft (**!=** Visual Studio IDE)
- wide extension support
- lightweight, multiplatform support
- good [docs & instructions](https://code.visualstudio.com/docs/editor/codebasics)
- choice of many React developers

#### Install VSCode Extensions

Press _ctrl-shift-x_ or click extensions icon on the left panel.

Search and install:

- EditorConfig for VS Code
- Auto Import
- ESLint
- JavaScript (ES6) Code Snippets

Other handy extensions:

- Duplicate file: Add _right-click -> Duplicate file_ action
- Prettier: Code formatter

#### VSCode - Basic Usage

Active **project** is the folder open on the left side panel (_File -> Open folder..._)

Handy keyboard shortcuts (finnish layout, check _File -> Preferences -> Keyboard shortcuts_ for more)

- Multiline comment: _ctrl-'_
- Delete line: _ctrl-shift-k_
- Move line(s): _alt-up/down_
- Copy line(s): _alt-shift-up/down_
- Auto format code: _alt-shift-f_
- Open integrated console: _ctrl-ö_
- [Command palette](https://code.visualstudio.com/docs/getstarted/tips-and-tricks#_command-palette): _ctrl-shift-p_
- Quick find/open files: _ctrl-p_
- Split editor: _ctrl-§_

[Visual Studio Code Tips and Tricks](https://code.visualstudio.com/docs/getstarted/tips-and-tricks)

#### VSCode - Settings

(Windows users only) Change integrated console to Bash in Windows:

1. Install [Git for Windows](https://git-scm.com/downloads) to default location
2. Edit vscode settings file (_File -> Preferences -> Settings_) and search for 'terminal'.
3. Change 'Terminal › External: Windows Exec' value to "C:\\Program Files\\Git\\bin\\bash.exe"

---

### Other option: WebStorm/PhpStorm

- free for Metropolia students. [Apply for license here](https://www.jetbrains.com/student/)
  - _@metropolia.fi_ email address needed for a free license
- full featured IDE
- quite ready out of the box. No need for plugins.
- based on IntelliJ IDEA, just like Android Studio

### Other picks

- [Atom](https://atom.io/)
- [Brackets](http://brackets.io/)
- Other IDEs like: IntelliJ Ultimate IDEA, Eclipse, NetBeans...

---

### Browser & debugging

- Chrome & [Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools/)

---

### Package Management: [NPM](https://www.npmjs.com/) - Node.js Package Manager

- Install [node.js](https://nodejs.org/en/) to get the package manager **npm**
- npm packages needed in a project (dependencies) are listed in the `package.json` file and can be install with `npm install` command
- locally installed (=project specific) packages are downloaded to `node_modules/` folder (should be excluded from version control)

---

### Building (bundling) code & automating tasks: [Webpack](https://webpack.js.org/)

>At its core, webpack is a static module bundler for modern JavaScript applications.

- module support
- local dev server
- live reload
- file loaders
- wide plugin support
- creates different bundles for local development and production deployment

Other similar tools:

- [Grunt](https://gruntjs.com/) task runner
- [Gulp](https://gulpjs.com/) automation tool

---

## Source Code Management & version control

Optional but recommended.

- Git & Github for web projects
- [Unity Collaborate](https://unity3d.com/unity/features/collaborate) (or Git) for Unity projects
