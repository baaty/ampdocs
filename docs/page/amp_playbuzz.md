---
layout: page
---

### 説明

[Playbuzz](http://www.playbuzz.com/)の動画プレーヤーを表示

### 使い方

    <amp-playbuzz 属性>
    </amp-playbuzz>

### 必要なスクリプト

    <script async custom-element="amp-playbuzz" src="https://cdn.ampproject.org/v0/amp-playbuzz-0.1.js"></script>

### 属性

| 属性名             | 説明                                                   |
|--------------------|--------------------------------------------------------|
| src                | PlaybuzzアイテムのURL                                       |
| data-item          | PlaybuzzアイテムのアイテムID                                    |
| data-item-info     | 作成日、作成者名などのデータ情報を表示するかどうか                   |
| data-share-buttons | 共有ボタンを表示するかどうか                                     |
| data-comments      | ユーザーのコメントを表示するかどうか                                   |
| fallback           | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights            | メディア式に基づいた要素の縦サイズ                                 |
| layout             | レイアウト                                                  |
| media              | メディア属性                                               |
| noloading          | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                 | イベントの実行用                                            |
| placeholder        | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes              | メディア式に基づいた要素の横サイズ                                 |
| width              | 横幅                                                   |
| height             | 高さ                                                    |

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### data-item

    <amp-playbuzz
      data-item="a6aa5a14-8888-4618-b2e3-fe6a30d8c51b"
      layout="responsive"
      height="300"
      width="300"
      data-item-info="false"
      data-share-buttons="false"
      data-comments="false">
    </amp-playbuzz>

#### src

    <amp-playbuzz
      src="https://www.playbuzz.com/HistoryUK/10-classic-christmas-movies"
      layout="responsive"
      height="300"
      width="300"
      data-item-info="false"
      data-share-buttons="false"
      data-comments="false">
    </amp-playbuzz>
