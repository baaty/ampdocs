---
layout: page
---

### 説明

動画プレーヤーを表示

### 使い方

    <amp-video 属性>
    </amp-video>

### 必要なスクリプト

    <script async custom-element="amp-video" src="https://cdn.ampproject.org/v0/amp-video-0.1.js"></script>

### 属性

| 属性名                | 説明                                                   |
|-----------------------|--------------------------------------------------------|
| height(必須)          | 高さ                                                    |
| width(必須)           | 横幅                                                   |
| src                   | 動画ファイルのURL                                           |
| poster                | 動画の再生を開始する前に表示するサムネイル画像                     |
| autoplay              | 自動再生                                               |
| controls              | コントローラを表示                                            |
| controlsList          | インターフェイスを表示                                          |
| dock                  | 最小化                                                 |
| loop                  | ループ                                                    |
| crossorigin           | オリジン                                                   |
| disableremoteplayback | リモート再生UI                                             |
| noaudio               | 動画に音声がないことを示すアノテーション                              |
| rotate-to-fullscreen  | 横向きに回転すると、動画が全画面表示                          |
| artwork               | 動画のアートワークとして使用するサムネイル画像                          |
| artist                | 動画ファイルの作成者                                        |
| album                 | 動画のアルバム名                                            |
| title                 | 動画のタイトル                                              |
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

    <amp-video
      controls
      width="640"
      height="360"
      layout="responsive"
      poster="/static/inline-examples/images/kitten-playing.png">
      <source src="/static/inline-examples/videos/kitten-playing.webm" type="video/webm" />
      <source src="/static/inline-examples/videos/kitten-playing.mp4" type="video/mp4" />
      <div fallback>
        <p>This browser does not support the video element.</p>
      </div>
    </amp-video>

#### Media Session 属性あり

    <amp-video
      width="720"
      height="305"
      layout="responsive"
      src="https://yourhost.com/videos/myvideo.mp4"
      poster="https://yourhost.com/posters/poster.png"
      artwork="https://yourhost.com/artworks/artwork.png"
      title="Awesome video"
      artist="Awesome artist"
      album="Amazing album">
    </amp-video>

#### 横向きに回転すると、動画が全画面表示(rotate-to-fullscreen)

    <amp-video
      rotate-to-fullscreen
      layout=fill
      width=300
      height=500
      loop
      preload="metadata"
      controls>
    </amp-video>

#### 自動再生(autoplay)

    <amp-video
      autoplay
      src="https://commondatastorage.googleapis.com/gtv-videos-bucket/sample/ForBiggerJoyrides.mp4"
      width="720"
      height="405"
      layout="responsive"
      controls>
    </amp-video>
