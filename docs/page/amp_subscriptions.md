---
layout: page
---

### 説明

ペイウォールコンテンツを設定

### 使い方

#### JSON-LD

    <script type="application/ld+json">
      {
        "@context": "http://schema.org",
        "@type": "NewsArticle",
        "isAccessibleForFree": false,
        "publisher": {
          "@type": "Organization",
          "name": "The Norcal Tribune"
        },
        "hasPart": {...},
        "isPartOf": {
          "@type": ["CreativeWork", "Product"],
          "name" : "The Norcal Tribune",
          "productID": "norcal_tribune.com:basic"
        }
      }
    </script>

#### Microdata

    <div itemscope itemtype="http://schema.org/NewsArticle">
      <meta itemprop="isAccessibleForFree" content="false" />
      <div
        itemprop="isPartOf"
        itemscope
        itemtype="http://schema.org/CreativeWork http://schema.org/Product">
        <meta itemprop="name" content="The Norcal Tribune" />
        <meta itemprop="productID" content="norcal_tribute.com:basic" />
      </div>
    </div>

### 必要なスクリプト

    <script async custom-element="amp-subscriptions" src="https://cdn.ampproject.org/v0/amp-subscriptions-0.1.js"></script>
