---
layout: page
---

### 説明

データを動的に読み込み、指定したテンプレートを使って表示

### 使い方

    <amp-list 属性>
      <template type="amp-mustache">
        表示内容
      </template>
    </amp-list>

### 必要なスクリプト

    <script async custom-element="amp-list" src="https://cdn.ampproject.org/v0/amp-list-0.1.js"></script>

### 属性

| 属性名                  | 説明                                                   |
|-------------------------|--------------------------------------------------------|
| src(必須)               | コンテンツのURL                                              |
| credentials             | credentialsオプションを定義                                  |
| items                   | レンダリングする配列を特定する式を定義                             |
| max-items               | 最大数                                                 |
| single-item             | 単一の要素配列のように扱う                                   |
| reset-on-refresh        | アクションによって更新されたときに再表示                              |
| \[is-layout-container\] | amp-listのレイアウトがCONTAINERに変更                          |
| binding                 | 評価に基づいてレンダリングをブロックするかどうか                            |
| fallback                | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights                 | メディア式に基づいた要素の縦サイズ                                 |
| layout                  | レイアウト                                                  |
| media                   | メディア属性                                               |
| noloading               | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                      | イベントの実行用                                            |
| placeholder             | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes                   | メディア式に基づいた要素の横サイズ                                 |
| width                   | 横幅                                                   |
| height                  | 高さ                                                    |

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

    <amp-list
      width=10
      height=10
      src="https://data.com/articles.json?ref=CANONICAL_URL">
      <div></div>
    </amp-list>

#### Bind(data-amp-bind-src)

    <amp-list
      data-amp-bind-src="foo.bar"
      width=10
      height=10>
      <div></div>
    </amp-list>

#### アクションによって更新されたときに再表示(reset-on-refresh)

    <amp-list
      reset-on-refresh
      width=10
      height=10
      src="https://data.com/articles.json?ref=CANONICAL_URL">
      <div></div>
    </amp-list>

#### 評価に基づいてレンダリングをブロックするかどうか(binding)

    <amp-list
      binding="refresh"
      width=10
      height=10
      src="https://data.com/articles.json?ref=CANONICAL_URL">
      <div></div>
    </amp-list>

#### auto-resize

    <amp-list
      width=10
      height=10
      src="https://data.com/articles.json?ref=CANONICAL_URL"
      auto-resize>
      <div></div>
    </amp-list>

#### load-more

    <amp-list
      width=10
      height=10
      src="https://data.com/articles.json?ref=CANONICAL_URL"
      load-more="auto">
    </amp-list>

#### load-more-bookmark

    <amp-list
      width=10
      height=10
      src="https://data.com/articles.json?ref=CANONICAL_URL"
      load-more="manual"
      load-more-bookmark="next">
    </amp-list>

#### custom children

    <amp-list
      width=10
      height=10
      src="https://data.com/articles.json?ref=CANONICAL_URL"
      load-more="manual"
      load-more-bookmark="next">
      <amp-list-load-more load-more-button></amp-list-load-more>
      <amp-list-load-more load-more-loading></amp-list-load-more>
      <amp-list-load-more load-more-failed></amp-list-load-more>
      <amp-list-load-more load-more-end></amp-list-load-more>
    </amp-list>
