---
layout: page
---

### 説明

カルーセル(画像などを横に並べた、スクロール機能付きの表示エリア)を表示

### 使い方

    <amp-carousel 属性>
      表示したい要素
    </amp-carousel>

### 必要なスクリプト

    <script async custom-element="amp-carousel" src="https://cdn.ampproject.org/v0/amp-carousel-0.2.js"></script>

### 属性

| 属性名                      | 説明                                                   |
|-----------------------------|--------------------------------------------------------|
| type(必須)                  | カルーセルの表示タイプ                                          |
| controls                    | 矢印などのナビゲートを表示                                      |
| data-next-button-aria-label | 次のアイテムのラベル                                            |
| data-prev-button-aria-label | 前のアイテムのラベル                                            |
| data-button-count-format    | カウント形式                                               |
| autoplay                    | 自動再生                                               |
| delay                       | 自動再生時の次のスライドに切り替わる時間(ミリ秒)                   |
| loop                        | ループするか                                                 |
| slide                       | 初めに表示されるインデックス番号                                  |
| fallback                    | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights                     | メディア式に基づいた要素の縦サイズ                                 |
| layout                      | レイアウト                                                  |
| media                       | メディア属性                                               |
| noloading                   | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                          | イベントの実行用                                            |
| placeholder                 | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes                       | メディア式に基づいた要素の横サイズ                                 |
| width                       | 横幅                                                   |
| height                      | 高さ                                                    |

### タイプ

| タイプ名           | 説明                              |
|-----------------|---------------------------------|
| carousel(デフォルト) | 全てのスライドが表示され水平方向にスクロール可能 |
| slides          | 一度に一つのスライドを表示                |

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

    <amp-carousel
      id="scrollable-carousel"
      width="800"
      height="300"
      layout="fixed"
      type="carousel">
      <amp-img src="https://picsum.photos/1600/900?image=110"
        width="400"
        height="225"
        aria-label="Aria labels are cool."></amp-img>
      <amp-img src="https://picsum.photos/1600/900?image=112"
        width="400"
        height="225"></amp-img>
    </amp-carousel>
    button on="tap:scrollable-carousel.goToSlide(index=0)">Go to slide 0</button>
    <button on="tap:scrollable-carousel.goToSlide(index=3)">Go to slide 3</button>
    <button on="tap:scrollable-carousel.goToSlide(index=5)">Go to slide 5</button>

#### いろいろな要素

    <amp-carousel width=400 height=300 layout=responsive type=slides>
      <div>hello world</div>
      <amp-img src="https://lh3.googleusercontent.com/pSECrJ82R7-AqeBCOEPGPM9iG9OEIQ_QXcbubWIOdkY=w400-h300-no-n" layout=fill>
      </amp-img>
    </amp-carousel>

#### 自動再生(autoplay)

    <amp-carousel layout="fixed" width=500 height=500 autoplay delay>
    </amp-carousel>

#### 自動再生時の次のスライドに切り替わる時間を指定(delay)

    <amp-carousel layout="fixed" width=500 height=500 autoplay delay=5000>
    </amp-carousel>

#### 自動再生回数を指定

    <amp-carousel layout="fixed" width=500 height=500 autoplay=5>
    </amp-carousel>
