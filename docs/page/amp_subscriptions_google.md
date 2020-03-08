---
layout: page
---

### 説明

Subscribe with Googleのサブスクリプションスタイルのアクセスプロトコルを実装

### 使い方

    <script type="application/json" id="amp-subscriptions">
      {
        "services": [
          {
            // Local service configuration
          },
          {
            "serviceId": "subscribe.google.com"
          }
        ]
      }
    </script>

### 必要なスクリプト

    <script async custom-element="amp-subscriptions-google" src="https://cdn.ampproject.org/v0/amp-subscriptions-google-0.1.js"></script>

### 例

#### 基本的な使い方

    <script type="application/json" id="amp-subscriptions">
      {
        "services": [
          {
             // Local service configuration
            "authorizationUrl": "https://...",
            "pingbackUrl": "https://...",
            "actions":{
              "login": "https://...",
              "subscribe": "https://..."
            }
          },
          {
            "serviceId": "subscribe.google.com"
          }
        ]
      }
    </script>
    <script type="application/ld+json">
      {
        "@context": "http://schema.org",
        "@type": "NewsArticle",
        {...},
        "isAccessibleForFree": "False",
        "publisher": {
          "@type": "Organization",
          "name": "The Norcal Tribune",
          "logo": {...}
        },
        "hasPart": {
          "@type": "WebPageElement",
          "isAccessibleForFree": "False",
          "cssSelector" : ".paywall"
        },
        "isPartOf": {
          "@type": ["CreativeWork", "Product"],
          "name" : "The Norcal Tribune",
          "productID": "norcal_tribune.com:basic"
        }
      }
    </script>
