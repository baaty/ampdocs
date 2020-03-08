---
layout: page
---

### 説明

傾きと連動したアニメーション

### 使い方

    <amp-orientation-observer 属性>
    </amp-orientation-observer>

### 必要なスクリプト

    <script async custom-element="amp-orientation-observer" src="https://cdn.ampproject.org/v0/amp-orientation-observer-0.1.js"></script>

### 属性

| 属性名      | 説明                                                   |
|-------------|--------------------------------------------------------|
| alpha-range | アルファ範囲                                               |
| beta-range  | ベータ範囲                                                |
| gamma-range | ガンマ範囲                                                |
| smoothing   | 平滑化                                                 |
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

### レイアウト

| レイアウト名   | 説明        |
|-----------|-----------|
| nodisplay | 要素が非表示 |

### 例

#### 基本的な使い方

    <amp-orientation-observer
      layout="nodisplay">
    </amp-orientation-observer>

#### on

    <amp-orientation-observer
      beta-range="0 180"
      on="beta:clockAnim1.seekTo(percent=event.percent)"
      layout="nodisplay" smoothing="5">
    </amp-orientation-observer>
