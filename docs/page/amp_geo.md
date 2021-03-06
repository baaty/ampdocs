---
layout: page
---

### 説明

地理位置情報インターフェイス

### 使い方

    <amp-geo layout="nodisplay">
    </amp-geo>

### 必要なスクリプト

    <script async custom-element="amp-geo" src="https://cdn.ampproject.org/v0/amp-geo-0.1.js"></script>

### レイアウト

| レイアウト名     | 説明                                                   |
|-------------|--------------------------------------------------------|
| nodisplay   | 要素が非表示                                            |
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

    <amp-geo layout="nodisplay">
      <script type="application/json">
      {
        "ISOCountryGroups": {
          "soccer": [ "au", "ca", "ie", "nz", "us", "za" ],
          "football": [ "unknown" ]
        }
      }
      </script>
    </amp-geo>
