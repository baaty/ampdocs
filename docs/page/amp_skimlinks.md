---
layout: page
---

### 説明

スキムリンクを実行

### 使い方

    <amp-skimlinks 属性>
    </amp-skimlinks>

### 必要なスクリプト

    <script async custom-element="amp-skimlinks" src="https://cdn.ampproject.org/v0/amp-skimlinks-0.1.js"></script>

### 属性

| 属性名               | 説明                                                   |
|----------------------|--------------------------------------------------------|
| publisher-code(必須) | スキムリンク発行者コード                                        |
| excluded-domains     | 除外ドメイン                                               |
| link-selector        | 追跡するリンクを制限                                         |
| custom-tracking-id   | トラッキングID                                               |
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

### レイアウト

| レイアウト名   | 説明        |
|-----------|-----------|
| nodisplay | 要素が非表示 |

### 例

#### 基本的な使い方

    <amp-skimlinks
      layout="nodisplay"
      publisher-code="123X456">
    </amp-skimlinks>
