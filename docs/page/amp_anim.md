---
layout: page
---

### 説明

アニメーションGIFなどを表示

### 使い方

    <amp-anim 属性>
    </amp-anim>

### 必要なスクリプト

    <script async custom-element="amp-anim" src="https://cdn.ampproject.org/v0/amp-anim-0.1.js"></script>

### 属性

| 属性名       | 説明                                                   |
|--------------|--------------------------------------------------------|
| height(必須) | 高さ                                                    |
| width(必須)  | 横幅                                                   |
| src          | 画像ファイルのURL                                           |
| srcset       | デバイスの解像度で違う画像を表示                               |
| alt          | 画像ファイルを表示できなかった時の代替テキスト                         |
| attribution  | 画像の属性                                              |
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

    <amp-anim
      layout="responsive"
      height="300"
      width="400"
      src="lemur.gif">
    </amp-anim>

#### 画像の属性(attribution)

    <amp-anim
      alt="Lemurs"
      attribution="National Geographic Channel"
      layout="responsive"
      height="300"
      width="400"
      src="lemur.gif"
      object-fit="cover"
      object-position="left center">
    </amp-anim>
