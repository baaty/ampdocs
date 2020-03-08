---
layout: page
---

### 説明

ユーザから同意を取るためのUIを表示

### 使い方

    <amp-consent layout="nodisplay" id="consent-element">
      <script type="application/json">
        {
          設定
        }
      </script>
      <div id="consent-ui">
        <button on="tap:consent-element.accept" role="button">Accept</button>
        <button on="tap:consent-element.reject" role="button">Reject</button>
        <button on="tap:consent-element.dismiss" role="button">Dismiss</button>
      </div>
    </amp-consent>

### 必要なスクリプト

    <script async custom-element="amp-consent" src="https://cdn.ampproject.org/v0/amp-consent-0.1.js"></script>

### 設定

| 要素名            | 説明                            |
| ----------------- | ------------------------------- |
| consentInstanceId | 識別子                          |
| checkConsentHref  | 指定したURLから構成要素を取得 |
| consentInstanceId | 同意のインスタンスID           |

### 応答要素

| 要素名            | 説明                             |
| ----------------- | -------------------------------- |
| consentRequired   | ユーザの同意が必要かどうか       |
| consentStateValue | 現在の同意状態                   |
| consentString     | 同意文字列                       |
| expireCache       | キャッシュのクリアが必要かどうか |

### レイアウト

| レイアウト名 | 説明         |
| ------------ | ------------ |
| nodisplay    | 要素が非表示 |

### 例

#### 基本的な使い方

    <amp-consent id='ABC' layout='nodisplay' type='_ping_'>
      <script type="application/json">
        {
          "consents": {},
          "postPromptUI": "postPromptUI",
          "clientConfig": {
            "CMP_id": "test_id",
            "other_info": "test_info"
          }
        }
      </script>
      <div id="postPromptUI">
        Post Prompt UI
        <button on="tap:ABC.prompt(consent=_ping_)" role="button">Manage</button>
      </div>
    </amp-consent>
