---
layout: page
---

### 説明

パターンに基づいて URL を書き換える

### 使い方

    <amp-link-rewriter 属性>
      <script type="application/json">
        設定
      </script>
    </amp-link-rewriter>

### 必要なスクリプト

    <script async custom-element="amp-link-rewriter" src="https://cdn.ampproject.org/v0/amp-link-rewriter-0.1.js"></script>

### 属性

| 属性名      | 説明                                                   |
|-------------|--------------------------------------------------------|
| layout      | レイアウト                                                  |
| fallback    | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights     | メディア式に基づいた要素の縦サイズ                                 |
| media       | メディア属性                                               |
| noloading   | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on          | イベントの実行用                                            |
| placeholder | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes       | メディア式に基づいた要素の横サイズ                                 |
| width       | 横幅                                                   |
| height      | 高さ                                                    |

### JSON の設定

| 名前         | 説明                                         |
|--------------|----------------------------------------------|
| output(必須) | URL                                          |
| section      | URL書き換えが動作する領域                         |
| attribute    | フィルター処理されたセクションから取得されたアンカー要素に一致するルール |

### レイアウト

| レイアウト名   | 説明        |
|-----------|-----------|
| nodisplay | 要素が非表示 |

### 例

#### 基本的な使い方

    <amp-link-rewriter layout="nodisplay">
      <script type="application/json">
        {
          "output": "https://visit.foo.net?pid=110&url=${href}&cid=${data.customerId}&mid=${data.merchantId}&ref=DOCUMENT_REFERRER&location=SOURCE_URL&rel=${rel}",
          "section": [
            "#track-section"
          ],
          "attribute": {
            "href": "((?!\bskip\\.com\b).)*",
            "class": "content"
          },
          "vars": {
            "customerId": "12345",
            "merchantId": "3234"
          }
        }
      </script>
    </amp-link-rewriter>
