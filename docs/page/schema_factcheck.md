---
layout: page
---

### 説明

ファクトチェック  
他者の主張のページが Google の検索結果に表示された時に、ファクトチェックとして自分のページのリンクを表示

### タイプ

| タイプ名       | 説明          |
|-------------|---------------|
| ClaimReview | クレーム評価のレビュー |
| Claim       | クレーム          |
| Rating      | 評価          |

#### ClaimReview

| プロパティ名             | 説明                  |
|---------------------|---------------------|
| claimReviewed(必須) | 評価された主張の簡単な要約 |
| reviewRating(必須)  | 主張の評価             |
| url(必須)           | ファクトチェックの記事のURL     |
| author              | ファクトチェック記事の公開元   |
| datePublished       | ファクトチェックが公開された日    |
| itemReviewed        | 行われた主張を表すオブジェクト   |

#### Claim

| プロパティ名         | 説明                                   |
|-----------------|--------------------------------------|
| appearance      | 主張が表示されるCreativeWorkのURL           |
| author          | 主張者                                 |
| datePublished   | 主張する日付または主張が一般の話題になった日付 |
| firstAppearance | この主張が最初に行われたCreativeWorkのURL      |

#### Rating

| プロパティ名             | 説明              |
|---------------------|------------------|
| alternateName(必須) | 真実度の評価       |
| bestRatin           | 数値による評価       |
| name                | alternateNameと同じ |
| ratingValue         | 数値による評価       |
| worstRating         | 数値による評価       |

### 例

    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "ClaimReview",
      "datePublished": "2016-06-22",
      "url": "http://example.com/news/science/worldisflat.html",
      "claimReviewed": "The world is flat",
      "itemReviewed": {
        "@type": "Claim",
        "author": {
          "@type": "Organization",
          "name": "Square World Society",
          "sameAs": "https://example.flatworlders.com/we-know-that-the-world-is-flat"
        },
        "datePublished": "2016-06-20",
        "appearance": {
          "@type": "OpinionNewsArticle",
          "url": "http://skeptical.example.net/news/a122121",
          "name": "Square Earth - Flat earthers for the Internet age",
          "datePublished": "2016-06-22",
          "author": {
            "@type": "Person",
            "name": "T. Tellar"
          }
        }
      },
      "author": {
        "@type": "Organization",
        "name": "Example.com science watch"
      },
      "reviewRating": {
        "@type": "Rating",
        "ratingValue": "1",
        "bestRating": "5",
        "worstRating": "1",
        "alternateName": "False"
      }
    }
    </script>
