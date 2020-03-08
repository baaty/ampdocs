---
layout: page
---

### ページの検出

AMP版と非AMP版のページがある場合に、2つを関連付けるにはlinkタグを使う

#### AMP版と非AMP版の2つがある場合

##### 非AMP版

    <link rel="amphtml" href="https://www.example.com/url/to/amp/document.html">

##### AMP版

    <link rel="canonical" href="https://www.example.com/url/to/full/document.html">

#### どちらか1つしかない場合

    <link rel="canonical" href="https://www.example.com/url/to/amp/document.html">
