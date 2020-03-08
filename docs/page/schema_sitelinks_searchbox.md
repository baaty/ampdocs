---
layout: page
---

### 説明

サイトリンク検索ボックス

### タイプ

| タイプ名   | 説明   |
|---------|--------|
| WebSite | Webサイト |

### プロパティ

| プロパティ名                           | 説明           |
|----------------------------------|----------------|
| potentialAction(必須)             | クエリの送信先のURI |
| potentialAction.query-input(必須) | 文字列         |
| potentialAction.target(必須)      | 検索形式       |
| url(必須)                         | サイトのトップページ     |

### 例

    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "WebSite",
      "url": "https://www.example.com/",
      "potentialAction": {
        "@type": "SearchAction",
        "target": "https://query.example.com/search?q={search_term_string}",
        "query-input": "required name=search_term_string"
      }
    }
    </script>
