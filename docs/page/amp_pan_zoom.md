---
layout: page
---

### 説明

インタラクティブコンテンツの表示

### 使い方

    <amp-layout layout="responsive" width="4" height="3">
      <amp-pan-zoom 属性>
        <svg>
          ...
        </svg>
      </amp-pan-zoom>
    </amp-layout>

### 必要なスクリプト

    <script async custom-element="amp-pan-zoom" src="https://cdn.ampproject.org/v0/amp-pan-zoom-0.1.js"></script>

### 属性

| 属性名          | 説明                                                   |
|-----------------|--------------------------------------------------------|
| max-scale       | 最大ズームスケール                                            |
| initial-scale   | ズームスケール                                                |
| initial-x       | 変換x座標                                              |
| initial-y       | 変換y座標                                              |
| reset-on-resize | サイズ変更時のリセット                                         |
| controls        | コントロール                                                 |
| fallback        | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights         | メディア式に基づいた要素の縦サイズ                                 |
| layout          | レイアウト                                                  |
| media           | メディア属性                                               |
| noloading       | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on              | イベントの実行用                                            |
| placeholder     | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes           | メディア式に基づいた要素の横サイズ                                 |
| width           | 横幅                                                   |
| height          | 高さ                                                    |

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| fill         | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed        | 指定した横幅と高さで固定                |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### 基本的な使い方

    <amp-pan-zoom
      layout="responsive"
      width="1"
      height="1">
      <amp-img
        id="img0"
        src="/examples/img/sample.jpg"
        width="641"
        height="481"
        layout="fixed">
      </amp-img>
    </amp-pan-zoom>
