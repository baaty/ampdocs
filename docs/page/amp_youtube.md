---
layout: page
---

### 説明

YouTubeの動画プレーヤーを表示

### 使い方

    <amp-youtube 属性>
    </amp-youtube>

### 必要なスクリプト

    <script async custom-element="amp-youtube" src="https://cdn.ampproject.org/v0/amp-youtube-0.1.js"></script>

### 属性

| 属性名              | 説明                                                   |
|---------------------|--------------------------------------------------------|
| autoplay            | 自動再生                                               |
| data-videoid        | YouTube動画ID                                          |
| data-live-channelid | YouTubeチャンネルID                                         |
| data-param-\*       | パラメータ                                                  |
| dock                | 最小化                                                 |
| credentials         | 証明書                                                 |
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

    <amp-youtube
      width="480"
      height="270"
      data-videoid="dQw4w9WgXcQ">
    </amp-youtube>

#### 自動再生(autoplay)

    <amp-youtube
      autoplay
      data-videoid="lBTCB7yLs8Y"
      width="358"
      height="204"
      layout="responsive">
    </amp-youtube>

#### Live Channel Id

    <amp-youtube
      id="myLiveChannel"
      data-live-channelid="UCB8Kb4pxYzsDsHxzBfnid4Q"
      width="358"
      height="204"
      layout="responsive">
      <amp-img
        src="https://i.ytimg.com/vi/Wm1fWz-7nLQ/hqdefault_live.jpg"
        placeholder
        layout="fill"/>
    </amp-youtube>

#### loop

    <amp-youtube
      loop
      width="480"
      height="270"
      data-videoid="dQw4w9WgXcQ">
    </amp-youtube>
