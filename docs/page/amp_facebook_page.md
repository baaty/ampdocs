---
layout: page
---

### 説明

Facebookページを表示

### 使い方

    <amp-facebook-page 属性>
    </amp-facebook-page>

### 必要なスクリプト

    <script async custom-element="amp-facebook-page" src="https://cdn.ampproject.org/v0/amp-facebook-page-0.1.js"></script>

### 属性

| 属性名             | 説明                                                   |
|--------------------|--------------------------------------------------------|
| data-href(必須)    | FacebookページのURL                                        |
| data-locale        | ロケール                                                   |
| data-tabs          | レンダリングするタブを指定                                        |
| data-hide-cover    | ヘッダーのカバー写真を非表示                                    |
| data-show-facepile | 好きな友達のプロフィール写真を表示                               |
| data-hide-cta      | アクションボタンのカスタム呼び出しを非表示                             |
| data-small-header  | 小さいヘッダー                                               |
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
| fill         | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed        | 指定した横幅と高さで固定                |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |
| flex-item    | 親要素や周りの要素に応じて自動的にサイズ調整 |
| nodisplay    | 要素が非表示                        |
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### 基本的な使い方

    <amp-facebook-page width=552 height=310
      layout="responsive"
      data-tabs="timeline"
      data-href="https://www.facebook.com/barackobama/">
    </amp-facebook-page>

#### 好きな友達のプロフィール写真を表示(data-show-facepile)

    <amp-facebook-page width="300" height="300"
      layout="fixed"
      data-adapt-container-width="true"
      data-show-facepile="true"
      data-href="https://www.facebook.com/itsdougthepug">
    </amp-facebook-page>
