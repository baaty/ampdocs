---
layout: page
---

### 説明

ServiceWorkerを埋め込む

### 使い方

    <amp-install-serviceworker 属性>
    </amp-install-serviceworker>

### 必要なスクリプト

    <script async custom-element="amp-install-serviceworker" src="https://cdn.ampproject.org/v0/amp-install-serviceworker-0.1.js"></script>

### 属性

| 属性名                                    | 説明                                                   |
|-------------------------------------------|--------------------------------------------------------|
| src(必須)                                 | ServiceWorkerのURL                                      |
| data-iframe-src                           | インストールするHTMLドキュメントのURL                                 |
| data-scope                                | スコープ                                                   |
| layout                                    | レイアウト                                                  |
| data-no-service-worker-fallback-url-match | 書き換えられるURLに一致する正規表現                            |
| data-no-service-worker-fallback-shell-url | 書き換えるために使用するシェルのURL                                |
| fallback                                  | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights                                   | メディア式に基づいた要素の縦サイズ                                 |
| media                                     | メディア属性                                               |
| noloading                                 | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                                        | イベントの実行用                                            |
| placeholder                               | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes                                     | メディア式に基づいた要素の横サイズ                                 |
| width                                     | 横幅                                                   |
| height                                    | 高さ                                                    |

### 例

#### 基本的な使い方

    <amp-install-serviceworker
      src="https://www.your-domain.com/serviceworker.js"
      data-iframe-src="https://www.your-domain.com/install-serviceworker.html"
      layout="nodisplay">
    </amp-install-serviceworker>
