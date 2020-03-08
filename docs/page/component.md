---
layout: page
---

### AMP HTML宣言

    <!doctype html>
    <html ⚡ lang="ja">

DOCTYPE宣言をして、html ⚡ のlang属性を指定することが必須  
カミナリの部分は「amp」の文字でもOK

### headタグとbodyタグ

    <head>
    </head>
    <body>
    </body>

headタグとbodyタグの指定が必須

### meta要素

    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width,minimum-scale=1,initial-scale=1">

meta要素でUTF-8とviewportを指定することが必須

### boilerplate

    <style amp-boilerplate>body{-webkit-animation:-amp-start 8s steps(1,end) 0s 1 normal both;-moz-animation:-amp-start 8s steps(1,end) 0s 1 normal both;-ms-animation:-amp-start 8s steps(1,end) 0s 1 normal both;animation:-amp-start 8s steps(1,end) 0s 1 normal both}@-webkit-keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}@-moz-keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}@-ms-keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}@-o-keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}@keyframes -amp-start{from{visibility:hidden}to{visibility:visible}}</style><noscript><style amp-boilerplate>body{-webkit-animation:none;-moz-animation:none;-ms-animation:none;animation:none}</style></noscript>

amp-boilerplate（ボイラープレート）はhead内に記述が必須なスタイルシート  

### AMPのJSライブラリを読み込む

    <script async src="https://cdn.ampproject.org/v0.js"></script>

AMP JSライブラリを読み込むことが必須

### canonicalタグ

AMPページの元となる通常ページが存在する場合、rel=amphtmlのlink要素にAMPページへのURLを指定  
逆に、AMPページのrel=canonicalのlink要素には通常ページのURLを指定

#### AMPページに埋め込むタグ

    <link rel="canonical" href="【オリジナルページのURL】">

#### AMPの元となるオリジナルページに埋め込むタグ

    <link rel="amphtml" href="【対象のAMPページURL】">