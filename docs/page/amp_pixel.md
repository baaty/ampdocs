---
layout: page
---

### 説明

サーバへデータを送信  
ページビューの送信などに使われる

### 使い方

    <amp-pixel 属性>
    </amp-pixel>

### 属性

| 属性名         | 説明                                                   |
|----------------|--------------------------------------------------------|
| src(必須)      | URL                                                    |
| referrerpolicy | リンク先にアクセスする時のリファラーポリシー                               |
| allow-ssr-img  |                                                        |
| fallback       | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights        | メディア式に基づいた要素の縦サイズ                                 |
| layout         | レイアウト                                                  |
| media          | メディア属性                                               |
| noloading      | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on             | イベントの実行用                                            |
| placeholder    | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes          | メディア式に基づいた要素の横サイズ                                 |
| width          | 横幅                                                   |
| height         | 高さ                                                    |

### レイアウト

| レイアウト名   | 説明                |
|-----------|-------------------|
| fixed     | 指定した横幅と高さで固定 |
| nodisplay | 要素が非表示         |

### 例

#### 基本的な使い方

    <amp-pixel
      src="https://foo.com/tracker/foo"
      layout="nodisplay">
    </amp-pixel>

#### リンク先にアクセスする時のリファラーポリシー(referrerpolicy)

    <amp-pixel
      src="https://foo.com/tracker/foo"
      layout="nodisplay"
      referrerpolicy="no-referrer">
    </amp-pixel>
