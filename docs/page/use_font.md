---
layout: page
---

### 説明

Webフォントは、現時点では下記の5つのみ利用可能

- [Typography.com](https://cloud.typography.com)
- [Fonts.com](https://fast.fonts.net)
- [Google Fonts](https://fonts.googleapis.com)
- [Typekit](https://use.typekit.net)
- [Font Awesome](https://maxcdn.bootstrapcdn.com)

### 使い方

#### link

    <link rel="stylesheet" href="URL">

#### @font-face

    <style amp-custom>
      @font-face {
        font-family: "フォント名";
        src: url("URL");
      }
      body {ß
        font-family: "フォント名", serif;
      }
    </style>

### 例

#### link

    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Tangerine">

#### @font-face

    <style amp-custom>
      @font-face {
        font-family: "Bitstream Vera Serif Bold";
        src: url("https://somedomain.org/VeraSeBd.ttf");
      }
      body {
        font-family: "Bitstream Vera Serif Bold", serif;
      }
    </style>
