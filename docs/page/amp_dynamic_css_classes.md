---
layout: page
---

### 説明

動的なCSSクラス名をHTML要素に追加

### 使い方

    <style amp-custom>
      処理
    </style>

### 必要なスクリプト

    <script async custom-element="amp-dynamic-css-classes" src="https://cdn.ampproject.org/v0/amp-dynamic-css-classes-0.1.js"></script>

### 例

#### 基本的な使い方

    <style amp-custom>
      body:not(.amp-referrer-pinterest-com) .if-pinterest,
    </style>
