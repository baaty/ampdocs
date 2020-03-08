---
layout: page
---

### 説明

プッシュ通知の購読設定

### 使い方

    <amp-web-push-widget 属性>
    </amp-web-push-widget>

### 必要なスクリプト

    <script async custom-element="amp-web-push" src="https://cdn.ampproject.org/v0/amp-web-push-0.1.js"></script>

### 属性

| 属性名           | 説明                                                   |
|------------------|--------------------------------------------------------|
| visibility(必須) | ウィジェットがいつ表示されるか                                      |
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

| レイアウト名 | 説明 |
| ------------ | ---- |
| nodisplay    |

### 構成

    <amp-web-push
      helper-iframe-url = "https://example.com/helper-iframe.html"
      permission-dialog-url = "https://example.com/permission-dialog.html"
      service- worker-url = "https://example.com/service-worker.js">
    </ amp-web-push >

### 設定

| 名前                  | 説明                        |
|-----------------------|-----------------------------|
| helper-iframe-url     | helper-iframe.htmlへのURL     |
| permission-dialog-url | permission-dialog.htmlへのURL |
| service-worker-url    | JavaScriptサービスワーカーファイルへのURL |
| service-worker-scope  | インストールするService Workerのスコープ |

### 例

#### 基本的な使い方

    <amp-web-push
      id="amp-web-push"
      layout="nodisplay"
      helper-iframe-url="https://example.com/helper-iframe.html"
      permission-dialog-url="https://example.com/permission-dialog.html"
      service-worker-url="https://example.com/service-worker.js">
    </amp-web-push>

#### service-worker-scope

    <amp-web-push
      id="amp-web-push"
      layout="nodisplay"
      helper-iframe-url="https://example.com/helper-iframe.html"
      permission-dialog-url="https://example.com/permission-dialog.html"
      service-worker-url="https://example.com/service-worker.js"
      service-worker-scope="/">
    </amp-web-push>

#### 購読

    <amp-web-push-widget
      visibility="unsubscribed"
      layout="fixed"
      width="250"
      height="80">
      <button on="tap:amp-web-push.subscribe">Subscribe to Notifications</button>
    </amp-web-push-widget>

#### 解除

    <amp-web-push-widget
      visibility="subscribed"
      layout="fixed"
      width="250"
      height="80">
      <button on="tap:amp-web-push.unsubscribe">
        Unsubscribe from Notifications
      </button>
    </amp-web-push-widget>
