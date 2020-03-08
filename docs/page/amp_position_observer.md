---
layout: page
---

### 説明

任意の位置でボタンの表示と非表示を切り替えるアニメーションを表示

### 使い方

    <amp-position-observer 属性>
    </amp-position-observer>

### 必要なスクリプト

    <script async custom-element="amp-position-observer" src="https://cdn.ampproject.org/v0/amp-position-observer-0.1.js"></script>

### 属性

| 属性名              | 説明                                                   |
|---------------------|--------------------------------------------------------|
| target              | 監視する要素のID                                          |
| intersection-ratios | ターゲットをどれだけ表示するか                                      |
| viewport-margins    | ビューポートマージン                                             |
| once                | 一度だけ実行                                             |
| fallback            | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights             | メディア式に基づいた要素の縦サイズ                                 |
| layout              | レイアウト                                                  |
| media               | メディア属性                                               |
| noloading           | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                  | イベントの実行用                                            |
| placeholder         | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes               | メディア式に基づいた要素の横サイズ                                 |
| width               | 横幅                                                   |
| height              | 高さ                                                    |

### レイアウト

| レイアウト名   | 説明        |
|-----------|-----------|
| nodisplay | 要素が非表示 |

### 例

#### 基本的な使い方

    <amp-position-observer
      layout="nodisplay">
    </amp-position-observer>

#### on

    <amp-position-observer
      on="enter:foo;exit:bar;scroll:baz(percent=event.percent)"
      layout="nodisplay">
    </amp-position-observer>
