---
layout: page
---

### 説明

広告を動的に表示

### 使い方

    <amp-auto-ads 属性>
    </amp-auto-ads>

### 必要なスクリプト

    <script async custom-element="amp-auto-ads" src="https://cdn.ampproject.org/v0/amp-auto-ads-0.1.js"></script>

### 属性

| 属性名      | 説明                                                   |
|-------------|--------------------------------------------------------|
| type(必須)  | 広告名(adsenseとdoubleclickのみ)                          |
| data-\*     | 広告の詳細設定                                          |
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

### 設定

    {
      Configオブジェクト,
    }

#### Config オブジェクトの属性

| 属性名           | 説明                                         |
|------------------|--------------------------------------------|
| placements(必須) | 広告の設置場所                                |
| attributes       | amp-ad要素に適用する属性値へのマッピングを指定          |
| adConstraints    | ページ上に広告を掲載する場合に使用する必要がある制約を指定 |

#### placements の属性

| 属性名       | 説明                                |
|--------------|-------------------------------------|
| anchor(必須) | 要素の検索に使用する情報                |
| pos(必須)    | 相対的な位置                         |
| type(必須)   | タイプ                                 |
| style        | スタイル                                |
| attributes   | amp-ad要素に適用する属性値へのマッピングを指定 |

#### anchor の属性

| 属性名         | 説明                         |
|----------------|------------------------------|
| selector(必須) | CSSセレクタ                      |
| index          | インデックス                       |
| all            | 選択されたすべての要素を含める必要があるか |
| min_c          | 最小の長さ                     |
| sub            | 任意の要素内で要素を選択        |

#### style の属性

| 属性名 | 説明       |
|--------|----------|
| top_m  | 上余白(px) |
| bot_m  | 下余白(px) |

#### pos の値

| 値 | 説明        |
|----|-----------|
| 1  | 直前        |
| 2  | 最初の子要素 |
| 3  | 最後の子要素 |
| 4  | 直後        |

#### tupe の値

| 値 | 説明         |
|----|------------|
| 1  | バナー広告の位置 |

#### adConstraints の属性

| 属性名                  | 説明                |
|-------------------------|-------------------|
| initialMinSpacing(必須) | 既存の広告との最短距離 |
| subsequentMinSpacing    | 広告の間隔           |
| maxAdCount              | 広告の最大数         |

#### subsequentMinSpacing の属性

| 属性名        | 説明          |
|-------------|-------------|
| adCount(必須) | 広告数        |
| spacing(必須) | 広告の最小間隔 |

### 例

#### タグ

    <amp-auto-ads
      type="adsense"
      data-ad-client="ca-pub-5439573510495356">
    </amp-auto-ads>

#### 設定

    {
      "placements": [
        {
          "anchor": {
            "selector": "DIV#domId",
            "index": 2,
            "sub": {
              "selector": "P.paragraph",
              "all": true,
            },
          },
          "pos": 4,
          "type": 1,
          "style": {
            "top_m": 5,
            "bot_m": 10,
          },
        },
      ]
    }
