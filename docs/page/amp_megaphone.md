---
layout: page
---

### 説明

[Megaphone.fm](https://megaphone.fm/)ポッドキャストエピソードまたはプレイリストを表示

### 使い方

    <amp-megaphone 属性>
    </amp-megaphone>

### 必要なスクリプト

    <script async custom-element="amp-megaphone" src="https://cdn.ampproject.org/v0/amp-megaphone-0.1.js"></script>

### 属性

| 属性名        | 説明                                                   |
|---------------|--------------------------------------------------------|
| data-episode  | Megaphone.fm ID                                        |
| data-playlist | プレイリストのMegaphone.fm ID                                 |
| data-start    | エピソードを開始する時間(秒)                                   |
| data-episodes | 表示するエピソードの数                                         |
| data-tile     | モード                                                    |
| data-light    | テーマ                                                    |
| data-sharing  | 共有ボタン                                                |
| width         | 横幅                                                   |
| height        | 高さ                                                    |
| fallback      | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights       | メディア式に基づいた要素の縦サイズ                                 |
| layout        | レイアウト                                                  |
| media         | メディア属性                                               |
| noloading     | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on            | イベントの実行用                                            |
| placeholder   | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes         | メディア式に基づいた要素の横サイズ                                 |

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| fixed        | 指定した横幅と高さで固定                |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |

### 例

#### 基本的な使い方

    <amp-megaphone
      height="166"
      layout="fixed-height"
      data-episode="OSC7749686951"
      data-light>
    </amp-megaphone>

#### エピソードを開始する時間(data-start)

    <amp-megaphone
      data-start="56"
      height=166
      data-episode="OSC7749686951"
      layout="fixed-height">
    </amp-megaphone>
