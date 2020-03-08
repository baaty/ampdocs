---
layout: page
---

### 説明

[Poool](https://poool.tech/)ペイウォールを表示

### 使い方

#### HTML

    <section poool-access-preview amp-access="NOT access">
    </section>
    <section poool-access-content amp-access="access" amp-access-hide>
    </section>
    <section amp-access="NOT error AND NOT access" id="poool">
    </section>

#### 設定

    <script id="amp-access" type="application/json">
      {
        "vendor": "poool",
        "poool": {
          設定
        }
      }
    </script>

### 必要なスクリプト

    <script async custom-element="amp-access-poool" src="https://cdn.ampproject.org/v0/amp-access-poool-0.1.js"></script>

### 設定

| 設定名             | 説明                                                                      |
| ------------------ | ------------------------------------------------------------------------- |
| bundleID(必須)     | アプリID(ダッシュボードで確認可能)                                       |
| itemID(必須)       | 記事ID                                                                   |
| pageType(必須)     | ユーザがページにアクセスしたことを伝えるキー                              |
| debug              | デバックモード                                                            |
| forceWidget        | 現在のウィジェット                                                        |
| loginButtonEnabled | ログインボタンの有無                                                      |
| signatureEnabled   | 記事がロックされた時に表示される署名の有無                                |
| videoClient        | 動画の設定                                                                |
| customSegment      | カスタムグループ/セグメントスラッグでネイティブセグメントをオーバーライド |
| cookiesEnabled     | Cookeを無効                                                              |

### 例

#### 基本的な使い方

    <script id="amp-access" type="application/json">
      {
        "vendor": "poool",
        "poool": {
          "bundleID": "Q9X1R-27SFS-MYC31-MCYQ1",
          "forceWidget": "gift",
          "cookiesEnabled": "true",
          "itemID": "amp-article-test",
          "customSegment": "amp-segment"
        }
      }
    </script>
    <section poool-access-preview amp-access="NOT access">
      <p>権限がありません</p>
    </section>
    <section amp-access="error" amp-access-hide class="error-section">
      Oops... Something broke.
    </section>
    <section poool-access-content amp-access="access" amp-access-hide>
      <p>権限があります</p>
    </section>
    <section amp-access="NOT error AND NOT access" id="poool">
    </section>
