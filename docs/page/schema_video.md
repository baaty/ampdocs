---
layout: page
---

### 説明

動画コンテンツ  
Google 検索から動画を見つけて見てもらえやすくなる

### タイプ

| タイプ名       | 説明              |
|-------------|-------------------|
| VideoObject | 動画              |
| ItemList    | 特定の種類のアイテムリスト |
| Clip        | クリップ              |

### プロパティ

#### VideoObject

| プロパティ名              | 説明                                      |
|----------------------|-------------------------------------------|
| description(必須)    | 説明                                      |
| name(必須)           | タイトル                                      |
| thumbnailUrl(必須)   | サムネイル画像                                 |
| uploadDate(必須)     | 最初に公開された日付(ISO8601形式)             |
| contentUrl           | URL                                       |
| duration             | 再生時間                                  |
| embedUrl             | 特定の動画のプレーヤーを指定するURL                 |
| expires              | その日以降は動画が使用できなくなる日付(ISO8601形式) |
| interactionStatistic | 視聴された回数                               |

#### ItemList

| プロパティ名                 | 説明     |
|------------------------|----------|
| itemListElement(必須)   | 注釈     |
| ListItem.position(必須) | 順序位置 |
| ListItem.url(必須)      | URL      |

#### Clip

| プロパティ名           | 説明     |
|-------------------|----------|
| name(必須)        | タイトル     |
| startOffset(必須) | 開始時間 |
| url(必須)         | URL      |
| endOffset         | 終了時間 |

### 例

    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "VideoObject",
      "name": "Introducing the self-driving bicycle in the Netherlands",
      "description": "This spring, Google is introducing the self-driving bicycle in Amsterdam, the world’s premier cycling city. The Dutch cycle more than any other nation in the world, almost 900 kilometres per year per person, amounting to over 15 billion kilometres annually. The self-driving bicycle enables safe navigation through the city for Amsterdam residents, and furthers Google’s ambition to improve urban mobility with technology. Google Netherlands takes enormous pride in the fact that a Dutch team worked on this innovation that will have great impact in their home country.",
      "thumbnailUrl": [
        "https://example.com/photos/1x1/photo.jpg",
        "https://example.com/photos/4x3/photo.jpg",
        "https://example.com/photos/16x9/photo.jpg"
       ],
      "uploadDate": "2016-03-31T08:00:00+08:00",
      "duration": "PT1M54S",
      "contentUrl": "https://www.example.com/video/123/file.mp4",
      "embedUrl": "https://www.example.com/embed/123",
      "interactionStatistic": {
        "@type": "InteractionCounter",
        "interactionType": { "@type": "http://schema.org/WatchAction" },
        "userInteractionCount": 5647018
      }
    }
    </script>
