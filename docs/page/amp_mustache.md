---
layout: page
---

### 説明

Mustache形式のテンプレートを表示

### 使い方

#### テンプレート

    <template type="amp-mustache">
    </template>

#### script

    <script type="text/plain" template="amp-mustache">
    </script>

### 必要なスクリプト

    <script async custom-template="amp-mustache" src="https://cdn.ampproject.org/v0/amp-mustache-0.2.js"></script>

### 例

#### amp-list

    <amp-list
      width="auto"
      height="100"
      layout="fixed-height"
      src="/example.json">
      <template type="amp-mustache">
        <amp-analytics>
          <script type="application/json">
            \{\{\{ json_data \}\}\}
          </script>
        <amp-analytics/>
      </template>
    </amp-list>

#### template

    <template type="amp-mustache">
      <div>
        <script type="text/plain" template="amp-mustache">
          Nested Template script tags are not allowed.
        </script>
      </div>
    </template>
