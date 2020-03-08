---
layout: page
---

### 説明

インラインフレームを表示

### 使い方

    <amp-iframe 属性>
    </amp-iframe>

### 必要なスクリプト

    <script async custom-element="amp-iframe" src="https://cdn.ampproject.org/v0/amp-iframe-0.1.js"></script>

### 属性

| 属性名            | 説明                                                   |
|-------------------|--------------------------------------------------------|
| src               | コンテンツのURL                                              |
| srcdoc            | コンテンツのURL。src属性よりも優先                               |
| frameborder       | フレームの枠                                                |
| allowfullscreen   | フルスクリーンを許可するかどうか                                     |
| allowtransparency | インラインフレームの背景を透過にするかどうか                             |
| referrerpolicy    | 読み込む際にリファラーの送信方法をキーワードで指定                     |
| sandbox           | センドボックス                                                |
| fallback          | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights           | メディア式に基づいた要素の縦サイズ                                 |
| layout            | レイアウト                                                  |
| media             | メディア属性                                               |
| noloading         | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                | イベントの実行用                                            |
| placeholder       | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes             | メディア式に基づいた要素の横サイズ                                 |
| width             | 横幅                                                   |
| height            | 高さ                                                    |

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

    <amp-iframe
      width="200"
      height="200"
      src="https://example.com">
    </amp-iframe>

#### 属性を指定

    <amp-iframe
      width="200"
      height="200"
      src="https://example.com"
      allow="geolocation; microphone"
      allowfullscreen
      allowpaymentrequest
      allowtransparency
      frameborder="0"
      referrerpolicy="origin"
      tabindex="-1"
      resizable
      sandbox="allow-same-origin allow-scripts"
      scrolling="no">
    </amp-iframe>
