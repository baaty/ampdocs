---
layout: page
---

### 説明

レスポンシブレイアウト

### 使い方

    <amp-layout 属性>
    </amp-layout>

### 必要なスクリプト

    <script async custom-element="amp-kaltura-player" src="https://cdn.ampproject.org/v0/amp-kaltura-player-0.1.js"></script>

### 属性

| 属性名      | 説明                                                   |
|-------------|--------------------------------------------------------|
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
| container    | 子要素に応じて自動的にサイズ調整          |
| fill         | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed        | 指定した横幅と高さで固定                |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |
| flex-item    | 親要素や周りの要素に応じて自動的にサイズ調整 |
| intrinsic    | 指定したアスペクト比に自動的にサイズ調整       |
| nodisplay    | 要素が非表示                        |
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### 基本的な使い方

    <amp-layout
      layout="responsive"
      width="2"
      height="1">
      This `amp-layout` acts like a `div` that always keeps a `2x1` aspect ratio.
    </amp-layout>
