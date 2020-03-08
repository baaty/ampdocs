---
layout: page
---

### 説明

[Gfycat Video](https://gfycat.com/)の動画プレーヤーを表示

### 使い方

    <amp-gfycat 属性>
    </amp-gfycat>

### 必要なスクリプト

    <script async custom-element="amp-gfycat" src="https://cdn.ampproject.org/v0/amp-gfycat-0.1.js"></script>

### 属性

| 属性名           | 説明                                                   |
|------------------|--------------------------------------------------------|
| data-gfyid(必須) | GfycatID                                               |
| height(必須)     | 高さ                                                    |
| width(必須)      | 横幅                                                   |
| noautoplay       | 自動再生しない                                            |
| fallback         | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights          | メディア式に基づいた要素の縦サイズ                                 |
| layout           | レイアウト                                                  |
| media            | メディア属性                                               |
| noloading        | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on               | イベントの実行用                                            |
| placeholder      | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes            | メディア式に基づいた要素の横サイズ                                 |

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| fill         | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed        | 指定した横幅と高さで固定                |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |
| flex-item    | 親要素や周りの要素に応じて自動的にサイズ調整 |
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### 基本的な使い方

    <amp-gfycat
      data-gfyid="TautWhoppingCougar"
      width="640"
      height="360"
      layout="responsive">
    </amp-gfycat>

#### 自動再生しない(noautoplay)

    <amp-gfycat
      data-gfyid="LeanMediocreBeardeddragon"
      width="640"
      height="360"
      noautoplay>
    </amp-gfycat>
