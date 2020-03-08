---
layout: page
---

### 説明

2 つの画像を比較するスライダーを表示

### 使い方

    <amp-image-slider 属性>
    </amp-image-slider>

### 必要なスクリプト

    <script async custom-element="amp-image-slider" src="https://cdn.ampproject.org/v0/amp-image-slider-0.1.js"></script>

### 属性

| 属性名                  | 説明                                                   |
|-------------------------|--------------------------------------------------------|
| disable-hint-reappear   | ヒントを再表示しない                                          |
| initial-slider-position | スライダーバーの位置                                           |
| step-size               | スライダーバーの移動数                                         |
| fallback                | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights                 | メディア式に基づいた要素の縦サイズ                                 |
| layout                  | レイアウト                                                  |
| media                   | メディア属性                                               |
| noloading               | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                      | イベントの実行用                                            |
| placeholder             | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes                   | メディア式に基づいた要素の横サイズ                                 |
| width                   | 横幅                                                   |
| height                  | 高さ                                                    |

### アクション

| アクション名 | 説明                |
|---------|-------------------|
| seekTo  | スライダーバーを移動したら実行 |

### レイアウト

| レイアウト名    | 説明                         |
|------------|----------------------------|
| fixed      | 指定した横幅と高さで固定          |
| intrinsic  | 指定したアスペクト比に自動的にサイズ調整 |
| nodisplay  | 要素が非表示                  |
| responsive | 画面サイズに応じて自動的にサイズ調整   |

### 例

#### 基本的な使い方

    <amp-image-slider
      tabindex="0"
      layout="responsive"
      width="1024"
      height="600">
      <amp-img src="https://unsplash.it/1080/720?image=1037" layout="fill"></amp-img>
      <amp-img src="https://unsplash.it/1080/720?image=1038" layout="fill"></amp-img>
    </amp-image-slider>

#### ヒントを再表示しない(disable-hint-reappear)

    <amp-image-slider
      disable-hint-reappear
      class="hint-hidden"
      tabindex="0"
      layout="responsive"
      width="1024"
      height="600">
      <amp-img src="https://unsplash.it/1080/720?image=1037" layout="fill"></amp-img>
      <amp-img src="https://unsplash.it/1080/720?image=1038" layout="fill"></amp-img>
      <div first class="label">BEFORE</div>
      <div second class="label">AFTER</div>
    </amp-image-slider>
