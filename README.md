## Khipu

Named after [recording devices](https://en.wikipedia.org/wiki/Quipu) fashioned from strings, Khipu is an experimental port of Twine, a tool for telling interactive, nonlinear stories, to Tauri from Electron. It is intended as a soft fork that is backwards-compatible with the latest stable releases.

### KNOWN ISSUES

- In-app (for lack of a better word) debugging, exporting files and hyperlinks doesn't work.

### SYNOPSIS

The story formats in minified format under `story-formats/` exist in separate
repositories:

-   [Harlowe](https://foss.heptapod.net/games/harlowe/)
-   [Paperthin](https://github.com/klembot/paperthin)
-   [Snowman](https://github.com/klembot/snowman)
-   [SugarCube](https://github.com/tmedwards/sugarcube-2)

#### BUILDS

Binary packages for Twine are available on the [Releases](https://github.com/tonytins/Khipu/releases) tab for Windows, MacOS
and Linux. As always, only install from sources you trust.

### INSTALL

Run `npm install` at the top level of the directory to install all goodies.

Working with the documentation requires installing
[mdbook](https://rust-lang.github.io/mdBook/), which is not a Node-based
project. You can either install it directly from the project web site or use
your operating system's package manager.

### BUILDING

Run `npm start` to begin serving a development version of Twine locally. This
server will automatically update with changes you make.

Run `npm run start:tauri` to run a development version of the Tauri app. **Running this can damage files in your Twine storied folder. Take a backup copy of this folder before proceeding.** Most of the app will automatically update as you work, but if you want the app to read story files initially again, you will need to restart the process.

To create a release, run `npm run build:tauri`. Finished files will be found under `src-tauri/target`.

`npm test` will test the source code respectively.

`npm run clean` will delete existing files in `electron-build/` and `dist/`.

## Credits

By Chris Klimas, Lorenzo Ancora, Leon Arnott, Daithi O Crualaoich, Ingrid Cheung, Thomas Michael Edwards, Micah Fitch, Juhana Leinonen, Michael Savich, and Ross Smith