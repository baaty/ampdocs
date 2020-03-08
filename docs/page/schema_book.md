---
layout: page
---

### 説明

書籍など  
Googole検索で見つけた書籍を検索結果から直接購入することが可能  
決められたプロバイダのみ使用可能

### タイプ

| タイプ名 | 説明 |
|-------|----|
| Book  | 書籍 |

### プロパティ

#### Book

| プロパティ名           | 説明               |
|-------------------|------------------|
| author(必須)      | 書籍の著者          |
| name(必須)        | 書籍のタイトル          |
| url(必須)         | 書籍に関するサイトの URL  |
| workExample(必須) | 書籍の版            |
| @id               | 作品のグローバルに一意のID |
| sameAs            | 書籍のIDを明確にする RL |

#### Country

| プロパティ名    | 説明 |
|-----------|----|
| name(必須) | 国名 |

#### EntryPoint

| プロパティ名              | 説明               |
|---------------------|--------------------|
| actionPlatform(必須) | リンクが動作するプラットフォーム |
| urlTemplate(必須)    | コンテンツへのリンク         |

#### Offer

| プロパティ名             | 説明                   |
|---------------------|----------------------|
| price(必須)         | 商品の価格              |
| priceCurrency(必須) | 通貨(ISO4217形式)      |
| @id                 | グローバルに一意な販売情報のID |
| availability        | 商品アイテムの在庫状況      |
| eligibleRegion      | 販売情報が有効な国       |
| ineligibleRegion    | 販売情報が有効でない国     |

#### Person

| プロパティ名    | 説明               |
|------------|------------------|
| name(必須) | 個人の名前          |
| sameAs     | 書籍のIDを明確にするURL |

#### ReadAction

| プロパティ名                   | 説明            |
|--------------------------|-----------------|
| expectsAcceptanceOf(必須) | アクションの状態のコンテナ |
| target(必須)              | アクションターゲットのコンテナ |

#### workExample

| プロパティ名               | 説明               |
|-----------------------|--------------------|
| bookFormat(必須)      | 書籍の形式          |
| isbn(必須)            | ISBN               |
| potentialAction(必須) | 書籍を読むアクション      |
| @id                   | グローバルに一意のID      |
| author                | 書籍の著者          |
| bookEdition           | 書籍の版            |
| datePublished         | 最初の出版日        |
| name                  | タイトル               |
| sameAs                | 書籍のIDを明確にするURL |
| url                   | 書籍のURL           |

### 例

    <script type="application/ld+json">
    {
      "@context":"https://schema.org",
      "@type":"Book",
      "name" : "The Catcher in the Rye",
      "author": {
        "@type":"Person",
        "name":"J.D. Salinger"
      },
      "url" : "http://www.barnesandnoble.com/store/info/offer/JDSalinger",
      "workExample" : [{
        "@type": "Book",
        "isbn": "031676948",
        "bookEdition": "2nd Edition",
        "bookFormat": "https://schema.org/Hardcover",
        "potentialAction":{
        "@type":"ReadAction",
        "target":
          {
            "@type":"EntryPoint",
            "urlTemplate":"http://www.barnesandnoble.com/store/info/offer/0316769487?purchase=true",
            "actionPlatform":[
              "http://schema.org/DesktopWebPlatform",
              "http://schema.org/IOSPlatform",
              "http://schema.org/AndroidPlatform"
            ]
          },
          "expectsAcceptanceOf":{
            "@type":"Offer",
            "Price":6.99,
            "priceCurrency":"USD",
            "eligibleRegion" : {
              "@type":"Country",
              "name":"US"
            },
            "availability": "https://schema.org/InStock"
          }
        }
      },{
        "@type": "Book",
        "isbn": "031676947",
        "bookEdition": "1st Edition",
        "bookFormat": "https://schema.org/EBook",
        "potentialAction":{
        "@type":"ReadAction",
        "target":
          {
            "@type":"EntryPoint",
            "urlTemplate":"http://www.barnesandnoble.com/store/info/offer/031676947?purchase=true",
            "actionPlatform":[
              "http://schema.org/DesktopWebPlatform",
              "http://schema.org/IOSPlatform",
              "http://schema.org/AndroidPlatform"
            ]
          },
          "expectsAcceptanceOf":{
            "@type":"Offer",
            "Price":1.99,
            "priceCurrency":"USD",
            "eligibleRegion" : {
              "@type":"Country",
              "name":"UK"
            },
            "availability": "https://schema.org/InStock"
          }
        }
      }]
    }
    </script>
