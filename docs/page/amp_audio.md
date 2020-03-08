---
layout: page
---

### 説明

音声プレーヤー(HTML5のaudioタグ)を表示

### 使い方

    <amp-audio 属性>
    </amp-audio>

### 必要なスクリプト

    <script async custom-element="amp-audio" src="https://cdn.ampproject.org/v0/amp-audio-0.1.js"></script>

### 属性

| 属性名       | 説明                                                   |
|--------------|--------------------------------------------------------|
| src          | 音声ファイルのパス                                            |
| preload      | ページがロードされる時に音声ファイルをロードするか                           |
| autoplay     | 自動再生                                               |
| loop         | ループ再生                                                |
| muted        | デフォルトでミュート状態                                         |
| controlsList | controlsList属性                                       |
| fallback     | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights      | メディア式に基づいた要素の縦サイズ                                 |
| layout       | レイアウト                                                  |
| media        | メディア属性                                               |
| noloading    | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on           | イベントの実行用                                            |
| placeholder  | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes        | メディア式に基づいた要素の横サイズ                                 |
| width        | 横幅                                                   |
| height       | 高さ                                                    |

### メディア属性

| 属性名  | 説明           |
|---------|---------------|
| artwork | アートワーク画像のURL |
| artist  | アーティスト名       |
| album   | アルバム名         |
| title   | 曲名           |

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| fixed        | 指定した横幅と高さで固定                |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |
| nodisplay    | 要素が非表示                        |

### 例

#### メディア属性を指定

    <amp-audio
      width="400"
      height="300"
      src="https://yourhost.com/audios/myaudio.mp3"
      artwork="https://yourhost.com/artworks/artwork.png"
      title="Awesome music"
      artist="Awesome singer"
      album="Amazing album">
      <source type="audio/mpeg" src="foo.mp3" />
    </amp-audio>

#### ロード(preload)

    <amp-audio
      preload="auto"
      width="400"
      height="300"
      autoplay
      src="https://yourhost.com/audios/myaudio.mp3">
      <div fallback>
        <p>Your browser doesn’t support HTML5 audio</p>
      </div>
      <source type="audio/mpeg" src="foo.mp3">
      <source type="audio/ogg" src="foo.ogg">
    </amp-audio>

#### ボタンで曲を切り替える

    <amp-audio
      id="audio"
      width="auto"
      height="50"
      src="av/audio.mp3"
      [src]="source"
      artist="Example Artist"
      [artist]="artist"
      layout="fixed-height">
    </amp-audio>
    <button on="tap:AMP.setState({source: 'https://ccrma.stanford.edu/~jos/mp3/bachfugue.mp3'})">Change src</button>
    <button on="tap:AMP.setState({artist: 'The AMP Team'})">Set artist (Media Session)</button>

#### 再生ボタン・停止ボタン

    <amp-audio
      id="audio"
      width="auto"
      height="50"
      src="av/audio.mp3"
      artist="Example Artist"
      layout="fixed-height">
    </amp-audio>
    <button on="tap:audio.play">Play</button>
    <button on="tap:audio.pause">Pause</button>
