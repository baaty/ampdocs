---
layout: page
---

### 説明

Pinterestのコンテンツを表示

### 使い方

    <amp-pinterest 属性>
    </amp-pinterest>

### 必要なスクリプト

    <script async custom-element="amp-pinterest" src="https://cdn.ampproject.org/v0/amp-pinterest-0.1.js"></script>

### 保存ボタンの属性

| 属性名           | 説明                                                   |
|------------------|--------------------------------------------------------|
| height(必須)     | 高さ                                                    |
| width(必須)      | 横幅                                                   |
| data-do(必須)    | コンテンツの種類                                             |
| data-url(必須)   | コンテンツのURL                                              |
| data-media       | メディアファイルのURL                                           |
| data-description | メディアファイルの詳細                                          |
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

### フォローボタンの属性

| 属性名        | 説明              |
|---------------|-------------------|
| height(必須)  | 高さ               |
| width(必須)   | 横幅              |
| data-do(必須) | コンテンツの種類        |
| data-href     | フォロー対象のユーザーのURL |
| data-label    | フォローボタンのテキスト      |

### ウィジェットの属性

| 属性名         | 説明       |
|----------------|------------|
| height(必須)   | 高さ        |
| width(必須)    | 横幅       |
| data-do(必須)  | コンテンツの種類 |
| data-url(必須) | コンテンツのURL  |
| alt            | 代替テキスト   |

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

#### Save button

    <amp-pinterest
      height="20"
      width="40"
      data-do="buttonPin"
      data-url="http://www.flickr.com/photos/kentbrew/6851755809/"
      data-media="http://farm8.staticflickr.com/7027/6851755809_df5b2051c9_z.jpg"
      data-description="Next stop: Pinterest">
    </amp-pinterest>

#### Pin widget

    <amp-pinterest
      width="245"
      height="330"
      data-do="embedPin"
      data-url="https://www.pinterest.com/pin/99360735500167749/">
    </amp-pinterest>

#### Follow button

    <amp-pinterest
      height="20"
      width="94"
      data-do="buttonFollow"
      data-href="https://www.pinterest.com/kentbrew/"
      data-label="Kent Brewster">
    </amp-pinterest>
