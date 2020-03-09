---
layout: page
---

### 説明

レシピ

### タイプ

| タイプ名    | 説明              |
|----------|-------------------|
| ItemList | 特定の種類のアイテムリスト |
| Recipe   | レシピ               |

### プロパティ

#### ItemList

| プロパティ名                 | 説明     |
|------------------------|----------|
| itemListElement(必須)   | 注釈     |
| ListItem.position(必須) | 順序位置 |
| ListItem.url(必須)      | URL      |

#### Recipe

| プロパティ名            | 説明                                    |
|--------------------|-----------------------------------------|
| image(必須)        | 完成した料理の画像                         |
| name(必須)         | レシピ名                                   |
| aggregateRating    | 平均レビュースコア                             |
| author             | レシピの作者                                |
| cookTime           | 調理するのにかかる時間(ISO8601形式)            |
| datePublished      | レシピが公開された日付(ISO8601形式)            |
| description        | 概要                                    |
| keywords           | キーワード                                   |
| nutrition.calories | 1人分のカロリー数                            |
| prepTime           | 調理にかかる時間(ISO8601形式)               |
| recipeCategory     | レシピの食事やコースの種類                       |
| recipeCuisine      | レシピに関連付けられている地域                    |
| recipeIngredient   | レシピに必要な材料                           |
| recipeInstructions | 調理方法                                |
| recipeYield        | レシピの分量                                |
| totalTime          | 料理の準備と調理にかかる合計時間(ISO8601形式) |
| video              | 動画                                    |

### 例
#### 基本的な使い方

    <script type="application/ld+json">
    {
      "@context": "https://schema.org/",
      "@type": "Recipe",
      "video": [
        {
          "name": "Party Coffee Cake",
          "description": "How to make Party Coffee Cake.",
          "thumbnailUrl": [
            "https://example.com/photos/1x1/photo.jpg",
            "https://example.com/photos/4x3/photo.jpg",
            "https://example.com/photos/16x9/photo.jpg"
          ],
          "contentUrl": "http://www.example.com/videos/123_600x400.mp4",
          "embedUrl": "http://www.example.com/videoplayer?id=123",
          "uploadDate": "2018-02-05T08:00:00+08:00"
        }
      ]
    }
    </script>

#### クックパッド

    <script type='application/ld+json'>
    {
      "@context": "https://schema.org",
      "@type": "Recipe",
      "name": "xxxx",
      "headline": "xxxx",
      "author": {
        "@type": "Organization",
        "name": "xxxx",
        "url": "https://cookpad.com/kitchen/xxxx"
      },
      "publisher": {
        "@type": "Organization",
        "name": "クックパッド",
        "url":"https://cookpad.com/",
        "logo": {
          "@type": "ImageObject",
          "url": "https://cookpad.com/assets/logo_cookpad_square.png"
        }
      },
      "mainEntityOfPage": {
        "@type": "WebPage",
        "@id": "https://cookpad.com/recipe/xxxx"
      },
      "image": [
        "https://img.cpcdn.com/recipes/xxxx"
      ],
      "datePublished": "2020-02-27",
      "description": "xxxx",
      "recipeYield": "x人分",
      "recipeIngredient": [
        "xxxx"
      ],
      "recipeInstructions": [
        {
          "@type": "HowToStep",
          "text": "xxxx"
        }
      ],
      "cookTime": "PT30M",
      "recipeCategory": "",
      "keywords": "xxxx",
      "dateModified":"2020-02-28"
    }
    </script>