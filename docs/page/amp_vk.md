---
layout: page
---

### 説明

[VK](https://vk.com/)の投稿を表示

### 使い方

    <amp-vk 属性>
    </amp-vk>

### 必要なスクリプト

    <script async custom-element="amp-vk" src="https://cdn.ampproject.org/v0/amp-vk-0.1.js"></script>

### 属性

| 属性名         | 説明                                                   |
|----------------|--------------------------------------------------------|
| data-embedtype | 埋め込みのタイプ(post or poll)                               |
| data-owner-id  | 投稿の所有者ID                                          |
| data-post-id   | 投稿の投稿ID                                            |
| data-hash      | ウィジェット接続のセキュリティハッシュ                                  |
| data-api-id    | 投票のAPI ID                                            |
| data-poll-id   | 投票ID                                                 |
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

| レイアウト名    | 説明                               |
|------------|----------------------------------|
| fixed      | 指定した横幅と高さで固定                |
| flex-item  | 親要素や周りの要素に応じて自動的にサイズ調整 |
| responsive | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### post

    <amp-vk
      width="500"
      height="300"
      data-embedtype="post"
      layout="responsive"
      data-owner-id="1"
      data-post-id="45616"
      data-hash="Yc8_Z9pnpg8aKMZbVcD-jK45eAk">
    </amp-vk>

#### poll

    <amp-vk
      width="400"
      height="300"
      layout="responsive"
      data-embedtype="poll"
      data-api-id="6183531"
      data-poll-id="274086843_1a2a465f60fff4699f">
    </amp-vk>
