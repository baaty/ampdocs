---
layout: page
---

### 説明

フライングカーペット(フルスクリーンで画面を表示するUI)を表示

### 使い方

    <amp-fx-flying-carpet 属性>
    </amp-fx-flying-carpet>

### 必要なスクリプト

    <script async custom-element="amp-fx-flying-carpet" src="https://cdn.ampproject.org/v0/amp-fx-flying-carpet-0.1.js"></script>

### 属性

| 属性名       | 説明                                                   |
|--------------|--------------------------------------------------------|
| height(必須) | 高さ                                                    |
| fallback     | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights      | メディア式に基づいた要素の縦サイズ                                 |
| layout       | レイアウト                                                  |
| media        | メディア属性                                               |
| noloading    | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on           | イベントの実行用                                            |
| placeholder  | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes        | メディア式に基づいた要素の横サイズ                                 |
| width        | 横幅                                                   |

### 例

#### 基本的な使い方

    <amp-fx-flying-carpet height="300px">
      <amp-img src="fullscreen.png" width="100vw" height="100vh"></amp-img>
    </amp-fx-flying-carpet>
