---
layout: page
---

### 説明

評論家レビュー

### タイプ

| タイプ名 | 説明     |
| -------- | -------- |
| Review   | レビュー |

### プロパティ

#### Review

| プロパティ名                         | 説明                                                                        |
| ------------------------------------ | --------------------------------------------------------------------------- |
| datePublished(必須)                  | レビューが公開された日付(ISO8601形式)                                      |
| description(必須)                    | レビュー本文                                                                |
| itemReviewed(必須)                   | レビュー対象のアイテム                                                      |
| publisher(必須)                      | レビューサイト運営者の付随情報                                              |
| publisher.name(必須)                 | レビューのサイト運営者の名前                                                |
| itemReviewed.address                 | 特定のビジネス拠点の住所                                                    |
| itemReviewed.address.addressCountry  | 国コード                                                                    |
| itemReviewed.address.addressLocality | 市区町村                                                                    |
| itemReviewed.address.addressRegion   | 都道府県                                                                    |
| itemReviewed.address.postalCode      | 郵便番号                                                                    |
| itemReviewed.address.streetAddress   | 町名、番地                                                                  |
| itemReviewed.author                  | 書籍の著者の付随情報                                                        |
| itemReviewed.author.name             | 書籍の著者名                                                                |
| itemReviewed.isbn                    | 書籍のISBN                                                                 |
| itemReviewed.name                    | レビュー対象の名前                                                          |
| itemReviewed.sameAs                  | レビュー対象のURL                                                          |
| aggregateRating                      | レビュー対象のアイテムに付けられた平均スコア                                |
| aggregateRating.bestRating           | レーティングシステムで使用できる最大値                                      |
| aggregateRating.ratingCount          | レビュー対象のアイテムに付けられた評価の数                                  |
| aggregateRating.ratingValue          | レビュー対象のアイテムに付けられた平均評価                                  |
| aggregateRating.worstRating          | レーティングシステムで使用できる最小値                                      |
| author                               | レビュー投稿者                                                              |
| author.name                          | レビュー投稿者の名前                                                        |
| author.sameAs                        | 投稿者に関するページのURL                                                  |
| inLanguage                           | 言語コード                                                                  |
| itemReviewed.actor                   | 映画のメインキャストに関する付随情報                                        |
| itemReviewed.actor.name              | 俳優の名前                                                                  |
| itemReviewed.actor.sameAs            | 俳優に関するページのURL                                                    |
| itemReviewed.datePublished           | 書籍の出版日、映画の公開日、またはDVDなどのメディアの発売日(ISO8601形式) |
| itemReviewed.director                | 映画の監督に関する付随情報                                                  |
| itemReviewed.director.name           | 監督の名前                                                                  |
| itemReviewed.director.sameAs         | 監督に関するページのURL                                                    |
| itemReviewed.geo                     | ビジネス拠点の地理座標                                                      |
| itemReviewed.geo.latitude            | ビジネス拠点の緯度                                                          |
| itemReviewed.geo.longitude           | ビジネス拠点の経度                                                          |
| itemReviewed.telephone               | ビジネス拠点の電話番号                                                      |
| publisher.sameAs                     | サイト運営者の公式ウェブサイトまたはウィキペディアページのURL              |
| reviewRating                         | レビュー                                                                    |
| reviewRating.bestRating              | レーティングシステムで使用できる最大値                                      |
| reviewRating.ratingValue             | レビュー対象のアイテムに付けられた評価                                      |
| reviewRating.worstRating             | レーティングシステムで使用できる最小値                                      |
| URL                                  | レビューの全文が掲載されているウェブページのURL                            |

### 例

    <script type="application/ld+json">
    {
      "@context":"https://schema.org",
      "@type":"Review",
      "author": {
        "@type":"Person",
        "name":"Lisa Kennedy",
        "sameAs":"https://plus.google.com/114108465800532712602"
      },
      "url": "http://www.localreviews.com/restaurants/1/2/3/daves-steak-house.html",
      "datePublished":"2014-03-13T20:00",
      "publisher": {
          "@type":"Organization",
          "name":"Denver Post",
          "sameAs":"http://www.denverpost.com"
      },
      "description":"Great old fashioned steaks but the salads are sub par.",
      "inLanguage":"en",
      "itemReviewed": {
        "@type":"Restaurant",
        "name": "Dave's Steak House",
        "sameAs": "http://davessteakhouse.example.com",
        "image": "http://davessteakhouse.example.com/logo.jpg",
        "servesCuisine": "Steak House",
        "priceRange": "$$$",
        "address": {
          "@type": "PostalAddress",
          "streetAddress": "148 W 51st St",
          "addressLocality": "New York",
          "addressRegion": "NY",
          "postalCode": "10019",
          "addressCountry": "US"
        },
        "geo": {
          "@type": "GeoCoordinates",
          "latitude": 40.761293,
          "longitude": -73.982294
        },
        "telephone": "+12122459600",
        "aggregateRating": {
          "@type": "AggregateRating",
          "ratingValue": "88",
          "bestRating": "100",
          "ratingCount": "20"
        }
      },
      "reviewRating": {
         "@type":"Rating",
         "worstRating":1,
         "bestRating":4,
         "ratingValue":3.5
      }
    }
    </script>
