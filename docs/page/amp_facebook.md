---
layout: page
---

### 説明

Facebookの投稿や動画を表示

### 使い方

    <amp-facebook 属性>
    </amp-facebook>

### 必要なスクリプト

    <script async custom-element="amp-facebook" src="https://cdn.ampproject.org/v0/amp-facebook-0.1.js"></script>

### 属性

| 属性名                      | 説明                                                   | デフォルト値 |
|-----------------------------|--------------------------------------------------------|---------|
| data-href(必須)             | コンテンツのURL                                              |         |
| height(必須)                | 高さ                                                    |         |
| width(必須)                 | 横幅                                                   |         |
| data-embed-as               | コンテンツの種類。投稿(post)、動画(video)、コメント(comment)        | post    |
| data-include-comment-parent | コメントの返信を表示するか                                      | false   |
| data-align-center           | 中央揃えにするか                                            | false   |
| data-locale                 | ロケール                                                   |         |
| fallback                    | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |         |
| heights                     | メディア式に基づいた要素の縦サイズ                                 |         |
| layout                      | レイアウト                                                  |         |
| media                       | メディア属性                                               |         |
| noloading                   | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |         |
| on                          | イベントの実行用                                            |         |
| placeholder                 | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |         |
| sizes                       | メディア式に基づいた要素の横サイズ                                 |         |
| width                       | 横幅                                                   |         |
| height                      | 高さ                                                    |         |

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

    <amp-facebook
      width=486
      height=657
      layout="responsive"
      data-href="https://www.facebook.com/zuck/posts/10102593740125791">
    </amp-facebook>

#### ロケール(data-locale)

    <amp-facebook
      width=486
      height=657
      layout="responsive"
      data-href="https://www.facebook.com/zuck/posts/10102593740125791"
      data-locale="fr_FR">
    </amp-facebook>

#### 動画(video)

    <amp-facebook
      width=552
      height=574
      layout="responsive"
      data-embed-as="video"
      data-href="https://www.facebook.com/zuck/videos/10102509264909801/">
    </amp-facebook>

#### コメント(comment)

    <amp-facebook
      width=552
      height=200
      layout="responsive"
      data-embed-as="comment"
      data-include-parent="true"
      data-href="https://www.facebook.com/zuck/posts/10102735452532991?comment_id=717538375088203">
    </amp-facebook>

#### 中央揃え(data-align-center)

    <amp-facebook
      width=552
      height=350
      layout="responsive"
      data-href="https://www.facebook.com/notes/facebook-engineering/under-the-hood-the-javascript-sdk-truly-asynchronous-loading/10151176218703920/"
      data-align-center="true">
    </amp-facebook>
