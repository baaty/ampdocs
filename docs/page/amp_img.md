---
layout: page
---

### 説明

画像を表示  
AMPではimgタグは使えないので、こちらを使う

### 使い方

    <amp-img 属性>
    </amp-img>

### 属性

| 属性名       | 説明                                                   |
|--------------|--------------------------------------------------------|
| height(必須) | 高さ                                                    |
| width(必須)  | 横幅                                                   |
| src          | 画像ファイルのURL                                           |
| srcset       | デバイスの解像度によって、違う画像を表示                           |
| alt          | 代替テキスト                                               |
| attribution  | 画像の属性                                              |
| fallback     | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights      | メディア式に基づいた要素の縦サイズ                                 |
| layout       | レイアウト                                                  |
| media        | メディア属性                                               |
| noloading    | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on           | イベントの実行用                                            |
| placeholder  | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes        | メディア式に基づいた要素の横サイズ                                 |

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| fill         | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed        | 指定した横幅と高さで固定                |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |
| flex-item    | 親要素や周りの要素に応じて自動的にサイズ調整 |
| nodisplay    | 要素が非表示                        |
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### 基本的な使い方

    <amp-img
      alt="A view of the sea"
      src="/static/inline-examples/images/sea.jpg"
      width="900"
      height="675"
      layout="responsive">
    </amp-img>

#### フォールバック画像の指定

    <amp-img
      alt="Mountains"
      width="550"
      height="368"
      src="/static/inline-examples/images/mountains.webp">
      <amp-img
        fallback
        alt="Mountains"
        width="550"
        height="368"
        src="/static/inline-examples/images/mountains.jpg"></amp-img>
    </amp-img>

#### アスペクト比を設定

    <amp-img
      width="1.33"
      height="1"
      alt="A view of the sea"
      src="/static/inline-examples/images/sea.jpg"
      layout="responsive">
    </amp-img>
