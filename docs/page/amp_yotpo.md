---
layout: page
---

### 説明

[Yotpo](https://support.yotpo.com/en/on-site/reviews-widget)のオンサイトウィジェットを表示

### 使い方

    <amp-yotpo 属性>
    </amp-yotpo>

### 必要なスクリプト

    <script async custom-element="amp-yotpo" src="https://cdn.ampproject.org/v0/amp-yotpo-0.1.js"></script>

### 属性

| 属性名       | 説明                                                   |
|--------------|--------------------------------------------------------|
| data-app-key | アカウントアプリキー                                             |
| data-\*      | パラメータ                                                  |
| fallback     | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights      | メディア式に基づいた要素の縦サイズ                                 |
| layout       | レイアウト                                                  |
| media        | メディア属性                                               |
| noloading    | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on           | イベントの実行用                                            |
| placeholder  | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes        | メディア式に基づいた要素の横サイズ                                 |
| width        | 横幅                                                   |
| height       | 高さ                                                    |

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| fill         | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed        | 指定した横幅と高さで固定                |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |
| flex-item    | 親要素や周りの要素に応じて自動的にサイズ調整 |
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### ボトムラインウィジェット

    <amp-yotpo
      width="550"
      height="100"
      data-app-key="liSBkl621ZZsb88tsckAs6Bzx6jQeTJTv8CDf8y5"
      data-widget-type="BottomLine"
      data-product-id="9408616206">
    </amp-yotpo>

#### レビューウィジェット

    <amp-yotpo
      width="550"
      height="700"
      layout="responsive"
      data-app-key="liSBkl621ZZsb88tsckAs6Bzx6jQeTJTv8CDf8y5"
      data-widget-type="MainWidget"
      data-product-id="9408616206"
      data-name="hockey skates"
      data-url="https://ranabram.myshopify.com/products/hockey-skates"
      data-image-url="https://ichef.bbci.co.uk/news/320/media/images/83351000/jpg/_83351965_explorer273lincolnshirewoldssouthpicturebynicholassilkstone.jpg"
      data-descriptipn="skates"
      data-yotpo-element-id="1">

   </amp-yotpo>
