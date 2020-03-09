---
layout: page
---

### 説明

商品ページ

### タイプ

| タイプ名          | 説明    |
|----------------|---------|
| AggregateOffer | オファーリスト |
| Offer          | オファー    |
| Product        | プロダクト   |

### プロパティ

#### AggregateOffer

| プロパティ名             | 説明                         |
|---------------------|----------------------------|
| lowPrice(必須)      | 全ての商品の中の最低価格         |
| priceCurrency(必須) | 通過を表す文字列(日本円は「JPY」) |
| highPrice           | 全ての商人の中の最高価格         |
| offerCount          | 商品数                       |

#### Offer

| プロパティ名             | 説明                         |   |
|---------------------|----------------------------|---|
| availability(必須)  | 制限のある商品リスト               |   |
| price(必須)         | 価格                         |   |
| priceCurrency(必須) | 通過を表す文字列(日本円は「JPY」) |   |
| itemOffered         | 販売するアイテム                   |   |
| priceValidUntil     | 販売できなくなる日付(ISO8601形式)  |   |
| url                 | 商品の URL                    |   |

#### Product

| プロパティ名         | 説明                       |
|-----------------|--------------------------|
| image(必須)     | 画像                       |
| name(必須)      | 商品名                     |
| aggregateRating | 商品のネストされたaggregateRating |
| brand           | 商品のブランド                  |
| description     | 商品の説明                  |
| offers          | 商品の販売情報              |
| review          | 商品のネストされたReview          |
| gtin8           | グローバル識別子                |
| gtin13          | グローバル識別子                |
| gtin14          | グローバル識別子                |
| mpn             | グローバル識別子                |
| isbn            | グローバル識別子                |
| sku             | 販売者固有の識別子          |

### 例
#### 基本的な使い方
    <script type="application/ld+json">
    {
      "@context": "https://schema.org/",
      "@type": "Product",
      "name": "Executive Anvil",
      "image": [
        "https://example.com/photos/1x1/photo.jpg",
        "https://example.com/photos/4x3/photo.jpg",
        "https://example.com/photos/16x9/photo.jpg"
       ],
      "description": "Sleeker than ACME's Classic Anvil, the Executive Anvil is perfect for the business traveler looking for something to drop from a height.",
      "sku": "0446310786",
      "mpn": "925872",
      "brand": {
        "@type": "Thing",
        "name": "ACME"
      },
      "review": {
        "@type": "Review",
        "reviewRating": {
          "@type": "Rating",
          "ratingValue": "4",
          "bestRating": "5"
        },
        "author": {
          "@type": "Person",
          "name": "Fred Benson"
        }
      },
      "aggregateRating": {
        "@type": "AggregateRating",
        "ratingValue": "4.4",
        "reviewCount": "89"
      },
      "offers": {
        "@type": "Offer",
        "url": "https://example.com/anvil",
        "priceCurrency": "USD",
        "price": "119.99",
        "priceValidUntil": "2020-11-05",
        "itemCondition": "https://schema.org/UsedCondition",
        "availability": "https://schema.org/InStock",
        "seller": {
          "@type": "Organization",
          "name": "Executive Objects"
        }
      }
    }
    </script>

#### メルカリ
    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "Product",
      "url": "https://item.mercari.com/jp/xxxx/",
      "name": "xxx",
      "image": "https://static.mercdn.net/item/detail/orig/photos/xxxx",
      "offers": {
        "@type": "Offer",
        "price": "3400",
        "priceCurrency": "JPY"
      }
    }
    </script>