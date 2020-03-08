---
layout: page
---

### 説明

ページに対するアクセス制御

### 使い方

    <script id="amp-access" type="application/json">
      {
        設定
      }
    </script>

### 設定

| 設定名                        | 説明                             |
| ----------------------------- | -------------------------------- |
| authorization                 | 認証エンドポイントのURL         |
| pingback                      | PingbackエンドポイントのURL    |
| noPingback                    | Pingbackの有無                  |
| login                         | ログインページのURL             |
| authorizationFallbackResponse | 認証に失敗した時に使われるJSON  |
| authorizationTimeout          | 認証リクエストのタイムアウト時間 |
| type                          | タイプ(client or server)         |
| namespace                     | 名前空間                         |

### 必要なスクリプト

    <script async custom-element="amp-access" src="https://cdn.ampproject.org/v0/amp-access-0.1.js"></script>

### 例

#### 基本的な使い方

    <script id="amp-access" type="application/json">
      {
        "authorization": "/documentation/examples/api/amp-access/authorization?rid=READER_ID&url=CANONICAL_URL&ref=DOCUMENT_REFERRER&_=RANDOM",
        "pingback": "/documentation/examples/api/amp-access/pingback?rid=READER_ID&url=CANONICAL_URL&ref=DOCUMENT_REFERRER&_=RANDOM",
        "login": {
          "sign-in": "/documentation/examples/api/amp-access/login?rid=READER_ID&url=CANONICAL_URL",
          "sign-out": "/documentation/examples/api/amp-access/logout"
        },
        "authorizationFallbackResponse": {
          "error": true,
          "loggedIn": false,
          "powerUser": false
        }
      }
    </script>
    <span amp-access="NOT loggedIn" role="button" tabindex="0" amp-access-hide>
      <h5>Please login to comment</h5>
      <button on="tap:amp-access.login-sign-in" class="button-primary comment-button">Login</button>
    </span>

#### ログインボタン

    <span amp-access="NOT loggedIn" role="button" tabindex="0" amp-access-hide>
      <h5>Please login to comment</h5>
    <button>
    <script id="amp-access" type="application/json">
      {
        "authorization": "https://ampbyexample.com/samples_templates/comment_section/authorization?rid=READER_ID&url=CANONICAL_URL&ref=DOCUMENT_REFERRER&_=RANDOM",
        "noPingback": "true",
        "login": {
          "sign-in": "https://ampbyexample.com/samples_templates/comment_section/login?rid=READER_ID&url=CANONICAL_URL",
          "sign-out": "https://ampbyexample.com/samples_templates/comment_section/logout"
        },
        "authorizationFallbackResponse": {
          "error": true,
          "loggedIn": false
        }
      }
    </script>
