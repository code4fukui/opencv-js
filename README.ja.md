# opencv-js

[
![NPMバージョン](httpshttps://img.shields.io/npm/v/@techstark/opencv-js.svg)
](https://www.npmjs.com/package/@techstark/opencv-js)
[
![ライセンス](https://img.shields.io/npm/l/@techstark/opencv-js.svg)
](https://github.com/TechStark/opencv-js/blob/main/package.json)
[
![スター履歴](https://api.star-history.com/svg?repos=techstark/opencv-js&type=Date)
](https://star-history.com/#techstark/opencv-js&Date)

Node.jsおよびブラウザ環境で簡単に利用できるよう、コンパイル済みのOpenCV.jsを提供するNPMパッケージです。

このパッケージには、公式の[OpenCV 4.10.0リリース](https://docs.opencv.org/4.10.0/)の `opencv.js` が含まれています。このファイルは [https://docs.opencv.org/4.10.0/opencv.js](https://docs.opencv.org/4.10.0/opencv.js) から直接ダウンロードしたものです。

## 主な機能

-   **コンパイル済みですぐに使える:** バージョン4.10.0の公式 `opencv.js` ビルドが含まれています。
-   **クロスプラットフォーム対応:** Node.jsとブラウザベースのプロジェクトの両方で動作します。
-   **TypeScript対応:** 完全なTypeScriptサポートのための型宣言ファイルが同梱されています（`mirada` に感謝）。
-   **信頼性の高いAPIリファレンス:** 実行時に生成された、利用可能なすべてのメソッドとプロパティのリストである `doc/cvKeys.json` ファイルを提供します。

## ライブデモ

#### 画像処理 (React)

静止画に対するCannyエッジ検出のデモです。

-   **ライブデモ & コード:** [CodeSandbox](https://codesandbox.io/s/techstarkopencv-js-demo-page-f7gvk?file=/src/TestPage.jsx)
-   **テスト画像:** [Lenna.png](test/Lenna.png)

<img src="https://user-images.githubusercontent.com/132509/130320696-eaa3899b-2356-4e9f-bbc9-0a969465c58e.png" height="500px" alt="Lenna画像に対するCannyエッジ検出を示すReactデモ" />

#### リアルタイム顔検出

Webカメラのライブ映像から顔を検出します。

-   **ライブデモ & コード:** [CodeSandbox](https://codesandbox.io/s/opencv-js-face-detection-i1i3u)

![リアルタイム顔検出](https://user-images.githubusercontent.com/132509/160820773-cdb023a6-77a2-4f2e-a0e9-fb06931c8f9f.gif)

#### Angularの例

-   **コードを見る:** [CodeSandbox](https://codesandbox.io/s/techstark-opencv-js-angular-demo-hkmc1n?file=/src/app/app.component.ts)

## インストール

```bash
npm install @techstark/opencv-js
```

または

```bash
yarn add @techstark/opencv-js
```

## 使い方

プロジェクトにモジュールをインポートします:

```javascript
import cv from "@techstark/opencv-js";

// TypeScriptの場合は、tsconfig.jsonで "esModuleInterop": true を設定するか、
// 以下のように名前空間インポートを使用してください:
import * as cv from "@techstark/opencv-js";
```

### ブラウザでの設定 (Webpack)

Webpackを使用してブラウザ環境でこのパッケージを利用する場合、Node.jsのコアモジュールに対するフォールバックを追加する必要があります。`webpack.config.js` に以下を追記してください:

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

## APIリファレンス

同梱されているTypeScriptの型宣言は、バンドルされている `opencv.js` のバージョンと完全に同期していない場合があります。実行時に検証された、利用可能なすべてのメソッドとプロパティの正確なリストについては、**[`doc/cvKeys.json`](doc/cvKeys.json)** ファイルを参照してください。

## コード例

ReactやAngularを使用したより完全なプロジェクト例については、[opencv-js-examples](https://github.com/TechStark/opencv-js-examples) リポジトリを参照してください。

## 公式ドキュメント

OpenCV.js APIの使い方のチュートリアルについては、公式の [OpenCV.js Tutorials](https://docs.opencv.org/4.10.0/#:~:text=OpenCV%2DPython%20Tutorials-,OpenCV.js%20Tutorials,-Tutorials%20for%20contrib) を参照してください。

## ライセンス

Apache-2.0
