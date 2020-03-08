---
layout: page
---

### 説明

[AddThis](https://www.addthis.com/)のコンテンツを表示  
AddThisは、ソーシャルボタンをまとめて設置できるサービス

### 使い方

    <amp-addthis 属性>
    </amp-addthis>

### 必要なスクリプト

    <script async custom-element="amp-addthis" src="https://cdn.ampproject.org/v0/amp-addthis-0.1.js"></script>

### 属性

| 属性名                 | 説明                                                   |
|------------------------|--------------------------------------------------------|
| data-pub-id(必須)      | サイト運営者ID                                            |
| data-widget-id(必須)   | ウィジェットID                                               |
| data-widget-type(必須) | ウィジェットタイプ                                              |
| data-title             | タイトル                                                   |
| data-url               | URL                                                    |
| data-media             | 画像や動画のURL                                          |
| data-description       | 説明                                                   |
| fallback               | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights                | メディア式に基づいた要素の縦サイズ                                 |
| layout                 | レイアウト                                                  |
| media                  | メディア属性                                               |
| noloading              | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                     | イベントの実行用                                            |
| placeholder            | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes                  | メディア式に基づいた要素の横サイズ                                 |
| width                  | 横幅                                                   |
| height                 | 高さ                                                    |

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

#### フローティング

    <amp-addthis
      width="320"
      layout="responsive"
      data-pub-id="ra-5c191331410932ff"
      data-widget-id="957l"
      data-widget-type="floating">
    </amp-addthis>

#### インライン

    <amp-addthis
      width="320"
      height="92"
      data-pub-id="ra-5c191331410932ff"
      data-widget-id="mv93"
      data-widget-type="inline">
    </amp-addthis>
