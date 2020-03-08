---
layout: page
---

### 説明

Twitterカードとは、Twitter上でURLが投稿された際に自動的にURLのページ情報を表示する仕組み

### カードタイプ

| タイプ名            | 説明                                                                     |
| ------------------- | ------------------------------------------------------------------------ |
| summary             | 概要の右側に小さな画像が表示                                             |
| summary_large_image | 大きな画像の下に概要が表示                                               |
| app                 | アプリを紹介用。ツイート上からアプリダウンロードページに直接アクセス可能 |
| player              | 動画や音声を再生                                                         |

### プロパティ

#### summary

| プロパティ名        | 説明                                            |
| ------------------- | ----------------------------------------------- |
| twitter:card(必須)  | カードタイプ                                    |
| twitter:title(必須) | コンテンツのタイトル                            |
| twitter:site        | カードフッターで使用されるWebサイトのユーザ名 |
| twitter:description | コンテンツの概要                                |
| twitter:image       | 画像へのURL                                    |
| twitter:image:alt   | 画像の代替テキスト                              |

#### summary_large_image

| プロパティ名        | 説明                                            |
| ------------------- | ----------------------------------------------- |
| twitter:card(必須)  | カードタイプ                                    |
| twitter:title(必須) | コンテンツのタイトル                            |
| twitter:site        | カードフッターで使用されるWebサイトのユーザ名 |
| twitter:description | コンテンツの概要                                |
| twitter:image       | 画像へのURL                                    |
| twitter:image:alt   | 画像の代替テキスト                              |

#### app

| プロパティ名                    | 説明                                            |
| ------------------------------- | ----------------------------------------------- |
| twitter:card(必須)              | カードタイプ                                    |
| twitter:site(必須)              | カードフッターで使用されるWebサイトのユーザ名 |
| twitter:app:id:iphone(必須)     | AppStoreのアプリID(数値)                      |
| twitter:app:id:ipad(必須)       | AppStoreのアプリID(数値)                      |
| twitter:app:id:googleplay(必須) | GooglePlayのアプリID(文字列)                  |
| twitter:description             | コンテンツの概要                                |
| twitter:app:url:iphone          | アプリのカスタムURLスキーム                   |
| twitter:app:url:ipad            | アプリのカスタムURLスキーム                   |
| twitter:app:country             | 国コード(日本はja)                             |
| twitter:app:url:googleplay      | アプリのカスタムURLスキーム                   |

#### player

| プロパティ名                | 説明                                            |
| --------------------------- | ----------------------------------------------- |
| twitter:card(必須)          | カードタイプ                                    |
| twitter:title(必須)         | コンテンツのタイトル                            |
| twitter:site(必須)          | カードフッターで使用されるWebサイトのユーザ名 |
| twitter:player(必須)        | iFrameプレーヤーへのHTTPS URL                 |
| twitter:player:width(必須)  | iFrameの横幅                                   |
| twitter:player:height(必須) | iFrameの高さ                                   |
| twitter:image(必須)         | 動画の代替画像                                  |
| twitter:description         | コンテンツの概要                                |
| twitter:image:alt           | 動画の代替テキスト                              |

### ルール

- Googleのrobots.txt仕様に準拠してURLをスキャン
- ツイート内でTwitterカードが表示されるURLは最大1つ
- ページごとにカードタイプは最大1つ
- 画像サイズは最小144x144または最大4096x4096で1：1のアスペクト比
- 画像サイズは5MB未満
- 画像形式はJPG、PNG、WEBP、およびGIF

### 確認

- [Card Validator \| Twitter Developers](https://cards-dev.twitter.com/validator)

### 正しく表示されない場合は

- [Troubleshooting cards — Twitter Developers](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/guides/troubleshooting-cards)

### 例

#### summary

    <meta name="twitter:card" content="summary" />
    <meta name="twitter:site" content="@flickr" />
    <meta name="twitter:title" content="Small Island Developing States Photo Submission" />
    <meta name="twitter:description" content="View the album on Flickr." />
    <meta name="twitter:image" content="https://farm6.staticflickr.com/5510/14338202952_93595258ff_z.jpg" />

#### summary_large_image

    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:site" content="@nytimes">
    <meta name="twitter:creator" content="@SarahMaslinNir">
    <meta name="twitter:title" content="Parade of Fans for Houston’s Funeral">
    <meta name="twitter:description" content="NEWARK - The guest list and parade of limousines with celebrities emerging from them seemed more suited to a red carpet event in Hollywood or New York than than a gritty stretch of Sussex Avenue near the former site of the James M. Baxter Terrace public housing project here.">
    <meta name="twitter:image" content="http://graphics8.nytimes.com/images/2012/02/19/us/19whitney-span/19whitney-span-articleLarge.jpg">

#### app

    <meta name="twitter:card" content="app">
    <meta name="twitter:site" content="@TwitterDev">
    <meta name="twitter:description" content="Cannonball is the fun way to create and share stories and poems on your phone. Start with a beautiful image from the gallery, then choose words to complete the story and share it with friends.">
    <meta name="twitter:app:country" content="US">
    <meta name="twitter:app:name:iphone" content="Cannonball">
    <meta name="twitter:app:id:iphone" content="929750075">
    <meta name="twitter:app:url:iphone" content="cannonball://poem/5149e249222f9e600a7540ef">
    <meta name="twitter:app:name:ipad" content="Cannonball">
    <meta name="twitter:app:id:ipad" content="929750075">
    <meta name="twitter:app:url:ipad" content="cannonball://poem/5149e249222f9e600a7540ef">
    <meta name="twitter:app:name:googleplay" content="Cannonball">
    <meta name="twitter:app:id:googleplay" content="io.fabric.samples.cannonball">
    <meta name="twitter:app:url:googleplay" content="http://cannonball.fabric.io/poem/5149e249222f9e600a7540ef">

#### player

    <meta name="twitter:card" content="player" />
      <meta name="twitter:site" content="@TwitterDev" />
      <meta name="twitter:title" content="Sample Player Card" />
      <meta name="twitter:description" content="This is a sample video. When you implement, make sure all links are secure." />
      <meta name="twitter:image" content="https://yoursite.com/example.png" />
      <meta name="twitter:player" content="https://yoursite.com/container.html" />
      <meta name="twitter:player:width" content="480" />
      <meta name="twitter:player:height" content="480" />
