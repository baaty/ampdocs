---
layout: page
---

### 説明

[Springboard](http://publishers.springboardplatform.com/)の動画プレーヤーを表示

### 使い方

    <amp-springboard-player 属性>
    </amp-springboard-player>

### 必要なスクリプト

    <script async custom-element="amp-springboard-player" src="https://cdn.ampproject.org/v0/amp-springboard-player-0.1.js"></script>

### 属性

| 属性名                | 説明                                                   |
|-----------------------|--------------------------------------------------------|
| data-site-id(必須)    | SpringBoardサイトID                                       |
| data-mode(必須)       | SpringBoardプレーヤーモード                                    |
| data-content-id(必須) | SpringBoardプレーヤーのコンテンツID                               |
| data-player-id(必須)  | スプリングボードプレーヤーID                                        |
| data-domain(必須)     | Springboardパートナードメイン                                   |
| data-items(必須)      | 再生リスト内の動画の数                                      |
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

| レイアウト名    | 説明                               |
|------------|----------------------------------|
| fill       | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed      | 指定した横幅と高さで固定                |
| flex-item  | 親要素や周りの要素に応じて自動的にサイズ調整 |
| responsive | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### 基本的な使い方

    <amp-springboard-player
      data-site-id="261"
      data-mode="video"
      data-content-id="1578473"
      data-player-id="test401"
      data-domain="test.com"
      data-items="10"
      layout="responsive"
      width="480"
      height="270">
    </amp-springboard-player>
