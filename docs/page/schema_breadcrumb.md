---
layout: page
---

### 説明

パンくずリスト  
そのページがサイト階層内のどこに位置するかを示すリスト

### タイプ

| タイプ名                | 説明                          |
|---------------------|-----------------------------|
| BreadcrumbList(必須) | リスト内のすべての要素を保持するコンテナアイテム |
| ListItem(必須)       | リスト項目                       |

#### BreadcrumbList

| プロパティ名               | 説明                         |
|----------------------|----------------------------|
| itemListElement(必須) | 特定の順序でリストされたパンくずリストの配列 |

#### ListItem

| プロパティ名        | 説明                  |
|---------------|-----------------------|
| item(必須)     | URL                   |
| name(必須)     | ユーザーに表示されるパンくずのタイトル |
| position(必須) | パンくずリスト内でのパンくずの位置  |

### 例

    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "BreadcrumbList",
      "itemListElement": [{
        "@type": "ListItem",
        "position": 1,
        "name": "Books",
        "item": "https://example.com/books"
      },{
        "@type": "ListItem",
        "position": 2,
        "name": "Authors",
        "item": "https://example.com/books/authors"
      },{
        "@type": "ListItem",
        "position": 3,
        "name": "Ann Leckie",
        "item": "https://example.com/books/authors/annleckie"
      },{
        "@type": "ListItem",
        "position": 4,
        "name": "Ancillary Justice",
        "item": "https://example.com/books/authors/ancillaryjustice"
      }]
    }
    </script>
