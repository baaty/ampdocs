---
layout: page
---

### 説明

自社の営業時間、各部門に関する情報、ビジネスについてのクチコミなどの情報

### タイプ

| タイプ名      | 説明               |
| ------------- | ------------------ |
| LocalBusiness | ビジネス           |
| Restaurant    | レストラン         |
| DaySpa        | エステ             |
| HealthClub    | フィットネスクラブ |

### プロパティ

| プロパティ名                           | 説明                                                    |
| -------------------------------------- | ------------------------------------------------------- |
| @id（必須)                             | URL                                                     |
| address(必須)                          | 場所                                                    |
| name(必須)                             | ビジネスの名前                                          |
| aggregateRating                        | 複数の評価やレビューに基づくローカルビジネスの平均評価 |
| department                             | 単一の部門についてネストされた項目                      |
| geo                                    | ビジネス拠点の地理的座標                                |
| geo.latitude                           | ビジネス拠点の緯度                                      |
| geo.longitude                          | ビジネス拠点の経度                                      |
| menu                                   | 食事を提供するビジネスの場合は、メニューのURL          |
| openingHoursSpecification              | ビジネスの営業時間                                      |
| openingHoursSpecification.closes       | 営業終了時刻をhh:mm:ss形式で指定                      |
| openingHoursSpecification.dayOfWeek    | 営業曜日                                                |
| openingHoursSpecification.opens        | 営業開始時刻をhh:mm:ss形式で指定                      |
| openingHoursSpecification.validFrom    | 営業の開始日をYYYY-MM-DD形式で指定                    |
| openingHoursSpecification.validThrough | 営業の終了日をYYYY-MM-DD形式で指定                    |
| review                                 | ローカルビジネスのレビュー                             |
| servesCuisine                          | レストランで提供する料理の種類                          |
| telephone                              | 電話番号                                                |
| url                                    | URL                                                     |

### 例

    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "Restaurant",
      "image": [
        "https://example.com/photos/1x1/photo.jpg",
        "https://example.com/photos/4x3/photo.jpg",
        "https://example.com/photos/16x9/photo.jpg"
       ],
      "@id": "http://davessteakhouse.example.com",
      "name": "Dave's Steak House",
      "address": {
        "@type": "PostalAddress",
        "streetAddress": "148 W 51st St",
        "addressLocality": "New York",
        "addressRegion": "NY",
        "postalCode": "10019",
        "addressCountry": "US"
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
          "name": "Lillian Ruiz"
        }
      },
      "geo": {
        "@type": "GeoCoordinates",
        "latitude": 40.761293,
        "longitude": -73.982294
      },
      "url": "http://www.example.com/restaurant-locations/manhattan",
      "telephone": "+12122459600",
      "servesCuisine": "American",
      "priceRange": "$$$",
      "openingHoursSpecification": [
        {
          "@type": "OpeningHoursSpecification",
          "dayOfWeek": [
            "Monday",
            "Tuesday"
          ],
          "opens": "11:30",
          "closes": "22:00"
        },
        {
          "@type": "OpeningHoursSpecification",
          "dayOfWeek": [
            "Wednesday",
            "Thursday",
            "Friday"
          ],
          "opens": "11:30",
          "closes": "23:00"
        },
        {
          "@type": "OpeningHoursSpecification",
          "dayOfWeek": "Saturday",
          "opens": "16:00",
          "closes": "23:00"
        },
        {
          "@type": "OpeningHoursSpecification",
          "dayOfWeek": "Sunday",
          "opens": "16:00",
          "closes": "22:00"
        }
      ],
      "menu": "http://www.example.com/menu",
      "acceptsReservations": "True"
    }
    </script>
