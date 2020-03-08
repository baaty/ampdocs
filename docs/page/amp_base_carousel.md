---
layout: page
---

### 説明

カルーセルを表示

### 使い方

    <amp-base-carousel 属性>
    </amp-base-carousel>

### 必要なスクリプト

    <script async custom-element="amp-base-carousel" src="https://cdn.ampproject.org/v0/amp-base-carousel-0.1.js"></script>

### 属性

| 属性名                | 説明                                                   | デフォルト値 |
|-----------------------|--------------------------------------------------------|---------|
| attr-name             | 構成要素                                               |         |
| mixed-length          | 各スライドに既存の幅を使用するか                                 | false   |
| visible-count         | 特定の時間に表示するスライド数                                 | 1       |
| advance-count         | 次に移動する時に進むスライド数                                  | 1       |
| auto-advance          | 自動的に進む                                             | false   |
| auto-advance-count    | 自動的に進む時のスライド数                                    | 1       |
| auto-advance-interval | 自動的に進む時の時間(ミリ秒)                                | 1000    |
| auto-advance-loops    | ループ回数                                                | 無限    |
| snap                  | スクロール時にカルーセルがスライドにスナップするかどうか                          | true    |
| snap-align            | スライドの位置(startかcenter)                                | start   |
| snap-by               | スナップの粒度                                              | 1       |
| slide                 | 表示される最初のスライド                                       | 0       |
| loop                  | ループするか                                                 | true    |
| horizontal            | 水平レイアウトにするか                                          | true    |
| fallback              | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |         |
| heights               | メディア式に基づいた要素の縦サイズ                                 |         |
| layout                | レイアウト                                                  |         |
| media                 | メディア属性                                               |         |
| noloading             | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |         |
| on                    | イベントの実行用                                            |         |
| placeholder           | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |         |
| sizes                 | メディア式に基づいた要素の横サイズ                                 |         |
| width                 | 横幅                                                   |         |
| height                | 高さ                                                    |         |

### イベント

| イベント名      | 説明                                  |
|-------------|-------------------------------------|
| slideChange | カルーセルによって表示されるインデックスが変更されたときに実行 |

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| fill         | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed        | 指定した横幅と高さで固定                |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |
| flex-item    | 親要素や周りの要素に応じて自動的にサイズ調整 |
| intrinsic    | 指定したアスペクト比に自動的にサイズ調整       |
| nodisplay    | 要素が非表示                        |
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### 基本的な使い方

    <amp-base-carousel
      width="4"
      height="3">
    </amp-base-carousel>

#### 自動的に進む(auto-advance)

    <amp-base-carousel
      auto-advance="true"
      width="4"
      height="3">
    </amp-base-carousel>

#### media query

    <amp-base-carousel
      auto-advance="(min-width: 800px) true, false">
      width="4"
      height="3"
    </amp-base-carousel>

#### multiple media queries

    <amp-base-carousel
      auto-advance="(min-width: 800px) true, (max-height: 1000px) true, false"
      width="4"
      height="3">
    </amp-base-carousel>

#### 次に移動する時に進むスライド数(advance-count)

    <amp-base-carousel
      advance-count="2"
      width="4"
      height="3">
    </amp-base-carousel>

#### 特定の時間に表示するスライド数(visible-count)

    <amp-base-carousel
      visible-count="2"
      width="4"
      height="3">
    </amp-base-carousel>

#### 少数

    <amp-base-carousel
      visible-count="3.2"
      width="4"
      height="3">
    </amp-base-carousel>
