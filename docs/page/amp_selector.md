---
layout: page
---

### 説明

フォームの選択肢を表示

### 使い方

    <amp-selector 属性>
    </amp-selector>

### 必要なスクリプト

    <script async custom-element="amp-selector" src="https://cdn.ampproject.org/v0/amp-selector-0.1.js"></script>

### 属性

| 属性名               | 説明                                                   |
|----------------------|--------------------------------------------------------|
| disabled             | 使用不可能にする                                          |
| form                 | Form要素                                               |
| multiple             | 複数選択可能                                           |
| name                 | パラメータ名                                                |
| keyboard-select-mode | キーボードナビゲーション動作                                       |
| fallback             | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights              | メディア式に基づいた要素の縦サイズ                                 |
| layout               | レイアウト                                                  |
| media                | メディア属性                                               |
| noloading            | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                   | イベントの実行用                                            |
| placeholder          | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes                | メディア式に基づいた要素の横サイズ                                 |
| width                | 横幅                                                   |
| height               | 高さ                                                    |

### イベント

| イベント名 | 説明                    |
|--------|-----------------------|
| select | ユーザーがオプションを選択したとき実行 |

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| container    | 子要素に応じて自動的にサイズ調整          |
| fill         | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed        | 指定した横幅と高さで固定                |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |
| flex-item    | 親要素や周りの要素に応じて自動的にサイズ調整 |
| nodisplay    | 要素が非表示                        |
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### 基本的な使い方

    <amp-selector
      class="sample-selector"
      layout="container">
      <ul>
        <li option="1">Option 1</li>
        <li option="2">Option 2</li>
      </ul>
    </amp-selector>

#### 複数選択可能

    <amp-selector
      multiple
      layout="container"
      class="sample-selector">
      <ul>
        <li option="1">Option 1</li>
        <li option="2">Option 2</li>
      </ul>
    </amp-selector>

#### アクション

    <amp-selector
      id="actionsSample"
      layout="container"
      class="sample-selector"
      multiple>
      <ul>
        <li option="1">Option 1</li>
        <li option="2">Option 2</li>
      </ul>
    </amp-selector>
    <button on="tap:actionsSample.clear">clear</button>
    <button on="tap:actionsSample.selectUp">selectUp</button>
    <button on="tap:actionsSample.selectUp(delta=2)">selectUp(delta=2)</button>
    <button on="tap:actionsSample.selectDown">selectDown</button>
    <button on="tap:actionsSample.selectDown(delta=2)">selectDown(delta=2)</button>
    <button on="tap:actionsSample.toggle(index=1)">toggle(index=1)</button>
    <button on="tap:actionsSample.toggle(index=1, value=true)">toggle(index=1, value=true)</button>
