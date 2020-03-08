---
layout: page
---

### 説明

[Viqeo](https://viqeo.tv/)の動画プレーヤーを表示

### 使い方

    <amp-viqeo-player 属性>
    </amp-viqeo-player>

### 必要なスクリプト

    <script async custom-element="amp-viqeo-player" src="https://cdn.ampproject.org/v0/amp-viqeo-player-0.1.js"></script>

### 属性

| 属性名         | 説明                                                   |
|----------------|--------------------------------------------------------|
| autoplay       | 自動再生                                               |
| data-profileid | データプロファイルID                                            |
| data-videoid   | ビデオの識別子                                             |
| width          | 横幅                                                   |
| height         | 高さ                                                    |
| fallback       | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights        | メディア式に基づいた要素の縦サイズ                                 |
| layout         | レイアウト                                                  |
| media          | メディア属性                                               |
| noloading      | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on             | イベントの実行用                                            |
| placeholder    | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes          | メディア式に基づいた要素の横サイズ                                 |
| width          | 横幅                                                   |
| height         | 高さ                                                    |

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

    <amp-viqeo-player
      data-profileid="184"
      data-videoid="b51b70cdbb06248f4438"
      width="640"
      height="360"
      layout="responsive">
    </amp-viqeo-player>

#### 自動再生(autoplay)

    <amp-viqeo-player
      width="640"
      height="400"
      data-profileid="184"
      data-videoid="922d04f30b66f1a32eb2"
      layout="responsive"
      autoplay>
    </amp-viqeo-player>
