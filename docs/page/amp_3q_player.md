---
layout: page
---

### 説明

[3Q](https://3q.video/)の動画プレーヤーを表示

### 使い方

    <amp-3q-player 属性>
    </amp-3q-player>

### 必要なスクリプト

    <script async custom-element="amp-3q-player" src="https://cdn.ampproject.org/v0/amp-3q-player-0.1.js"></script>

### 属性

| 属性名        | 説明                                                   |
|---------------|--------------------------------------------------------|
| data-id(必須) | DataID                                                 |
| autoplay      | 自動再生                                               |
| fallback      | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights       | メディア式に基づいた要素の縦サイズ                                 |
| layout        | レイアウト                                                  |
| media         | メディア属性                                               |
| noloading     | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on            | イベントの実行用                                            |
| placeholder   | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes         | メディア式に基づいた要素の横サイズ                                 |
| width         | 横幅                                                   |
| height        | 高さ                                                    |

### レイアウト

| レイアウト名    | 説明                               |
|------------|----------------------------------|
| fill       | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed      | 指定した横幅と高さで固定                |
| flex-item  | 親要素や周りの要素に応じて自動的にサイズ調整 |
| responsive | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### 基本的な使い方

    <amp-3q-player
      data-id="c8dbe7f4-7f7f-11e6-a407-0cc47a188158"
      layout="responsive"
      width="480"
      height="270">
    </amp-3q-player>

#### 自動再生(autoplay)

    <amp-3q-player
      autoplay
      id="video"
      data-id="c8dbe7f4-7f7f-11e6-a407-0cc47a188158"
      layout="responsive"
      height="360"
      width="640">
    </amp-3q-player>
