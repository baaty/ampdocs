---
layout: page
---

### 説明

[Powr](https://powr.com/)のプレーヤーを表示

### 使い方

    <amp-powr-player 属性>
    </amp-powr-player>

### 必要なスクリプト

    <script async custom-element="amp-powr-player" src="https://cdn.ampproject.org/v0/amp-powr-player-0.1.js"></script>

### 属性

| 属性名             | 説明                                                   |
|--------------------|--------------------------------------------------------|
| data-account(必須) | アカウントID                                                |
| data-player(必須)  | プレーヤーID                                                |
| data-video         | ビデオID                                                  |
| data-terms         | 表示するページを説明するキーワード                                  |
| data-referrer      | リファラー                                                  |
| data-param-\*      | Powrへのパラメータ                                            |
| autoplay           | 自動再生                                               |
| fallback           | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights            | メディア式に基づいた要素の縦サイズ                                 |
| layout             | レイアウト                                                  |
| media              | メディア属性                                               |
| noloading          | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                 | イベントの実行用                                            |
| placeholder        | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes              | メディア式に基づいた要素の横サイズ                                 |
| width              | 横幅                                                   |
| height             | 高さ                                                    |

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

    <amp-powr-player
      data-account="12345"
      data-player="12345"
      data-video="12345"
      layout="responsive"
      width="480"
      height="270">
    </amp-powr-player>
