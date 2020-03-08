---
layout: page
---

### 説明

長いテキストを省略記号で切り捨てて表示

### 使い方

    <amp-truncate-text 属性>
    </amp-truncate-text>

### 必要なスクリプト

    <script async custom-element="amp-truncate-text" src="https://cdn.ampproject.org/v0/amp-truncate-text-0.1.js"></script>

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

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| container    | 子要素に応じて自動的にサイズ調整          |
| fill         | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed        | 指定した横幅と高さで固定                |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |
| flex-item    | 親要素や周りの要素に応じて自動的にサイズ調整 |
| intrinsic    | 指定したアスペクト比に自動的にサイズ調整       |
| nodisplay    | 要素が非表示                        |
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 子要素

| 要素名              | 説明                           |
|---------------------|------------------------------|
| slot = "collapsed"  | 要素に切り捨てられたテキストがある場合に表示 |
| slot = "expanded"   | 要素が展開されたときに表示            |
| slot = "persistent" | 常に表示                        |

### 例

#### 基本的な使い方

    <amp-truncate-text
      layout="fixed"
      height="3em"
      width="20em">
      Some text that may get truncated.
      <button slot="collapsed">See more</button>
      <button slot="expanded">See less</button>
    </amp-truncate-text>

#### overflow-style

    <amp-truncate-text
      overflow-style="right"
      layout="fixed"
      width="150"
      height="80">
      Hello world
      <div slot="collapsed">Expand</div>
    </amp-truncate-text>
