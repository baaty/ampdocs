---
layout: page
---

### 説明

学校の講義や授業など

### タイプ

| タイプ名  | 説明         |
|--------|------------|
| Course | 教育コースの説明 |

### プロパティ

| プロパティ名  | 説明              |
|----------|-------------------|
| Course   | コース               |
| ItemList | 特定の種類のアイテムリスト |

#### Course

| プロパティ名           | 説明     |
|-------------------|----------|
| description(必須) | コースの説明 |
| name(必須)        | コースのタイトル |
| provider          | 組織     |

#### ItemList

| プロパティ名                 | 説明     |
|------------------------|----------|
| itemListElement(必須)   | 注釈     |
| ListItem.position(必須) | 順序位置 |
| ListItem.url(必須)      | URL      |

### 例

    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "Course",
      "name": "Introduction to Computer Science and Programming",
      "description": "Introductory CS course laying out the basics.",
      "provider": {
        "@type": "Organization",
        "name": "University of Technology - Eureka",
        "sameAs": "http://www.ut-eureka.edu"
      }
    }
    </script>
