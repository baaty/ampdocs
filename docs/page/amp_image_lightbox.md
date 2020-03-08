---
layout: page
---

### 説明

画像専用のライトボックスを表示

### 使い方

    <amp-image-lightbox 属性>
    </amp-image-lightbox>

### 必要なスクリプト

    <script async custom-element="amp-image-lightbox" src="https://cdn.ampproject.org/v0/amp-image-lightbox-0.1.js"></script>

### 属性

| 属性名                       | 説明                                                   |
|------------------------------|--------------------------------------------------------|
| layout(必須)                 | レイアウト                                                  |
| id(必須)                     | ライトボックス要素のID                                         |
| data-close-button-aria-label | 閉じるボタンに使用するラベル                                      |
| fallback                     | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights                      | メディア式に基づいた要素の縦サイズ                                 |
| layout                       | レイアウト                                                  |
| media                        | メディア属性                                               |
| noloading                    | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                           | イベントの実行用                                            |
| placeholder                  | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes                        | メディア式に基づいた要素の横サイズ                                 |
| width                        | 横幅                                                   |
| height                       | 高さ                                                    |

### レイアウト

| レイアウト名   | 説明        |
|-----------|-----------|
| nodisplay | 要素が非表示 |

### 例

#### 基本的な使い方

    <amp-image-lightbox
      id="lightbox1"
      layout="nodisplay">
    </amp-image-lightbox>
    <amp-img on="tap:lightbox1"
      role="button"
      tabindex="0"
      src="image1.jpg"
      width="200" height="100">
    </amp-img>

#### 閉じるボタンに使用するラベル(data-close-button-aria-label)

    <amp-image-lightbox
      data-close-button-aria-label="Close"
      id="image-lightbox1"
      layout="nodisplay">
    </amp-image-lightbox>
