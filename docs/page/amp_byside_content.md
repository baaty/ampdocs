---
layout: page
---

### 説明

[BySide](http://www.byside.com/)の動画プレーヤーを表示

### 使い方

    <amp-byside-content 属性>
    </amp-byside-content>

### 必要なスクリプト

    <script async custom-element="amp-byside-content" src="https://cdn.ampproject.org/v0/amp-byside-content-0.1.js"></script>

### 属性

| 属性名                | 説明                                                   |
|-----------------------|--------------------------------------------------------|
| data-webcare-id(必須) | 顧客アカウントID                                            |
| data-label(必須)      | コンテンツラベル                                               |
| data-lang             | コンテンツを表示する言語                                       |
| data-channel          | チャネル識別子                                             |
| data-fid              | ビジターフォースID                                             |
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

    <amp-byside-content
      data-webcare-id="D6604AE5D0"
      data-lang="en"
      data-label="amp-responsive"
      layout="responsive"
      height="500"
      width="1024">
    </amp-byside-content>

#### 言語指定

    <amp-byside-content
      data-webcare-id="D6604AE5D0"
      data-label="amp-simple"
      height="300"
      layout="fixed-height">
    </amp-byside-content>
