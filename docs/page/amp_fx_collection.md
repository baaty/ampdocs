---
layout: page
---

### 説明

フェードイン・フェードアウトのような視覚効果のエフェクトを設定  
任意の要素に付与できる属性が追加させる

### 使い方

    <任意のタグ amp-fx="視覚効果の種類" 属性>
    </任意のタグ>

### 必要なスクリプト

    <script async custom-element="amp-fx-collection" src="https://cdn.ampproject.org/v0/amp-fx-collection-0.1.js"></script>

#### 視覚効果の種類

| 名前            | 説明                                                   |
|-----------------|--------------------------------------------------------|
| parallax        | 視差                                                   |
| fade-in         | フェードイン                                                 |
| fade-in-scroll  | フェードインスクロール                                            |
| float-in-top    | 上のスクロール                                               |
| float-in-bottom | 下にスクロール                                               |
| fly-in-bottom   | 下に移動                                                |
| fly-in-left     | 左に移動                                                |
| fly-in-right    | 右に移動                                                |
| fly-in-top      | 上に移動                                                |
| fallback        | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights         | メディア式に基づいた要素の縦サイズ                                 |
| layout          | レイアウト                                                  |
| media           | メディア属性                                               |
| noloading       | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on              | イベントの実行用                                            |
| placeholder     | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes           | メディア式に基づいた要素の横サイズ                                 |
| width           | 横幅                                                   |
| height          | 高さ                                                    |

#### parallax の属性

| 属性名               | 説明      |
|----------------------|---------|
| data-parallax-factor | スクロール速度 |

#### fade-in の属性

| 属性名            | 説明                          |
|-------------------|-----------------------------|
| data-duration     | アニメーションが行われる期間             |
| data-easing       | アニメーションの継続時間全体にわたって変化 |
| data-margin-start | アニメーションの実行タイミング             |

#### fade-in-scroll の属性

| 属性名            | 説明              |
|-------------------|-----------------|
| data-margin-start | アニメーションの実行タイミング |
| data-margin-end   | アニメーションの終了タイミング |
| data-repeat       | 繰り返し            |

#### fly-in-bottom の属性

| 属性名               | 説明                          |
|----------------------|-----------------------------|
| data-duration        | アニメーションが行われる期間             |
| data-easing          | アニメーションの継続時間全体にわたって変化 |
| data-fly-in-distance | 移動距離                      |
| data-margin-start    | アニメーションの実行タイミング             |

#### fly-in-left の属性

| 属性名               | 説明                          |
|----------------------|-----------------------------|
| data-duration        | アニメーションが行われる期間             |
| data-easing          | アニメーションの継続時間全体にわたって変化 |
| data-fly-in-distance | 移動距離                      |
| data-margin-start    | アニメーションの実行タイミング             |

#### fly-in-right の属性

| 属性名               | 説明                          |
|----------------------|-----------------------------|
| data-duration        | アニメーションが行われる期間             |
| data-easing          | アニメーションの継続時間全体にわたって変化 |
| data-fly-in-distance | 移動距離                      |
| data-margin-start    | アニメーションの実行タイミング             |

#### fly-in-top の属性

| 属性名               | 説明                          |
|----------------------|-----------------------------|
| data-duration        | アニメーションが行われる期間             |
| data-easing          | アニメーションの継続時間全体にわたって変化 |
| data-fly-in-distance | 移動距離                      |
| data-margin-start    | アニメーションの実行タイミング             |

### 例

#### 視差(parallax)

    <div amp-fx="parallax" data-parallax-factor="0.8"></div>

#### 画像

    <amp-img amp-fx="parallax" data-parallax-factor="1.2" width="20" height="20" layout="responsive" src="https://example.com"></amp-img>

#### h1

    <h1 amp-fx="parallax"></h1>

#### フェードイン(fade-in)

    <div amp-fx="fade-in"></div>

#### フェードインスクロール(fade-in-scroll)

    <amp-img amp-fx="fade-in-scroll" width="20" height="20" layout="responsive" src="https://example.com"></amp-img>

#### 下に移動(fly-in-bottom)

    <h1 amp-fx="fly-in-bottom"></h1>

#### 左に移動(fly-in-left)

    <h1 amp-fx="fly-in-left"></h1>

#### 右に移動(fly-in-right)

    <h1 amp-fx="fly-in-right"></h1>

#### 上に移動(fly-in-top)

    <h1 amp-fx="fly-in-top"></h1>

#### 複数指定

    <amp-img amp-fx="fade-in parallax" width="20" height="20" layout="responsive" src="https://example.com"></amp-img>

#### 上のスクロール

    <h1 amp-fx="float-in-top"></h1>

#### 下のスクロール

    <h1 amp-fx="float-in-bottom"></h1>
