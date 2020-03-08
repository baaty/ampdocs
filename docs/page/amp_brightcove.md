---
layout: page
---

### 説明

[ブライトコーブ(Brightcove)](https://www.brightcove.com/ja/)の動画プレーヤーを表示

### 使い方

    <amp-brightcove 属性>
    </amp-brightcove>

### 必要なスクリプト

    <script async custom-element="amp-brightcove" src="https://cdn.ampproject.org/v0/amp-brightcove-0.1.js"></script>

### 属性

| 属性名              | 説明                                                   |
|---------------------|--------------------------------------------------------|
| data-account(必須)  | アカウントID                                                |
| data-video-id(必須) | 動画ID                                                 |
| data-player         | プレーヤーID(推奨)                                          |
| data-player-id      | プレーヤーID                                                |
| data-embed          | ビデオID                                                  |
| data-playlist-id    | プレイリストID                                               |
| data-referrer       | リファラー                                                  |
| data-param-\*       | Brightcoveの詳細設定                                    |
| autoplay            | 自動再生するか                                            |
| fallback            | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights             | メディア式に基づいた要素の縦サイズ                                 |
| layout              | レイアウト                                                  |
| media               | メディア属性                                               |
| noloading           | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                  | イベントの実行用                                            |
| placeholder         | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes               | メディア式に基づいた要素の横サイズ                                 |
| width               | 横幅                                                   |
| height              | 高さ                                                    |

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

    <amp-brightcove
      id="myPlayer"
      data-referrer="EXTERNAL_REFERRER"
      data-account="1290862519001"
      data-video-id="ref:amp-docs-sample"
      data-player-id="SyIOV8yWM"
      layout="responsive" width="480" height="270">
    </amp-brightcove>
    <button on="tap:myPlayer.play">Play</button>
    <button on="tap:myPlayer.pause">Pause</button>
    <button on="tap:myPlayer.mute">Mute</button>
    <button on="tap:myPlayer.unmute">Unmute</button>
    <button on="tap:myPlayer.fullscreen">Fullscreen</button>

#### 自動再生(autoplay)

    <amp-brightcove
      id="myPlayer"
      autoplay
      data-account="1290862519001"
      data-video-id="ref:amp-docs-sample"
      data-player-id="SyIOV8yWM"
      layout="responsive" width="480" height="270">
    </amp-brightcove>
