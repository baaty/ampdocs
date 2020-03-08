---
layout: page
---

### 説明

glTFの3Dモデルを表示  
glTFとは、JSONによって3Dモデルやシーンを表現するフォーマット

### 使い方

    <amp-3d-gltf 属性>
    </amp-3d-gltf>

### 必要なスクリプト

    <script async custom-element="amp-3d-gltf" src="https://cdn.ampproject.org/v0/amp-3d-gltf-0.1.js"></script>

### 属性

| 属性名        | 説明                                                   | デフォルト値                 |
|---------------|--------------------------------------------------------|-------------------------|
| src(必須)     | glTFファイルのパス                                            |                         |
| alpha         | キャンバスの空きスペースを透明にするかどうか                              | false                   |
| antialiasing  | アンチエイリアスをオンにするかどうか                                     | false                   |
| clearColor    | キャンバスの空きスペースを塗りつぶす際に使用する色                        |                         |
| maxPixelRatio | pixelRatioの上限                                        | window.devicePixelRatio |
| autoRotate    | モデルの中央を中心にしてカメラを自動的に回転するかどうか                  | false                   |
| enableZoom    | ズームをオンにするかどうか                                          | true                    |
| fallback      | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |                         |
| heights       | メディア式に基づいた要素の縦サイズ                                 |                         |
| layout        | レイアウト                                                  |                         |
| media         | メディア属性                                               |                         |
| noloading     | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |                         |
| on            | イベントの実行用                                            |                         |
| placeholder   | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |                         |
| sizes         | メディア式に基づいた要素の横サイズ                                 |                         |
| width         | 横幅                                                   |                         |
| height        | 高さ                                                    |                         |

### アクション

| アクション名                                                       | 説明          |
|---------------------------------------------------------------|-------------|
| setModelRotation(x, y, z, xMin, xMax, yMin, yMax, zMin, zMax) | モデルの回転を設定 |

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| fill         | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed        | 指定した横幅と高さで固定                |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |
| flex-item    | 親要素や周りの要素に応じて自動的にサイズ調整 |
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### 基本的な使い方

    <amp-3d-gltf
      layout="fixed"
      width="320"
      height="240"
      src="/static/samples/glTF/DamagedHelmet.glb">
    </amp-3d-gltf>

#### キャンパスの空きスペースを透明(alpha)

    <amp-3d-gltf
      alpha="true"
      layout="fixed"
      width="320"
      height="240"
      src="/static/samples/glTF/DamagedHelmet.glb">
    </amp-3d-gltf>

#### アンチエイリアスをオン(antialiasing)

    <amp-3d-gltf
      antialiasing="true"
      layout="fixed"
      width="320"
      height="240"
      src="/static/samples/glTF/DamagedHelmet.glb">
    </amp-3d-gltf>

#### キャンバスの空きスペースを塗りつぶす色を変更(clearColor)

    <amp-3d-gltf
      clearColor="cyan"
      layout="fixed"
      width="320"
      height="240"
      src="/static/samples/glTF/DamagedHelmet.glb">
    </amp-3d-gltf>

#### pixelRatioの上限を設定(maxPixelRatio)

    <amp-3d-gltf
      maxPixelRatio="1.5"
      layout="fixed"
      width="320"
      height="240"
      src="/static/samples/glTF/DamagedHelmet.glb">
    </amp-3d-gltf>

#### モデルの中央を中心にしてカメラを自動的に回転(autoRotate)

    <amp-3d-gltf
      autoRotate="true"
      layout="fixed"
      width="320"
      height="240"
      src="/static/samples/glTF/DamagedHelmet.glb">
    </amp-3d-gltf>

#### ズームをOFF(enableZoom)

    <amp-3d-gltf
      enableZoom="false"
      layout="fixed"
      width="320"
      height="240"
      src="/static/samples/glTF/DamagedHelmet.glb">
    </amp-3d-gltf>

#### アクション(setModelRotation)

    <amp-3d-gltf
      id="bottle"
      layout="responsive"
      antialiasing="true"
      maxPixelRatio="1.5"
      width="240"
      height="320"
      src="https://webgears-3d.github.io/3d-gltf-static/m/WaterBottle.glb">
    </amp-3d-gltf>
    <amp-position-observer
      on="scroll:bottle.setModelRotation(z=event.percent, zMin=6.59, zMax=5.96)"
      intersection-ratios="0.6"
      layout="nodisplay">
    </amp-position-observer>
