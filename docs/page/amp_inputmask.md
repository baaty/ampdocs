---
layout: page
---

### 説明

入力マスキング機能

### 必要なスクリプト

    <script async custom-element="amp-inputmask" src="https://cdn.ampproject.org/v0/amp-inputmask-0.1.js"></script>

### 属性

| 属性名          | 説明                                                   |
|-----------------|--------------------------------------------------------|
| mask            | 入力要素に適用するマスクを指定                                |
| mask-trim-zeros | マスクが貼り付けられた値からカスタムマスクに削除するゼロの数を指定              |
| mask-output     | フォームが入力値を送信する方法を指定                            |
| fallback        | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights         | メディア式に基づいた要素の縦サイズ                                 |
| layout          | レイアウト                                                  |
| media           | メディア属性                                               |
| noloading       | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on              | イベントの実行用                                            |
| placeholder     | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes           | メディア式に基づいた要素の横サイズ                                 |
| width           | 横幅                                                   |
| height          | 高さ                                                    |

### サポートされている要素

- input\[type=text\]
- input\[type=tel\]
- input\[type=search\]

### 例

#### 基本的な使い方

    <input mask="L0L_0L0">

#### フォームが入力値を送信する方法を指定（mask-output)

    <input mask="L0L_0L0" mask-output="raw">

#### マスクが貼り付けられた値からカスタムマスクに削除するゼロの数を指定(mask-trim-zeros)

    <input mask="00000" mask-trim-zeros="0" type="tel">
