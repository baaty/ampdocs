---
layout: page
---

### 説明

Facebookのいいねボタンを表示

### 使い方

    <amp-facebook-like 属性>
    </amp-facebook-like>

### 必要なスクリプト

    <script async custom-element="amp-facebook-like" src="https://cdn.ampproject.org/v0/amp-facebook-like-0.1.js"></script>

### 属性

| 属性名           | 説明                                                   |
|------------------|--------------------------------------------------------|
| data-href(必須)  | いいねされるページのURL                                          |
| data-locale      | ロケール                                                   |
| data-action      | ボタンに表示するアクション                                        |
| data-colorscheme | 外側のテキストの色                                           |
| data-kd_site     | 13歳未満の子供に向けコンテンツかどうか                             |
| data-layout      | レイアウト                                                  |
| data-ref         | 参照を追跡するためのラベル                                      |
| data-share       | いいねボタンの横に共有ボタンを含めるか                                |
| data-show_faces  | ボタンの下にプロファイル写真を表示するかどうか                           |
| data-size        | ボタンのサイズ                                                |
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

    <amp-facebook-like width=90 height=20
      layout="fixed"
      data-layout="button_count"
      data-href="https://www.facebook.com/testesmegadivertidos/">
    </amp-facebook-like>

#### ロケール(data-locale)

    <amp-facebook-like width=90 height=20
      layout="fixed"
      data-layout="button_count"
      data-href="https://www.facebook.com/testesmegadivertidos/"
      data-locale="fr_FR">
    </amp-facebook-like>

#### ボタンの下にプロファイル写真を表示する(data-show-faces)

    <amp-facebook-like width=225 height=80
      layout="fixed"
      title="Facebook Like"
      data-layout="standard"
      data-size="large"
      data-show-faces="true"
      data-href="https://www.facebook.com/GoogleBrasil">
    </amp-facebook-like>
