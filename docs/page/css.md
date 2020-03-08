---
layout: page
---

### スタイルシートについて

AMPでも通常のHTMLと同様にCSSを使ってスタイルを変更

### 使い方

    <head>
      ...
      <style amp-custom>
        この部分にしかCSSは記述できない
      </style>
      ...
    </head>

### 専用 CSS

| スタイル名               | 説明                                                 |
| ------------------------ | ---------------------------------------------------- |
| amp-mode-touch           | AMPがタッチ入力を検出したとき                       |
| amp-mode-mouse           | AMPがマウス入力を検出したとき                       |
| amp-mode-keyboard-active | AMPがキーボードがアクティブであることを検出したとき |

### 使えない CSS

| スタイル名                | 説明                     |
| ------------------------- | ------------------------ |
| !important 修飾子         | 使用不可                 |
| \<link rel="stylesheet"\> | カスタムフォント以外不可 |
| -amp-\*クラス             | 使用不可                 |
| i-amp-\*クラス            | 使用不可                 |

### 制限のある CSS

| スタイル名            | 説明                                             |
| --------------------- | ------------------------------------------------ |
| transition プロパティ | opacity、transform、-vendorPrefix-transform のみ |
| @keyframes {...}      | opacity、transform、-vendorPrefix-transform のみ |

### ルール

- CSSをすべてHTMLのHEAD内に記述
- style要素にはamp-custom属性が必須
- 要領は50KB
