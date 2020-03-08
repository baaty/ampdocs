---
layout: page
---

### 説明

構造化マークアップとは、Webページの構造を検索エンジンにより分かりやすく伝えるためにHTMLに記述する専用のコードのこと

### 種類

- JSON-LD(Google 推奨)
- microdata
- RDFa

### 書き方

#### JSON-LD

    <script type="application/ld+json">
    {
      @context: "http://schema.org",
      @type: "タイプ名",
      プロパティ名: 値, ...
    }
    </script>

### ルール

- [ウェブマスター向けガイドライン](https://support.google.com/webmasters/answer/35769?hl=ja)
- [構造化データに関する一般的なガイドライン](https://developers.google.com/search/docs/guides/sd-policies?hl=ja)
- [技術に関するガイドライン](https://developers.google.com/search/docs/data-types/article?hl=ja#technical-guidelines)
- [AMP ロゴガイドライン](https://developers.google.com/search/docs/data-types/article?hl=ja#logo-guidelines)

### 例

#### JSON-LD

    <script type="application/ld+json">
    {
      @context: "http://schema.org",
      @type: "Person",
      name: "札幌 太郎",
      birthDate: "2019-09-25"
    }
    </script>

### ツールでマークアップ

- [構造化データ マークアップ支援ツール](https://www.google.com/webmasters/markup-helper/)

### 検証方法

- [構造化データ テストツール](https://search.google.com/structured-data/testing-tool?hl=ja)
