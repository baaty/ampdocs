---
layout: page
---

### 説明

iframe を作成し、MathML 式を表示

### 使い方

    <amp-mathml 属性>
    </amp-mathml>

### 必要なスクリプト

    <script async custom-element="amp-mathml" src="https://cdn.ampproject.org/v0/amp-mathml-0.1.js"></script>

### 属性

| 属性名             | 説明                                                   |
|--------------------|--------------------------------------------------------|
| data-formula(必須) | レンダリングする数式                                           |
| inline             | インライン                                                  |
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

| レイアウト名   | 説明                      |
|-----------|-------------------------|
| container | 子要素に応じて自動的にサイズ調整 |

### 例

#### 基本的な使い方

    <amp-mathml
      layout="container"
      data-formula="\[x = {-b \pm \sqrt{b^2-4ac} \over 2a}.\]">
    </amp-mathml>

#### inline

    <amp-mathml
      inline
      layout="container"
      data-formula="\(x = {-b \pm \sqrt{b^2-4ac} \over 2a}.\)">
    </amp-mathml>
