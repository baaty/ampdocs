---
layout: page
---

### 説明

AMPプロジェクトが推奨するAMP用ベーステンプレート

### テンプレート

    <!doctype html>
    <html amp lang="en">
      <head>
        <meta charset="utf-8">
        <script async src="https://cdn.ampproject.org/v0.js"></script>
        <title>Hello, AMPs</title>
        <link rel="canonical" href="https://amp.dev/ja/documentation/guides-and-tutorials/start/create/basic_markup/">
        <meta name="viewport" content="width=device-width,minimum-scale=1,initial-scale=1">
        <script type="application/ld+json">
          {
            "@context": "http://schema.org",
            "@type": "NewsArticle",
            "headline": "Open-source framework for publishing content",
            "datePublished": "2015-10-07T12:02:41Z",
            "image": [
              "logo.jpg"
            ]
          }
        </script>
        <style amp-boilerplate>body{-webkit-animation:-amp-start 8s steps(1,end) 0s 1 normal both;-moz-animation:-amp-start 8s steps(1,end) 0s 1 normal both;-ms-animation:-amp-start 8s steps(1,end) 0s 1 normal both;animation:-amp-start 8s steps(1,end) 0s 1 normal both}@-webkit-keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}@-moz-keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}@-ms-keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}@-o-keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}@keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}</style><noscript><style amp-boilerplate>body{-webkit-animation:none;-moz-animation:none;-ms-animation:none;animation:none}</style></noscript>
      </head>
      <body>
        <h1>Welcome to the mobile web</h1>
      </body>
    </html>

### 必須項目

- 先頭に\<!doctype html\>
- \<html ⚡\>（\<html amp\>も可）
- \<head\>と\<body\>
- \<meta charset="utf-8"\>を\<head\>の最初の子要素
- \<script async src="https://cdn.ampproject.org/v0.js"\>\</script\>を\<head\>の2番目の子要素
- \<head\>内に\<link rel="canonical" href="\$SOME_URL"\>
- \<head\>内に\<meta name="viewport" content="width=device-width,minimum-scale=1,initial-scale=1"\>
- \<head\>内にAMPボイラープレートコード
