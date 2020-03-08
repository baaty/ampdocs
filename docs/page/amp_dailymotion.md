---
layout: page
---

### 説明

[Dailymotion](https://www.dailymotion.com/)の動画プレーヤーを表示

### 使い方

    <amp-dailymotion 属性>
    </amp-dailymotion>

### 必要なスクリプト

    <script async custom-element="amp-dailymotion" src="https://cdn.ampproject.org/v0/amp-dailymotion-0.1.js"></script>

### 属性

| 属性名                | 説明                                                   |
|-----------------------|--------------------------------------------------------|
| data-videoid(必須)    | ビデオID                                                  |
| height(必須)          | 高さ                                                    |
| width(必須)           | 横幅                                                   |
| autoplay              | 自動再生                                               |
| data-mute             | ミュート                                                   |
| data-endscreen-enable | 再生終了後に関連動画を表示するか                            |
| data-sharing-enable   | シェアボタンを表示するか                                         |
| data-start            | 再生開始位置を指定(秒単位)                              |
| data-ui-highlight     | ハイライトの色                                               |
| data-ui-logo          | Dailymotionのロゴを表示するか                                 |
| data-info             | 動画のタイトルを表示するか                                      |
| data-param-\*         | Dailymotionの詳細設定                                   |
| dock                  | 最小化するか                                              |
| fallback              | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights               | メディア式に基づいた要素の縦サイズ                                 |
| layout                | レイアウト                                                  |
| media                 | メディア属性                                               |
| noloading             | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                    | イベントの実行用                                            |
| placeholder           | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes                 | メディア式に基づいた要素の横サイズ                                 |

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| fill         | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed        | 指定した横幅と高さで固定                |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |
| flex-item    | 親要素や周りの要素に応じて自動的にサイズ調整 |
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### 基本的な使い方

    <amp-dailymotion
      data-videoid="x2m8jpp"
      width="500"
      height="281">
    </amp-dailymotion>

#### layoutを指定

    <amp-dailymotion
      layout="responsive"
      data-videoid="jx2m8pp"
      width="500"
      height="281">
    </amp-dailymotion>

#### 属性設定

    <amp-dailymotion
      data-videoid="jx2m8pp"
      width="500"
      height="281"
      layout="responsive"
      data-mute="true"
      data-endscreen-enable="false"
      data-sharing-enable="true"
      data-start="42"
      data-ui-highlight="ef0122"
      data-ui-logo="false"
      data-info="true">
    </amp-dailymotion>

#### ハイライトの色を設定

    <amp-dailymotion
      data-ui-highlight="fff"
      data-videoid="jx2m8pp"
      width="500"
      height="281">
    </amp-dailymotion>
