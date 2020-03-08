---
layout: page
---

### 説明

nexxOMNIAプラットフォームからのメディアストリームを表示

### 使い方

    <amp-nexxtv-player 属性>
    </amp-nexxtv-player>

### 必要なスクリプト

    <script async custom-element="amp-nexxtv-player" src="https://cdn.ampproject.org/v0/amp-nexxtv-player-0.1.js"></script>

### 属性

| 属性名                | 説明                                                   |
|-----------------------|--------------------------------------------------------|
| data-mediaid(必須)    | 再生するメディアのID                                          |
| data-client(必須)     | ドメインID                                                 |
| data-streamtype       | メディアストリーミングタイプ                                         |
| data-seek-to          | メディアの開始点                                            |
| data-mode             | データモード                                                 |
| data-origin           | ドメインメディア                                               |
| data-disable-ads      | 広告を有効になっているか                                       |
| data-streaming-filter | ストリーミングフィルター                                           |
| fallback              | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights               | メディア式に基づいた要素の縦サイズ                                 |
| layout                | レイアウト                                                  |
| media                 | メディア属性                                               |
| noloading             | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                    | イベントの実行用                                            |
| placeholder           | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes                 | メディア式に基づいた要素の横サイズ                                 |
| width                 | 横幅                                                   |
| height                | 高さ                                                    |

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

    <amp-nexxtv-player
      data-mediaid="71QQG852413DU7J"
      data-client="761"
      data-streamtype="video"
      data-seek-to="2"
      data-mode="static"
      data-origin="https://embed.nexx.cloud/"
      data-disable-ads="1"
      data-streaming-filter="nxp-bitrate-2500"
      layout="responsive"
      width="480"
      height="270">
    </amp-nexxtv-player>
