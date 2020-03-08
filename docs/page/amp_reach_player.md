---
layout: page
---

### 説明

[Beachfront Reach](http://beachfrontreach.com/)の動画プレーヤーを表示

### 使い方

    <amp-reach-player 属性>
    </amp-reach-player>

### 必要なスクリプト

    <script async custom-element="amp-reach-player" src="https://cdn.ampproject.org/v0/amp-reach-player-0.1.js"></script>

### 属性

| 属性名              | 説明                                                   |
|---------------------|--------------------------------------------------------|
| data-embed-id(必須) | 埋め込みID                                               |
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
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### 基本的な使い方

    <amp-reach-player
      data-embed-id="default"
      layout="responsive"
      width="560"
      height="315">
    </amp-reach-player>
