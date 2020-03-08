---
layout: page
---

### 説明

カルーセル

### タイプ

| タイプ名          | 説明              |
|---------------|-----------------|
| ItemList(必須) | 特定の種類のアイテムリスト |
| ListItem(必須) | リスト項目           |

#### ItemList

| プロパティ名               | 説明     |
|----------------------|----------|
| itemListElement(必須) | アイテムのリスト |

#### ListItem

| プロパティ名         | 説明                 |
|----------------|----------------------|
| item(必須)      | オールインワンページのリストで使用  |
| item.name(必須) | 表示されるアイテム名の文字列 |
| item.url(必須)  | アイテムのURL             |
| position(必須)  | カルーセル内でのアイテムの位置   |
| url(必須)       | 概要ページのURL          |

### 例

    <script type="application/ld+json">
    {
      "@context":"https://schema.org",
      "@type":"ItemList",
      "itemListElement":[
        {
          "@type":"ListItem",
          "position":1,
          "url":"http://example.com/coffee_cake.html"
        },
        {
          "@type":"ListItem",
          "position":2,
          "url":"http://example.com/apple_pie.html"
        },
        {
          "@type":"ListItem",
          "position":3,
          "url":"http://example.com/blueberry-pie.html"
        }
      ]
    }
    </script>
