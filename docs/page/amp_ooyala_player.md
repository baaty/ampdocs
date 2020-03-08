---
layout: page
---

### 説明

[Ooyala](https://www.ooyala.com/)の動画プレーヤーを表示

### 使い方

    <amp-ooyala-player 属性>
    </amp-ooyala-player>

### 必要なスクリプト

    <script async custom-element="amp-ooyala-player" src="https://cdn.ampproject.org/v0/amp-ooyala-player-0.1.js"></script>

### 属性

| 属性名               | 説明                                                   |
|----------------------|--------------------------------------------------------|
| data-embedcode(必須) | Backlotのビデオ埋め込みコード                                   |
| data-playerid(必須)  | プレーヤーID                                                |
| data-pcode(必須)     | プロバイダーコード                                              |
| data-playerversion   | プレイヤーのバージョン                                            |
| data-config          | カスタム設定のURL                                           |
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
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### 基本的な使い方

    <amp-ooyala-player
      data-embedcode="Vxc2k0MDE6Y_C7J5podo3UDxlFxGaZrQ"
      data-pcode="5zb2wxOlZcNCe_HVT3a6cawW298X"
      data-playerid="6440813504804d76ba35c8c787a4b33c"
      width="640"
      height="360">
    </amp-ooyala-player>
