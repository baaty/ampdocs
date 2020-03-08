---
layout: page
---

### 説明

ページを先行でロード

### 使い方

    <amp-next-page 属性>
    </amp-next-page>

### 必要なスクリプト

    <script async custom-element="amp-next-page" src="https://cdn.ampproject.org/v0/amp-next-page-0.1.js"></script>

### 属性

| 属性名      | 説明                                                   |
|-------------|--------------------------------------------------------|
| src         | コンポーネントの構成に使用されるJSONを返すリモートエンドポイントのURL            |
| fallback    | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights     | メディア式に基づいた要素の縦サイズ                                 |
| layout      | レイアウト                                                  |
| media       | メディア属性                                               |
| noloading   | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on          | イベントの実行用                                            |
| placeholder | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes       | メディア式に基づいた要素の横サイズ                                 |
| width       | 横幅                                                   |
| height      | 高さ                                                    |

### 例

#### 基本的な使い方

    <amp-next-page src="https://foo.com/data.json">
      <div separator>
        READ ANOTHER ARTICLE FROM OUR SITE!
      </div>
    </amp-next-page>
