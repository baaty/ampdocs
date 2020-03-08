---
layout: page
---

### 説明

[Brid.tv](https://www.brid.tv/)の動画プレーヤーを表示

### 使い方

    <amp-brid-player 属性>
    </amp-brid-player>

### 必要なスクリプト

    <script async custom-element="amp-brid-player" src="https://cdn.ampproject.org/v0/amp-brid-player-0.1.js"></script>

### 属性

| 属性名             | 説明                                                   |
|--------------------|--------------------------------------------------------|
| data-partner(必須) | パートナーID                                                |
| data-player(必須)  | プレーヤーID                                                |
| data-video(必須)   | ビデオID                                                  |
| autoplay           | 自動再生                                               |
| data-playlist      | プレイリストID                                               |
| data-outstream     | ストリームユニットID                                            |
| data-dynamic       | ダイナミックプレイリストタイプ                                        |
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

    <amp-brid-player
      id="myVideo"
      data-partner="264"
      data-player="4144"
      data-video="13663"
      layout="responsive"
      width="480" height="270">
    </amp-brid-player>
    <button on="tap:myVideo.play">Play</button>
    <button on="tap:myVideo.pause">Pause</button>
    <button on="tap:myVideo.mute">Mute</button>
    <button on="tap:myVideo.unmute">Unmute</button>
    <button on="tap:myVideo.fullscreen">Fullscreen</button>

#### 自動再生(autoplay)

    <amp-brid-player
      autoplay
      data-partner="264"
      data-player="4144"
      data-video="13663"
      layout="responsive"
      width="480" height="270">
    </amp-brid-player>

#### ストリームユニットIDを指定(data-outstream)

    <amp-brid-player
      autoplay
      data-partner="6205"
      data-player="0"
      data-outstream="3828"
      layout="responsive"
      width="480" height="270">
    </amp-brid-player>
