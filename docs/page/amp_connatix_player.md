---
layout: page
---

### 説明

[クラウドホスト](https://www.connatix.com/)の動画プレーヤーを表示

### 使い方

    <amp-connatix-player 属性>
    </amp-connatix-player>

### 必要なスクリプト

    <script async custom-element="amp-connatix-player" src="https://cdn.ampproject.org/v0/amp-connatix-player-0.1.js"></script>

### 属性

| 属性名               | 説明                                                   |
|----------------------|--------------------------------------------------------|
| data-player-id(必須) | プレーヤーID                                                |
| data-media-id        | メディアID                                                 |
| fallback             | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights              | メディア式に基づいた要素の縦サイズ                                 |
| layout               | レイアウト                                                  |
| media                | メディア属性                                               |
| noloading            | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                   | イベントの実行用                                            |
| placeholder          | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes                | メディア式に基づいた要素の横サイズ                                 |
| width                | 横幅                                                   |
| height               | 高さ                                                    |

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

    <amp-connatix-player
      data-player-id="f721b0d8-7a79-42b6-b637-fa4e86138ed9"
      layout="responsive"
      width="150"
      height="80">
    </amp-connatix-player>

#### Media Idを指定

    <amp-connatix-player
      data-media-id="527207df-2007-43c4-b87a-f90814bafd2e"
      data-player-id="f721b0d8-7a79-42b6-b637-fa4e86138ed9"
      layout="responsive"
      width="480"
      height="270">
    </amp-connatix-player>
