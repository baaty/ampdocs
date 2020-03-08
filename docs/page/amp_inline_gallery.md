---
layout: page
---

### 説明

ページネーションドットやサムネイルを付与したカルーセルを表示

### 使い方

    <amp-inline-gallery 属性>
    </amp-inline-gallery>

### 必要なスクリプト

    <script async custom-element="amp-inline-gallery" src="https://cdn.ampproject.org/v0/amp-inline-gallery-0.1.js"></script>

### 属性

| 属性名      | 説明                                                   |
|-------------|--------------------------------------------------------|
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

### amp-inline-gallery-pagination の属性

| 属性名 | 説明                        |
|--------|---------------------------|
| inset  | ページネーションインジケータをインセットとして表示 |

#### amp-inline-gallery-thumbnails の属性

| 属性名              | 説明 |
|---------------------|------|
| aspect-ratio-height | 高さ  |
| aspect-ratio-width  | 横幅 |
| loop                | ループ  |

### レイアウト

| レイアウト名   | 説明                      |
|-----------|-------------------------|
| container | 子要素に応じて自動的にサイズ調整 |

### 例

#### 基本的な使い方

    <amp-inline-gallery layout="container">
      <div>
        <amp-inline-gallery-thumbnails layout="fixed-height" height="96">
        </amp-inline-gallery-thumbnails>
      </div>
    </amp-inline-gallery>

#### ratio specified

    <amp-inline-gallery layout="container">
      <amp-inline-gallery-thumbnails layout="fixed-height" height="96" aspect-ratio-height="2.0" aspect-ratio-width="3">
      </amp-inline-gallery-thumbnails>
    </amp-inline-gallery>

#### loop

    <amp-inline-gallery layout="container">
      <amp-inline-gallery-thumbnails layout="fixed-height" height="96" loop="true">
      </amp-inline-gallery-thumbnails>
    </amp-inline-gallery>
