---
layout: page
---

### 説明

AOL O2 の動画プレーヤーを表示

### 使い方

    <amp-o2-player 属性>
    </amp-o2-player>

### 必要なスクリプト

    <script async custom-element="amp-o2-player" src="https://cdn.ampproject.org/v0/amp-o2-player-0.1.js"></script>

### 属性

| 属性名          | 説明                                                   |
|-----------------|--------------------------------------------------------|
| data-bcid(必須) | Buyer Company ID                                       |
| data-pid(必須)  | プレーヤー ID                                               |
| data-bid(必須)  | プレイリスト ID                                              |
| data-macros     | macros                                                 |
| data-vid        | 動画 ID                                                |
| fallback        | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights         | メディア式に基づいた要素の縦サイズ                                 |
| layout          | レイアウト                                                  |
| media           | メディア属性                                               |
| noloading       | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on              | イベントの実行用                                            |
| placeholder     | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes           | メディア式に基づいた要素の横サイズ                                 |
| width           | 横幅                                                   |
| height          | 高さ                                                    |

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

    <amp-o2-player
      data-pid="573d9bf1e4b02a3388f42c36"
      data-bcid="50d595ec0364e95588c77bd2"
      layout="responsive" width="480" height="270">
    </amp-o2-player>

#### data-macros

    <amp-o2-player
      data-pid="573d9bf1e4b02a3388f42c36"
      data-bcid="50d595ec0364e95588c77bd2"
      data-bid="573d9bd3e4b00df34e4325ed"
      data-macros="m.playertype=HTML5"
      layout="responsive" width="480" height="270">
    </amp-o2-player>
