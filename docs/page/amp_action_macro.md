---
layout: page
---

### 説明

再利用可能なアクションを作成

### 使い方

    <amp-action-macro 属性>
    </amp-action-macro>

### 必要なスクリプト

    <script async custom-element="amp-action-macro" src="https://cdn.ampproject.org/v0/amp-action-macro-0.1.js"></script>

### 属性

| 属性名      | 説明                                                   |
|-------------|--------------------------------------------------------|
| id(必須)    | DataID                                                 |
| execute     | 実行するアクション                                            |
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

    <amp-action-macro
      id="navigate-action"
      action="AMP.navigateTo('http://www.ampproject.org')">
    </amp-action-macro>
    <button on="tap:navigate-action"></button>

#### 引数あり

    <amp-action-macro
      id="scrollable-carousel-macro-args"
      execute="scrollable-carousel.goToSlide(index=x)"
      arguments="x">
    </amp-action-macro>

#### 複数アクション

    <amp-action-macro
      id="scrollable-carousel-macro-multi"
      execute="scrollable-carousel.goToSlide(index=x), scrollable-carousel.goToSlide(index=y)"
      arguments="y,x">
    </amp-action-macro>
