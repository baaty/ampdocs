---
layout: page
---

### 説明

ユーザーエクスペリエンスの実験(A/Bテストなど)するために使用

### 使い方

    <amp-experiment>
      <script type="application/json">
        {
          設定内容
        }
      </script>
    </amp-experiment>

### 必要なスクリプト

    <script async custom-element="amp-experiment" src="https://cdn.ampproject.org/v0/amp-experiment-1.0.js"></script>

### 設定

| キー名                | 説明                                |
| --------------------- | ----------------------------------- |
| variants(必須)        | トラフィックの割合(0-100)           |
| sticky                | スティッキーかどうか                |
| consentNotificationId | 実行する前に却下される要素の要素ID |
| cidScope              | CIDスコープ                        |
| group                 | グループ名                          |

### 例

#### 基本的な使い方

    <amp-experiment>
      <script type="application/json">
        {
          "background-color-test": {
            "variants": {
              "yellow": 50,
              "green": 50
            }
          },
          "font-color-test": {
            "sticky": false,
            "variants": {
              "blue": 20,
              "red": 20
            }
          },
          "border-test": {
            "consentNotificationId": "amp-user-notification",
            "variants": {
              "solid": 50,
              "dashed": 50
            }
          }
        }
      </script>
    </amp-experiment>
