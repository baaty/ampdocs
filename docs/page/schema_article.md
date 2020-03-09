---
layout: page
---

### 説明

ニュース、ブログなどの記事ページ  
Googleの検索結果に通常より大きい画像でカルーセルなどで表示  
どのタイプを使えばいいかわからない場合は、Articleの指定がオススメ

### タイプ

| タイプ名    | 説明                 |
| ----------- | -------------------- |
| Article     | 記事全般             |
| NewsArticle | ニュース記事         |
| BlogPosting | ブログ投稿された記事 |

### プロパティ

| プロパティ名                | 説明                                     |
| --------------------------- | ---------------------------------------- |
| author(必須)                | 記事の著者                               |
| author.name(必須)           | 著者の名前                               |
| datePublished(必須)         | 記事が最初に公開された日時(ISO8601 形式) |
| headline(必須)              | 記事の見出し                             |
| image(必須)                 | アイキャッチ画像                         |
| publisher(必須)             | 記事のパブリッシャー                     |
| publisher.logo(必須)        | パブリッシャーのロゴ                     |
| publisher.logo.height(必須) | ロゴの高さ(px)                           |
| publisher.logo.url(必須)    | ロゴのURL                               |
| publisher.logo.width(必須)  | ロゴの横幅                               |
| publisher.name(必須)        | パブリッシャーの名前                     |
| dateModified                | 記事が最近変更された日時(ISO8601 形式)   |
| description                 | 記事の概要                               |
| mainEntityOfPage            | 記事のURL                               |

### 例
#### 基本的な使い方
    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "NewsArticle",
      "mainEntityOfPage": {
        "@type": "WebPage",
        "@id": "https://google.com/article"
      },
      "headline": "Article headline",
      "image": [
        "https://example.com/photos/1x1/photo.jpg",
        "https://example.com/photos/4x3/photo.jpg",
        "https://example.com/photos/16x9/photo.jpg"
       ],
      "datePublished": "2015-02-05T08:00:00+08:00",
      "dateModified": "2015-02-05T09:20:00+08:00",
      "author": {
        "@type": "Person",
        "name": "John Doe"
      },
       "publisher": {
        "@type": "Organization",
        "name": "Google",
        "logo": {
          "@type": "ImageObject",
          "url": "https://google.com/logo.jpg"
        }
      },
      "description": "A most wonderful article"
    }
    </script>

#### アメブロ

    <script data-react-helmet="true" type="application/ld+json">
    {
      "@context": "http://schema.org",
      "@type": "BlogPosting",
      "mainEntityOfPage": {
        "@type": "WebPage",
        "@id": "https://ameblo.jp/staff/"
      },
      "headline": "スタッフブログ",
      "datePublished": "2004-09-28T20:14:31.000+09:00",
      "dateModified": "2020-03-04T20:00:00.000+09:00",
      "author": {
        "@type": "Person",
        "name":" アメーバスタッフ"
      },
      "publisher": {
        "@type": "Organization",
        "name": "Ameba",
        "logo": {
          "@type": "ImageObject",
          "url": "https://stat100.ameba.jp/ameblo/pc/img/amebloJp/abema_logo.png",
          "width": 600,
          "height": 32
        }
      },
      "image": {
        "@type": "ImageObject",
        "url": "https://stat100.ameba.jp/ameblo/sp/img/amp_entryimage.png",
        "width": 960,
        "height": 960
      }
    }
    </script>

#### GameWith
    <script type="application/ld+json">
    {
      "@context": "http://schema.org",
      "@type": "Article",
      "mainEntityOfPage": {
        "@type": "WebPage",
        "@id": "https://xn--eckwa2aa3a9c8j8bve9d.gamewith.jp/"
      },
      "headline": "モンスト攻略 | モンスターストライク徹底解説",
      "description": "GameWithのモンスト（モンスターストライク）攻略サイトです。毎日更新のリセマラランキングや降臨スケジュール、全モンスターの評価やおすすめの運極作成方法などを掲載しています。モンストの最新情報も確認できます。",
      "articleBody": "省略",
      "image": {
        "@type": "ImageObject",
        "url": "https://img.gamewith.jp/assets/images/games/covers/0d808d804fb21e0f557ead7ed401f9b5.png",
        "width": 980,
        "height": 300,
        "datePublished": "2014-03-28T18:22:43+09:00",
        "dateModified": "2020-03-07T11:40:30+09:00",
        "author": {
          "@type": "Person",
          "name": "モンスト攻略班"
        },
        "publisher": {
          "@type": "Organization",
          "name": "GameWith",
          "logo": {
            "@type": "ImageObject",
            "url": "https://xn--eckwa2aa3a9c8j8bve9d.gamewith.jp/assets/img/logo.png",
            "width": 276,
            "height": 46
          }
        }
      }
    }
    </script>
