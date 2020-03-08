---
layout: page
---

### 説明

ソフトウェアアプリ

### タイプ

| タイプ名               | 説明       |
|---------------------|------------|
| SoftwareApplication | ソフトウェアアプリ |

### プロパティ

#### SoftwareApplication

| プロパティ名             | 説明            |
|---------------------|-----------------|
| name(必須)          | アプリ名           |
| offers.price(必須)  | 販売価格        |
| aggregateRating     | アプリの平均レビュースコア |
| review              | レビュー            |
| applicationCategory | アプリのタイプ         |
| operatingSystem     | OS              |

### 例

    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "SoftwareApplication",
      "name": "Angry Birds",
      "operatingSystem": "ANDROID",
      "applicationCategory": "https://schema.org/GameApplication",
      "aggregateRating": {
        "@type": "AggregateRating",
        "ratingValue": "4.6",
        "ratingCount": "8864"
      },
      "offers": {
        "@type": "Offer",
        "price": "1.00",
        "priceCurrency": "USD"
      }
    }
    </script>
