---
layout: page
---

### 説明

Twitterのツイートを表示

### 使い方

    <amp-twitter 属性>
    </amp-twitter>

### 必要なスクリプト

    <script async custom-element="amp-twitter" src="https://cdn.ampproject.org/v0/amp-twitter-0.1.js"></script>

### 属性

| 属性名                    | 説明                                                   |   |
|---------------------------|--------------------------------------------------------|---|
| data-tweetid(必須)        | ツイートID                                                 |   |
| height(必須)              | 高さ                                                    |   |
| width(必須)               | 横幅                                                   |   |
| data-momentid             | モーメントID                                                |   |
| data-timeline-source-type | タイムラインタイプ                                              |   |
| data-\*                   | Twitterに渡すパラメータ                                       | [ |
| fallback                  | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |   |
| heights                   | メディア式に基づいた要素の縦サイズ                                 |   |
| layout                    | レイアウト                                                  |   |
| media                     | メディア属性                                               |   |
| noloading                 | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |   |
| on                        | イベントの実行用                                            |   |
| placeholder               | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |   |
| sizes                     | メディア式に基づいた要素の横サイズ                                 |   |

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| fill         | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed        | 指定した横幅と高さで固定                |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |
| flex-item    | 親要素や周りの要素に応じて自動的にサイズ調整 |
| intrinsic    | 指定したアスペクト比に自動的にサイズ調整       |
| nodisplay    | 要素が非表示                        |
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### 基本的な使い方

    <amp-twitter
      width="375"
      height="472"
      layout="responsive"
      data-tweetid="885634330868850689">
    </amp-twitter>

#### Moments

    <amp-twitter
      width=486
      height=1312
      layout="responsive"
      data-momentid="1009149991452135424"
      data-limit="2">
    </amp-twitter>

#### Timelines

    <amp-twitter
      width=486
      height=1312
      layout="responsive"
      data-timeline-source-type="profile"
      data-timeline-screen-name="amphtml"
      data-tweet-limit="5">
    </amp-twitter>
