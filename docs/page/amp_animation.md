---
layout: page
---

### 説明

アニメーションを定義して表示

### 使い方

    <amp-animation layout="nodisplay">
      <script type="application/json">
        {
          設定
        }
      </script>
    </amp-animation>

### 必要なスクリプト

    <script async custom-element="amp-animation" src="https://cdn.ampproject.org/v0/amp-animation-0.1.js"></script>

### レイアウト

| レイアウト名 | 説明         |
| ------------ | ------------ |
| nodisplay    | 要素が非表示 |

### 例

#### 基本的な使い方

    <amp-animation layout="nodisplay">
      <script type="application/json">
        {
          "target": "target1",
          "duration": 1000,
          "keyframes": {"opacity": 1}
        }
      </script>
    </amp-animation>
