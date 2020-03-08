---
layout: page
---

### 説明

reCAPTCHA v3トークンをフォーム送信する設定を追加

### 使い方

    <amp-recaptcha-input 属性>
    </amp-recaptcha-input>

### 必要なスクリプト

    <script async custom-element="amp-recaptcha-input" src="https://cdn.ampproject.org/v0/amp-recaptcha-input-0.1.js"></script>
    <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>

### 属性

| 属性名             | 説明                                                   |
|--------------------|--------------------------------------------------------|
| layout(必須)       | レイアウト                                                  |
| name(必須)         | 名前                                                   |
| data-sitekey(必須) | reCAPTCHA v3サイトキー                                      |
| data-action(必須)  | reCAPTCHA v3アクション                                      |
| fallback           | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights            | メディア式に基づいた要素の縦サイズ                                 |
| media              | メディア属性                                               |
| noloading          | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                 | イベントの実行用                                            |
| placeholder        | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes              | メディア式に基づいた要素の横サイズ                                 |
| width              | 横幅                                                   |
| height             | 高さ                                                    |
### レイアウト

| レイアウト名   | 説明        |
|-----------|-----------|
| nodisplay | 要素が非表示 |

### 例

#### 基本的な使い方

    <amp-reach-player
      data-embed-id="default"
      layout="responsive"
      width="560"
      height="315">
    </amp-reach-player>
