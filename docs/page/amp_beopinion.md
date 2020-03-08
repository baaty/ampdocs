---
layout: page
---

### 説明

[BeOp](https://beop.io/)のコンテンツを表示  
BeOpは主にヨーロッパの主要メディアと連携している広告サイト

### 使い方

    <amp-beopinion 属性>
    </amp-beopinion>

### 必要なスクリプト

    <script async custom-element="amp-beopinion" src="https://cdn.ampproject.org/v0/amp-beopinion-0.1.js"></script>

### 属性

| 属性名             | 説明                                                   |
|--------------------|--------------------------------------------------------|
| data-account(必須) | アカウント ID                                               |
| data-content(必須) | コンテンツ ID                                               |
| data-name          | スロット名前                                               |
| fallback           | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights            | メディア式に基づいた要素の縦サイズ                                 |
| layout             | レイアウト                                                  |
| media              | メディア属性                                               |
| noloading          | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                 | イベントの実行用                                            |
| placeholder        | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes              | メディア式に基づいた要素の横サイズ                                 |
| width              | 横幅                                                   |
| height             | 高さ                                                    |

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| fill         | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed        | 指定した横幅と高さで固定                |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |
| flex-item    | 親要素や周りの要素に応じて自動的にサイズ調整 |
| intrinsic    | 指定したアスペクト比に自動的にサイズ調整       |
| nodisplay    | 要素が非表示                        |
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### 基本的な使い方

    <amp-beopinion
      width="375"
      height="472"
      layout="responsive"
      data-account="589446dd42ee0d6fdd9c3dfd"
      data-content="5a703a2f46e0fb00016d51b3"
      data-name="content-slot">
    </amp-beopinion>
