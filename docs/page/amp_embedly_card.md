---
layout: page
---

### 説明

[Embedly カード](https://docs.embed.ly/docs/cards)を表示

### 使い方

    <amp-embedly-card 属性>
    </amp-embedly-card>

### 必要なスクリプト

    <script async custom-element="amp-embedly-card" src="https://cdn.ampproject.org/v0/amp-embedly-card-0.1.js"></script>

### 属性

| 属性名              | 説明                                                   |
|---------------------|--------------------------------------------------------|
| data-url(必須)      | 埋め込み情報を取得するURL                                   |
| data-card-via       | カードのビアコンテンツ                                            |
| data-card-theme     | テーマ                                                    |
| data-card-embed     | ビデオまたはリッチメディアへのURL                                     |
| data-card-image     | 画像のURL                                               |
| data-card-controls  | 共有アイコンを有効にするか                                      |
| data-card-align     | カードの表示方法                                           |
| data-card-recommend | 埋め込みの推奨を有効にするか                                   |
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

| レイアウト名    | 説明                       |
|------------|--------------------------|
| responsive | 画面サイズに応じて自動的にサイズ調整 |

### 例

#### 基本的な使い方

    <amp-embedly-card
      data-url="https://www.youtube.com/watch?v=lBTCB7yLs8Y"
      layout="responsive"
      width="100"
      height="50">
    </amp-embedly-card>

#### テーマを指定

    <amp-embedly-card
      data-url="https://twitter.com/AMPhtml/status/986750295077040128"
      layout="responsive"
      width="150"
      height="80"
      data-card-theme="dark"
      data-card-controls="0">
    </amp-embedly-card>
