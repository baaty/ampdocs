---
layout: page
---

### 説明

ミニッツメディアプレーヤーを表示

### 使い方

    <amp-minute-media-player 属性>
    </amp-minute-media-player>

### 必要なスクリプト

    <script async custom-element="amp-minute-media-player" src="https://cdn.ampproject.org/v0/amp-minute-media-player-0.1.js"></script>

### 属性

| 属性名                    | 説明                                                   |
|---------------------------|--------------------------------------------------------|
| data-content-type         | Minute Mediaプレーヤーのタイプ                                  |
| data-content-id           | Minute MediaプレーヤーID                                    |
| data-scanned-element-type | 特性                                                   |
| data-scanned-element      | 選択されたスキャン要素タイプ                                     |
| data-tags                 | タグ                                                     |
| data-minimum-date-factor  | 最後の日数                                              |
| data-scoped-keywords      | タグ                                                     |
| autoplay                  | 自動再生                                               |
| dock                      | 最小化                                                 |
| fallback                  | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights                   | メディア式に基づいた要素の縦サイズ                                 |
| layout                    | レイアウト                                                  |
| media                     | メディア属性                                               |
| noloading                 | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                        | イベントの実行用                                            |
| placeholder               | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes                     | メディア式に基づいた要素の横サイズ                                 |
| width                     | 横幅                                                   |
| height                    | 高さ                                                    |

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

    <amp-minute-media-player
      data-content-type="curated"
      data-content-id="fSkmeWKF"
      width="500"
      height="334"
      layout="responsive"
      autoplay>
    </amp-minute-media-player>
