---
layout: page
---

### 説明

採用企業のユーザによる評価

### タイプ

| タイプ名                | 説明                       |
| ----------------------- | -------------------------- |
| EmployerAggregateRating | 採用企業のユーザによる評価 |

### プロパティ

| プロパティ名       | 説明                                   |
| ------------------ | -------------------------------------- |
| bestRating(必須)   | レーティングシステムで使用できる最大値 |
| itemReviewed(必須) | 評価の対象となっている組織             |
| ratingCount(必須)  | 採用企業の評価の総数                   |
| ratingValue(必須)  | 採用企業の質の評価を示す数値           |
| worstRating(必須)  | レーティングシステムで使用できる最小値 |

### 例

    <script type="application/ld+json">
    {
      "@context" : "https://schema.org/",
      "@type": "EmployerAggregateRating",
      "itemReviewed": {
        "@type": "Organization",
        "name" : "World's Best Coffee Shop",
        "sameAs" : "http://www.worlds-best-coffee-shop.example.com"
      },
      "ratingValue": "91",
      "bestRating": "100",
      "worstRating": "1",
      "ratingCount" : "10561"
    }
    </script>
