---
layout: page
---

### 説明

Web フォント読み込み時の設定

### 使い方

    <amp-font 属性>
    </amp-font>

### 必要なスクリプト

    <script async custom-element="amp-font" src="https://cdn.ampproject.org/v0/amp-font-0.1.js"></script>

### 属性

| 属性名                | 説明                                                   |
|-----------------------|--------------------------------------------------------|
| font-family           | Webフォント名                                              |
| timeout               | タイムアウト時間                                             |
| on-load-add-class     | ロード時にドキュメントルートに追加されるCSSクラス名                        |
| on-load-remove-class  | ロード時にドキュメントルートから削除されるCSSクラス名                       |
| on-error-add-class    | タイムアウト時にドキュメントルートに追加されるCSSクラス名                     |
| on-error-remove-class | タイムアウト時にドキュメントルートから削除されるCSSクラス名                    |
| font-weight           | フォントの太さ                                               |
| font-style            | フォントのスタイル                                              |
| font-variant          | フォントのスモールキャップ                                          |
| fallback              | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights               | メディア式に基づいた要素の縦サイズ                                 |
| layout                | レイアウト                                                  |
| media                 | メディア属性                                               |
| noloading             | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                    | イベントの実行用                                            |
| placeholder           | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes                 | メディア式に基づいた要素の横サイズ                                 |
| width                 | 横幅                                                   |
| height                | 高さ                                                    |

### レイアウト

| レイアウト名   | 説明        |
|-----------|-----------|
| nodisplay | 要素が非表示 |

### 例

#### 基本的な使い方

    <amp-font
      layout="nodisplay"
      font-family="My Font"
      timeout="3000"
      on-error-remove-class="my-font-loading"
      on-error-add-class="my-font-missing">
    </amp-font>

#### on-load-add-class

    <amp-font
      layout="nodisplay"
      font-family="Comic AMP"
      timeout="2000"
      on-error-remove-class="comic-amp-font-loading"
      on-error-add-class="comic-amp-font-missing"
      on-load-remove-class="comic-amp-font-loading"
      on-load-add-class="comic-amp-font-loaded">
    </amp-font>

#### フォントの太さ(font-weight)

    <amp-font
      layout="nodisplay"
      font-family="Comic AMP Bold"
      timeout="3000"
      font-weight="bold"
      on-error-remove-class="comic-amp-bold-font-loading"
      on-error-add-class="comic-amp-bold-font-missing"
      on-load-remove-class="comic-amp-bold-font-loading"
      on-load-add-class="comic-amp-bold-font-loaded">
    </amp-font>
