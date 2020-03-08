---
layout: page
---

### 説明

ライトボックスを表示

### 使い方

    <amp-lightbox 属性>
    </amp-lightbox>

### 必要なスクリプト

    <script async custom-element="amp-lightbox" src="https://cdn.ampproject.org/v0/amp-lightbox-0.1.js"></script>

### 属性

| 属性名       | 説明                                                   |
|--------------|--------------------------------------------------------|
| id(必須)     | ライトボックスのID                                             |
| layout(必須) | レイアウト                                                  |
| animate-in   | アニメーションのスタイル                                           |
| scrollable   | スクロール可能にするか                                          |
| fallback     | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights      | メディア式に基づいた要素の縦サイズ                                 |
| media        | メディア属性                                               |
| noloading    | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on           | イベントの実行用                                            |
| placeholder  | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes        | メディア式に基づいた要素の横サイズ                                 |
| width        | 横幅                                                   |
| height       | 高さ                                                    |

### アクション

| アクション名 | 説明         |
|---------|-------------|
| open    | ライトボックスを開く  |
| close   | ライトボックスを閉じる |

### レイアウト

| レイアウト名   | 説明        |
|-----------|-----------|
| nodisplay | 要素が非表示 |

### 例

#### 基本的な使い方

    <amp-lightbox
      id="lb-0"
      layout="nodisplay">
    </amp-lightbox>

#### アニメーションのスタイル(animate-in)

    <amp-lightbox
      id="lb-3"
      layout="nodisplay"
      animate-in="fly-in-bottom">
    </amp-lightbox>

#### 閉じるボタン

    <amp-lightbox
      scrollable
      id="lightbox-scrollable"
      layout="nodisplay"
      animate-in="fly-in-bottom">
      <button on="tap:lightbox-scrollable.close" class="lightbox-close-button">
        Close Scrollable Lightbox
      </button>
      <p class="fixed">
        <amp-img src="https://lh3.googleusercontent.com/pSECrJ82R7-AqeBCOEPGPM9iG9OEIQ_QXcbubWIOdkY=w300-h200-no" width=300 height=200></amp-img>
      </p>
    </amp-lightbox>

#### 開くボタン

    <amp-lightbox
      scrollable
      id="lightbox-scrollable"
      layout="nodisplay"
      animate-in="fly-in-bottom">
      <p class="fixed">
        <amp-img src="https://lh3.googleusercontent.com/pSECrJ82R7-AqeBCOEPGPM9iG9OEIQ_QXcbubWIOdkY=w300-h200-no" width=300 height=200></amp-img>
      </p>
    </amp-lightbox>
    <button on="tap:lightbox-scrollable">
      Open Scrollable Lightbox
    </button>
