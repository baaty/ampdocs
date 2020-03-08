---
layout: page
---

### 説明

Facebookでシェアされた際に表示されるタイトルや画像などの設定

### 使い方

    <meta property="プロパティ名" content="値" />

### プロパティ

#### 共通

| プロパティ名   | 説明             |
| -------------- | ---------------- |
| og:url         | URL              |
| og:title       | タイトル         |
| og:description | 概要             |
| og:image       | アイキャッチ画像 |
| fb:app_id      | アプリID        |
| og:type        | メディアのタイプ |
| og:locale      | ロケール         |

#### 動画用

| プロパティ名        | 説明                                       |
| ------------------- | ------------------------------------------ |
| og:video            | 動画のURL                                 |
| og:video:secure_url | 動画のセキュアなURL                       |
| og:video:type       | 動画のMIMEタイプ                         |
| og:video:width      | 動画の横幅                                 |
| og:video:height     | 動画の高さ                                 |
| og:image            | ニュースフィードの高画質プレビュー用の画像 |

#### 画像用

| プロパティ名        | 説明                 |
| ------------------- | -------------------- |
| og:image            | 画像のURL           |
| og:image:secure_url | 画像のセキュアなURL |
| og:image:type       | 画像のMIMEタイプ   |
| og:image:width      | 画像の横幅           |
| og:image:height     | 画像の高さ           |

#### 3D アセット用

| プロパティ名 | 説明                  |
| ------------ | --------------------- |
| og:type      | 3Dアセットのタイプ   |
| og:asset     | 3DアセットのURL     |
| og:title     | 3Dアセットのタイトル |

### メディアタイプ

| タイプ名 | 説明         |
| -------- | ------------ |
| article  | 記事         |
| book     | 本           |
| profile  | プロフィーる |
| website  | Webサイト   |

### 確認方法

- [シェアデバッカー](https://developers.facebook.com/tools/debug/)

### 例

    <meta property="og:url" content="http://www.nytimes.com/2015/02/19/arts/international/when-great-minds-dont-think-alike.html" />
    <meta property="og:type" content="article" />
    <meta property="og:title" content="When Great Minds Don’t Think Alike" />
    <meta property="og:description" content="How much does culture influence creative thinking?" />
    <meta property="og:image" content="http://static01.nyt.com/images/2015/02/19/arts/international/19iht-btnumbers19A/19iht-btnumbers19A-facebookJumbo-v2.jpg" />
