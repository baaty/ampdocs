---
layout: page
---

### 説明

検索結果やナレッジグラフで組織のロゴとして使用する画像

### タイプ

| タイプ名        | 説明                     |
|--------------|------------------------|
| Organization | 学校、NGO、企業、クラブなどの組織 |

### プロパティ

| プロパティ名 | 説明                    |
|---------|-------------------------|
| logo    | ロゴのURL                  |
| url     | ロゴに関連付けられたウェブサイトのURL |

### 例

    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "Organization",
      "url": "http://www.example.com",
      "logo": "http://www.example.com/images/logo.png"
    }
    </script>
