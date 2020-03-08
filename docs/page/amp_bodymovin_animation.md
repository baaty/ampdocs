---
layout: page
---

### 説明

Adobe After Effectsで生成されたJSONからアニメーションを表示

### 使い方

    <amp-bodymovin-animation 属性>
    </amp-bodymovin-animation>

### 必要なスクリプト

    <script async custom-element="amp-bodymovin-animation" src="https://cdn.ampproject.org/v0/amp-bodymovin-animation-0.1.js"></script>

### 属性

| 属性名      | 必須                                                   |
|-------------|--------------------------------------------------------|
| src(必須)   | ファイルへのパス                                               |
| loop        | ループするか                                                 |
| noautoplay  | 自動再生OFFにするか                                        |
| renderer    | 専用のレンダリング                                            |
| fallback    | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights     | メディア式に基づいた要素の縦サイズ                                 |
| layout      | レイアウト                                                  |
| media       | メディア属性                                               |
| noloading   | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on          | イベントの実行用                                            |
| placeholder | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes       | メディア式に基づいた要素の横サイズ                                 |
| width       | 横幅                                                   |
| height      | 高さ                                                    |

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| fill         | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed        | 指定した横幅と高さで固定                |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |
| flex-item    | 親要素や周りの要素に応じて自動的にサイズ調整 |
| nodisplay    | 要素が非表示                        |
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### 基本的な使い方

    <amp-bodymovin-animation
      layout="fixed"
      width="200"
      height="200"
      src="https://nainar.github.io/loader.json">
    </amp-bodymovin-animation>

#### 5回ループ

    <amp-bodymovin-animation
      layout="fixed"
      width="200"
      height="200"
      src="https://nainar.github.io/loader.json"
      loop="5">
    </amp-bodymovin-animation>

#### 自動再生OFF

    <amp-bodymovin-animation
      id="anim"
      layout="fixed"
      width="200"
      height="200"
      src="https://nainar.github.io/loader.json"
      loop="true"
      name="ripple_1"
      noautoplay>
    </amp-bodymovin-animation>

#### renderer属性

    <amp-bodymovin-animation
      renderer="html"
      layout="fixed"
      width="200"
      height="200"
      src="https://nainar.github.io/loader.json"
      loop>
    </amp-bodymovin-animation>
