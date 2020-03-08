---
layout: page
---

### 説明

ドイツ生まれの少額決済システム([LaterPay](https://www.laterpay.net/))の設定

### 使い方

#### 表示

##### 権限がある場合

    <div amp-access="access" amp-access-hide="">
    </div>

###### 権限がない場合

    <section amp-access="NOT error AND NOT access" amp-access-hide="">
    </section>

##### エラーの場合

    <section class="error-section" amp-access="error" amp-access-hide="">
    </section>

#### 設定

    <script id="amp-access" type="application/json">
      {
        "vendor": "laterpay",
        "laterpay": {
          "property": value
        }
      }
    </script>

### 必要なスクリプト

    <script async custom-element="amp-access" src="https://cdn.ampproject.org/v0/amp-access-0.1.js">
    <script async custom-element="amp-analytics" src="https://cdn.ampproject.org/v0/amp-analytics-0.1.js">
    <script async custom-element="amp-access-laterpay" src="https://cdn.ampproject.org/v0/amp-access-laterpay-0.2.js">

### laterpay オプション

| 名前                       | 説明                                                                       |
| -------------------------- | -------------------------------------------------------------------------- |
| articleTitleSelector(必須) | ページ内の要素を決定するCSSセレクタ                                      |
| articleId                  | 記事と購入オプションをマッチング                                           |
| jwt                        | 動的な支払い設定用のJWTトークン                                          |
| locale                     | ロケール                                                                   |
| localeMessages             | 生成した購入オプションのリスト内のテキストをカスタマイズまたはローカライズ |
| scrollToTopAfterAuth       | 承認プロセスが成功すると、ページが最上部までスクロールするかどうか         |
| region                     | 地域(eu or us)                                                             |
| sandbox                    | サンドボックスモード                                                       |

### 例

#### 基本的な使い方

    <script id="amp-access" type="application/json">
      {
        "vendor": "laterpay",
        "laterpay": {
          "articleTitleSelector": ".content-container > header > h1",
          "localeMessages": {
            "header": "LaterPay"
          }
        }
      }
    </script>
    <section amp-access="NOT error AND NOT access" amp-access-hide>
      <div id="amp-access-laterpay-dialog" class="amp-access-laterpay"></div>
    </section>
    <section amp-access="error" amp-access-hide class="error-section">
      Oops... Something broke.
    </section>
    <div amp-access="access" amp-access-hide class="article-body" itemprop="articleBody">
    </div>
