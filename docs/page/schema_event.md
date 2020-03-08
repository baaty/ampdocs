---
layout: page
---

### 説明

イベント

### タイプ

| タイプ名 | 説明     |
| -------- | -------- |
| Event    | イベント |

### プロパティ

| プロパティ名           | 説明                                     |
| ---------------------- | ---------------------------------------- |
| location(必須)         | ロケーションの付随情報                   |
| location.address(必須) | イベント会場の詳しい所番地               |
| name(必須)             | タイトル                                 |
| startDate(必須)        | 開始日(ISO8601形式)                     |
| description            | イベントの説明                           |
| endDate                | 終了日                                   |
| image                  | 画像のURL                               |
| location.name          | イベントが開催される場所または会場の詳細 |
| offers                 | 販売の付随情報                           |
| offers.availability    | 販売方法                                 |
| offers.price           | 最低価格                                 |
| offers.priceCurrency   | 通過コード                               |
| offers.validFrom       | チェットの発売日                         |
| offers.url             | チケットが購入できるURL                 |
| performer              | パフォーマーの付随情報                   |
| performer.name         | パフォーマーの名前                       |

### 例

    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "Event",
      "name": "The Adventures of Kira and Morrison",
      "startDate": "2025-07-21T19:00",
      "endDate": "2025-07-21T23:00",
      "location": {
        "@type": "Place",
        "name": "Snickerpark Stadium",
        "address": {
          "@type": "PostalAddress",
          "streetAddress": "100 West Snickerpark Dr",
          "addressLocality": "Snickertown",
          "postalCode": "19019",
          "addressRegion": "PA",
          "addressCountry": "US"
        }
      },
      "image": [
        "https://example.com/photos/1x1/photo.jpg",
        "https://example.com/photos/4x3/photo.jpg",
        "https://example.com/photos/16x9/photo.jpg"
       ],
      "description": "The Adventures of Kira and Morrison is coming to Snickertown in a can’t miss performance.",
      "offers": {
        "@type": "Offer",
        "url": "https://www.example.com/event_offer/12345_201803180430",
        "price": "30",
        "priceCurrency": "USD",
        "availability": "https://schema.org/InStock",
        "validFrom": "2024-05-21T12:00"
      },
      "performer": {
        "@type": "PerformingGroup",
        "name": "Kira and Morrison"
      }
    }
    </script>
