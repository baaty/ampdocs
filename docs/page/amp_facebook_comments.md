---
layout: page
---

### 説明

Facebookのコメントを表示

### 使い方

    <amp-facebook-comments 属性>
    </amp-facebook-comments>

### 必要なスクリプト

    <script async custom-element="amp-facebook-comments" src="https://cdn.ampproject.org/v0/amp-facebook-comments-0.1.js"></script>

### 属性

| 属性名           | 説明                                                   |
|------------------|--------------------------------------------------------|
| data-href(必須)  | コメントページのURL                                            |
| data-locale      | ロケール                                                   |
| data-numposts    | 表示するコメントの数                                          |
| data-order-by    | コメントを表示するときに使用する順序                               |
| data-colorscheme | カラー                                                    |
| fallback         | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights          | メディア式に基づいた要素の縦サイズ                                 |
| layout           | レイアウト                                                  |
| media            | メディア属性                                               |
| noloading        | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on               | イベントの実行用                                            |
| placeholder      | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes            | メディア式に基づいた要素の横サイズ                                 |
| width            | 横幅                                                   |
| height           | 高さ                                                    |

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

    <amp-facebook-comments
      width=486
      height=657
      layout="responsive"
      data-href="http://www.directlyrics.com/adele-25-complete-album-lyrics-news.html">
    </amp-facebook>

#### time

    <amp-facebook-comments width=552 height=310
      layout="responsive"
      data-numposts="5"
      data-order-by="time"
      data-href="https://developers.facebook.com/docs/plugins/comments">
    </amp-facebook-comments>

#### social

    <amp-facebook-comments width=552 height=310
      layout="responsive"
      data-numposts="5"
      data-order-by="social"
      data-href="https://developers.facebook.com/docs/plugins/comments">
    </amp-facebook-comments>
