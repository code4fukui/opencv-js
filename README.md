# opencv-js

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

[
![NPM version](httpshttps://img.shields.io/npm/v/@techstark/opencv-js.svg)
](https://www.npmjs.com/package/@techstark/opencv-js)
[
![License](https://img.shields.io/npm/l/@techstark/opencv-js.svg)
](https://github.com/TechStark/opencv-js/blob/main/package.json)
[
![Star History](https://api.star-history.com/svg?repos=techstark/opencv-js&type=Date)
](https://star-history.com/#techstark/opencv-js&Date)

An NPM package for OpenCV.js, providing a pre-compiled version for easy use in Node.js and browser environments.

This package includes `opencv.js` from the official [OpenCV 4.10.0 release](https://docs.opencv.org/4.10.0/). The file was downloaded directly from [https://docs.opencv.org/4.10.0/opencv.js](https://docs.opencv.org/4.10.0/opencv.js).

## Key Features

-   **Pre-compiled & Ready to Use:** Includes the official `opencv.js` build for version 4.10.0.
-   **Cross-Compatible:** Works in both Node.js and browser-based projects.
-   **TypeScript Ready:** Comes with type declarations for full TypeScript support (thanks to `mirada`).
-   **Reliable API Reference:** Provides a `doc/cvKeys.json` file, a runtime-generated list of all available methods and properties.

## Live Demos

#### Image Processing (React)

A demo showcasing Canny edge detection on a static image.

-   **Live Demo & Code:** [CodeSandbox](https://codesandbox.io/s/techstarkopencv-js-demo-page-f7gvk?file=/src/TestPage.jsx)
-   **Test Image:** [Lenna.png](test/Lenna.png)

<img src="https://user-images.githubusercontent.com/132509/130320696-eaa3899b-2356-4e9f-bbc9-0a969465c58e.png" height="500px" alt="React demo showing Canny edge detection on the Lenna image" />

#### Real-time Face Detection

Detects faces from a live webcam feed.

-   **Live Demo & Code:** [CodeSandbox](https://codesandbox.io/s/opencv-js-face-detection-i1i3u)


![Real-time face detection](https://user-images.githubusercontent.com/132509/160820773-cdb023a6-77a2-4f2e-a0e9-fb06931c8f9f.gif)


#### Angular Example

-   **View Code:** [CodeSandbox](https://codesandbox.io/s/techstark-opencv-js-angular-demo-hkmc1n?file=/src/app/app.component.ts)

## Installation

```bash
npm install @techstark/opencv-js
```

or

```bash
yarn add @techstark/opencv-js
```

## Usage

Import the module into your project:

```javascript
import cv from "@techstark/opencv-js";

// For TypeScript, set "esModuleInterop": true in tsconfig.json
// or use the namespace import:
import * as cv from "@techstark/opencv-js";
```

### Browser Setup (Webpack)

When using this package in the browser with Webpack, you need to add fallbacks for Node.js core modules. In your `webpack.config.js`:

```js
module.exports = {
  // ...
  resolve: {
    fallback: {
      fs: false,
      path: false,
      crypto: false,
    },
  },
};
```

## API Reference

The included TypeScript type declarations may not be perfectly in sync with the bundled `opencv.js` version. For a definitive, runtime-verified list of all available methods and properties, please refer to the **[`doc/cvKeys.json`](doc/cvKeys.json)** file.

## Code Examples

For more complete project examples using React and Angular, see the [opencv-js-examples](https://github.com/TechStark/opencv-js-examples) repository.

## Official Documentation

For tutorials on how to use the OpenCV.js API, refer to the official [OpenCV.js Tutorials](https://docs.opencv.org/4.10.0/#:~:text=OpenCV%2DPython%20Tutorials-,OpenCV.js%20Tutorials,-Tutorials%20for%20contrib).

## License

Apache-2.0