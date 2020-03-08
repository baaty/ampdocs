---
layout: page
---

### AMP(アンプ)とは

モバイルページを高速に表示させるフレームワーク  
GoogleがTwitterと共同で開発を進めているAccelerated Mobile Pagesというプロジェクト

### 特徴

- 表示の高速化のためにHTMLに制約を加えた「AMP HTML」
- 高速にコンテンツのロードを行うためのJavaScriptコード「AMP JS」
- コンテンツのキャッシュ配信を行う「Google AMP Cache」

### ルール

- 非同期的に実行されるJavaScriptが原則として禁止
- 動的にサイズが変わるようなコンテンツは提供できない
- CSSは別ファイルに分離できず、スタイル指定はすべてHTMLソースファイル中に記述
- CSSのサイズは最大50KB
