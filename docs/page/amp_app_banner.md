---
layout: page
---

### 説明

アプリのインストールを促進するバナーを表示

### 使い方

    <amp-app-banner 属性>
    </amp-app-banner>

### 必要なスクリプト

    <script async custom-element="amp-app-banner" src="https://cdn.ampproject.org/v0/amp-app-banner-0.1.js"></script>

### 属性

| 属性名            | 説明                                                   |
|-------------------|--------------------------------------------------------|
| id(必須)          | 識別子                                                 |
| layout(必須)      | nodisplay限定                                          |
| open-button(必須) | buttonタグの属性。アプリをインストールするバナーなどを開く                    |
| fallback          | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights           | メディア式に基づいた要素の縦サイズ                                 |
| layout            | レイアウト                                                  |
| media             | メディア属性                                               |
| noloading         | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                | イベントの実行用                                            |
| placeholder       | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes             | メディア式に基づいた要素の横サイズ                                 |
| width             | 横幅                                                   |
| height            | 高さ                                                    |

### 制約

- 子要素として、\<amp-ad\>、\<amp-sticky-ad\>、\<amp-embed\>、\<amp-iframe\>はNG
- 高さは100pxまで
- \<body\>の子要素
- 複数設置はNG

### 例

#### 基本的な使い方

    <amp-app-banner layout="nodisplay" id="demo-app-banner-2134">
      <amp-img src="https://example.com/icon.png" width="60" height="51">
      </amp-img>
      <h3>App Name</h3>
      <p>Experience a richer experience on our mobile app!</p>
      <div class="actions">
        <button open-button>Get the app</button>
      </div>
    </amp-app-banner>
